# BananaJS WebSocket (WS) Implementation Guide
Overview
This WebSocket server implementation (ws.js) provides real-time communication capabilities for BananaJS applications. It handles client connections, message processing, and broadcasting functionality.

# Core Features
1. Connection Management

# 🚀 BananaJS WebSocket Implementation Guide

## Overview
BananaJS provides built-in WebSocket support for real-time communication between server and clients. This guide covers practical implementation with production-ready examples.

Core Implementation
1. WebSocket Server Setup
Create ws-server.js:

```bash
javascript
const WebSocket = require('ws');
const banana = require('@bananajs/core');

class BananaWebSocket {
  constructor(server) {
    this.wss = new WebSocket.Server({ server });
    this.clients = new Set();
    
    this.setupConnectionHandlers();
  }

  setupConnectionHandlers() {
    this.wss.on('connection', (ws) => {
      this.clients.add(ws);
      console.log('[BananaWS] New connection');

      ws.on('message', (message) => this.handleMessage(ws, message));
      ws.on('close', () => this.handleDisconnect(ws));
      ws.on('error', (error) => this.handleError(ws, error));
      
      this.sendWelcome(ws);
    });
  }

  handleMessage(ws, message) {
    try {
      const data = JSON.parse(message);
      console.log(`[BananaWS] Received: ${data.type}`);
      
      // Broadcast to all clients
      this.broadcast({
        type: 'message',
        payload: data,
        timestamp: Date.now()
      });
    } catch (error) {
      console.error('[BananaWS] Message error:', error);
    }
  }

  handleDisconnect(ws) {
    this.clients.delete(ws);
    console.log('[BananaWS] Client disconnected');
  }

  handleError(ws, error) {
    console.error('[BananaWS] Connection error:', error);
    ws.close();
  }

  sendWelcome(ws) {
    ws.send(JSON.stringify({
      type: 'welcome',
      payload: {
        message: 'Connected to BananaJS WebSocket',
        version: banana.version,
        timestamp: Date.now()
      }
    }));
  }

  broadcast(message) {
    const payload = JSON.stringify(message);
    this.clients.forEach(client => {
      if (client.readyState === WebSocket.OPEN) {
        client.send(payload);
      }
    });
  }
}
```


module.exports = BananaWebSocket;
Integration with BananaJS Server

```bash
1. Add to Your Main Server
javascript
// server.js
const http = require('http');
const banana = require('@bananajs/core');
const BananaWebSocket = require('./ws-server');

const app = banana();
const server = http.createServer(app);
const wsServer = new BananaWebSocket(server);

// Start server
server.listen(process.env.PORT || 3000, () => {
  console.log(`Server running with WebSocket support`);
});
Practical Use Cases
1. Real-Time Notifications
javascript
// Send to specific client
function sendNotification(client, message) {
  if (client.readyState === WebSocket.OPEN) {
    client.send(JSON.stringify({
      type: 'notification',
      payload: { message }
    }));
  }
}
```

2. Live Data Updates

```bash
javascript
// Broadcast data updates
wsServer.broadcast({
  type: 'data_update',
  payload: {
    users: getOnlineUsers(),
    stats: getLiveStats()
  }
});
3. Client Authentication
javascript
// In handleMessage
if (data.type === 'authenticate') {
  if (validateToken(data.token)) {
    ws.isAuthenticated = true;
    ws.userId = data.userId;
  }
}
Production Best Practices
Error Handling

javascript
process.on('uncaughtException', (error) => {
  console.error('WS Server Error:', error);
});
Heartbeat

javascript
// Add to BananaWebSocket class
setInterval(() => {
  this.broadcast({ type: 'ping' });
}, 30000);
Rate Limiting

javascript
// Track messages per connection
const rateLimiter = new Map();

ws.on('message', () => {
  const count = rateLimiter.get(ws) || 0;
  if (count > 100) ws.close();
  rateLimiter.set(ws, count + 1);
});
Client-Side Implementation
javascript
// browser-client.js
const socket = new WebSocket('ws://yourdomain.com');

socket.onmessage = (event) => {
  const data = JSON.parse(event.data);
  switch(data.type) {
    case 'notification':
      showToast(data.payload.message);
      break;
    case 'data_update':
      updateDashboard(data.payload);
      break;
  }
};

function sendMessage(type, payload) {
  if (socket.readyState === WebSocket.OPEN) {
    socket.send(JSON.stringify({ type, payload }));
  }
}
Monitoring and Debugging


```bash

# Enable debug logs
DEBUG=banana:ws* banana dev
Common events to monitor:
connection
message
close
error
Scaling Considerations
Redis Adapter (for multiple servers)
```

```bash

# available soon
npm install @bananajs/ws-redis
javascript
const RedisAdapter = require('@bananajs/ws-redis');
wsServer.adapter = new RedisAdapter();
Load Balancing

```



nginx

```bash
# nginx.conf
map $http_upgrade $connection_upgrade {
  default upgrade;
  '' close;
}

server {
  location /ws {
    proxy_pass http://bananajs_backend;
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection $connection_upgrade;
  }
}
```