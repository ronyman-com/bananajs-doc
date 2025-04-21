# Hot Module Replacement (HMR) in BananaJS 🔥
BananaJS implements a powerful Hot Module Replacement system that supercharges your development workflow without requiring full page reloads.

# How HMR Works in BananaJS
Diagram

graph TD
    A[File Change] --> B[BananaJS Detects Update]
    B --> C[HMRServer]
    C --> D[Compile Changes]
    D --> E[Send Updates to Client]
    E --> F[Smart Module Replacement]
    F --> G[UI Updates Instantly]

# Key Characteristics:
State Preservation: Maintains application state during updates

CSS Injection: Updates styles without reloading

Component Hot Swapping: Replaces components while maintaining DOM state

Error Recovery: Falls back to full reload if HMR fails

Using HMR in Development
Start your dev server with HMR enabled (default):

```bash
banana dev --hmr
Custom HMR Options:
bash
# Specify HMR port
banana dev --hmr --hmr-port 24678

# Disable HMR (fallback to live reload)
banana dev --no-hmr
HMR Configuration
Configure in banana.config.js:
```


```bash
javascript
export default {
  server: {
    hmr: {
      port: 24678,       // Custom HMR port
      protocol: 'ws',    // 'ws' | 'wss'
      overlay: true,     // Show error overlays
      reload: false      // Disable auto-reload fallback
    }
  }
}

```
Framework-Specific HMR Behavior
React Components
Preserves component state

Supports React Fast Refresh

Handles hooks properly

Vue Components
Maintains Vuex/Pinia state

Preserves DOM elements

Supports Vue's own HMR API

CSS Modules
Updates styles without flash
Maintains CSSOM state
Supports PostCSS transformations
Advanced HMR Patterns
Manual HMR API

```bash
javascript
if (import.meta.hot) {
  import.meta.hot.accept('./module.js', (newModule) => {
    // Custom update handler
  })
  
  import.meta.hot.dispose(() => {
    // Cleanup before module is replaced
  })
}
HMR Status Indicators
BananaJS adds these visual cues:
Blue pulse animation: Applying updates
Green checkmark: Update successful
Red error icon: Update failed (error shown)
Troubleshooting HMR
Common issues and solutions:
State Resetting Unexpectedly
```


```bash
javascript
// banana.config.js
export default {
  server: {
    hmr: {
      preserveState: true // Force state preservation
    }
  }
}
HMR Not Working
Ensure you're not using --no-hmr flag
Check for WebSocket connectivity issues
Verify firewall isn't blocking HMR port
Slow HMR Updates
```


```bash
# Try increasing the HMR timeout
banana dev --hmr-timeout 5000

```

Performance Optimizations
BananaJS HMR implements:

Differential updates (only sends changed modules)

Smart change detection

Parallel compilation

Cache-aware invalidation

Comparison with Live Reload
Feature	HMR	Live Reload
State Preserved	✅ Yes	❌ No
Update Speed	⚡ Instant	🐢 Full reload
Network Usage	Low (deltas only)	High (full assets)
Debugging	Easier	Harder
Enable HMR today for a smoother development experience! The average BananaJS developer saves 2-3 hours per week using HMR compared to full reload workflows.