# BananaJS.

[![npm version](https://img.shields.io/npm/v/@ronyman/bananajs.svg?style=flat-square)](https://www.npmjs.com/package/@ronyman/bananajs)
[![npm downloads](https://img.shields.io/npm/dm/@ronyman/bananajs.svg?style=flat-square)](https://www.npmjs.com/package/@ronyman/bananajs)
[![GitHub stars](https://img.shields.io/github/stars/ronyman-com/BananaJS.svg?style=social)](https://github.com/ronyman-com/bananaJS)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

> A modern, fast, and lightweight JavaScript framework for building web applications.

**Official Repository:** [ronyman-com/BananaJS](https://github.com/ronyman-com/@ronyman/bananajs)

![alt text](/assets/images/banana_dev_index.png)

## Create Project or App from browser.
![alt text](/assets/images/banana_dev_dash.png)

## biuld on node 18.18.2

### Banana.js Overview
Banana.js is a modern frontend framework designed for fast development and optimized builds. It leverages native ES modules for development and provides a plugin-based architecture for extensibility. Key features include:
Instant Server Start: Uses native ES modules for lightning-fast development server startup.
Hot Module Replacement (HMR): Updates modules in real-time without a full reload.
Plugin System: Extensible via plugins for handling various file types and optimizations.
Optimized Production Build: Bundles and minifies code for production.

## Core Architecture
Development Server: A lightweight server that serves ES modules directly to the browser.
Build System: A production build tool that bundles and optimizes assets.
Plugin System: A modular system for handling different file types (e.g., JS, CSS, images).
HMR: A mechanism to update modules in the browser without a full reload.


# 1-Create a new project:

# Use template Vue
`banana create my-app --template vue`

# User template react
`banana create my-app ----template react`

# 2-Install dependencies:

`cd my-app`
`npm install or yarn`


# Start the development server:
`yarn dev`
`yarn build`

## Create Project or App from CLI.
![alt text](/assets/images/cli_print.png)


### banana-docs

```bash

bananaJS/ \
├── Banana/                        # Core framework implementation \
│   ├── public/                   # Static assets served directly to clients \
│   │   ├── serve.json                # Server configuration for static hosting \
│   │   ├── assets/                 # Static asset files \
│   │   │   ├── logo.svg                # Brand logo in SVG format \
│   │   │   └── favicon.icon            # Browser tab icon \
│   │   ├── index.html                # Main HTML entry point with root DOM element \
│   │   ├── styles/                  # Global CSS styles (not component-scoped) \
│   │   │   └── main.css                # Framework-wide styles and CSS variables \
│   │   ├── github-icon.svg            # GitHub logo for integrations \
│   ├── src/                       # Framework source code (pre-compilation) \
│   │   ├── components/             # Reusable UI components (JSX) \
│   │   │   ├── Navbar.jsx              # Top navigation bar component \
│   │   │   ├── Sidebar.jsx             # Collapsible side navigation \
│   │   │   └── Footer.jsx              # Page footer with copyright/links \
│   │   ├── pages/                  # Route-based page components \
│   │   │   ├── Home.jsx                # Marketing landing page \
│   │   │   ├── GettingStarted.jsx      # Installation docs \
│   │   │   ├── Features.jsx            # Framework feature highlights \
│   │   │   ├── Plugins.jsx             # Plugin system documentation \
│   │   │   ├── ApiReference.jsx        # Auto-generated API docs \
│   │   │   ├── Examples.jsx            # Interactive code examples \
│   │   │   ├── Blog.jsx                # Blog post listings \
│   │   │   ├── Changelog.jsx           # Version release notes \
│   │   │   └── News.jsx                # Project announcements \
│   │   ├── router/                 # Client-side routing logic \
│   │   │   └── index.js                # Route definitions and history config \
│   │   ├── styles/                 # Component-scoped styles \
│   │   │   └── main.css                # CSS for framework components \
│   │   ├── App.jsx                    # Root application layout component \
│   │   └── main.jsx                   # React DOM render entry point \
│   ├── dist/                       # Production build output (auto-generated) \
│   ├── node_modules/               # NPM dependencies (auto-generated) \
│   ├── .env.example                # Environment variable template \
│   ├── .env.production             # Production-specific configs \
│   └── .env.development            # Development environment vars \
├── bin/                           # Command-line interface tools \
│   ├── banana.config.json            # CLI configuration defaults \
│   ├── build.cjs                     # Production build script (CommonJS) \
│   ├── cli.cjs                       # Main CLI entry point (commands) \
│   ├── server.cjs                    # Development server implementation \
│   └── websocket.cjs                 # WebSocket server implementation \
├── lib/                           # Shared JavaScript libraries \
│   ├── cli-version.cjs               # Version checking/management \
│   ├── create-app.cjs                # Scaffolds new applications \
│   ├── create-project.cjs            # Creates full project structure \
│   └── detect-framework.cjs          # Detects framework in existing projects \
├── public/                        # Global static assets \
│   ├── scripts/                    # Shared JavaScript utilities \
│   ├── styles/                     # Shared CSS resources \
│   │   ├── banana.css                # Core framework styles \
│   │   └── main.css                  # Base normalization/reset styles \
│   ├── dashboard.html                # Admin dashboard entry point \
│   ├── favicon.ico                   # Browser tab icon \
│   ├── github-icon                   # GitHub integration assets \
│   ├── index.html                    # Fallback HTML for SPA \
│   ├── logo.svg                      # Brand logo variants \
│   ├── main.ts                       # TypeScript entry point \
│   └── site.webmanifest              # PWA configuration \
├── src/                           # Application source code \
│   ├── pages/                      # View components \
│   │   ├── Dashboard.jsx              # Admin interface \
│   │   ├── Home.jsx                   # Main landing page \
│   │   └── NotFound.jsx               # 404 error page \
│   │   ├── hooks/                   # Custom React hooks \
│   │   │   └── useWebSocket.js         # WebSocket connection hook \
│   ├── router/                     # Application routing \
│   │   └── index.js                   # Route configuration \
│   ├── services/                   # Business logic/services \
│   │   ├── api.js                      # REST API client \
│   │   └── websocket.js                # Real-time communication \
│   ├── styles/                     # Application styles \
│   │   └── main.css                   # Global style rules \
│   ├── utils/                      # Helper functions \
│   │   └── security.js                 # Authentication utilities \
│   ├── App.jsx                        # Root component \
│   ├── App.module.css                  # CSS Modules styles \
│   ├── index.js                       # Legacy entry point \
│   ├── main.jsx                       # Modern React entry \
│   ├── main.ts                        # TypeScript entry \
│   ├── server.js                      # Express server config \
│   └── styles.scss                    # Sass stylesheet \
├── Projects/                      # Example implementations \
│   └── templates/                 # Blueprint projects \
│       └── default/               # Default starter template \
│           ├── public/               # Static assets served directly to clients \
│           │   ├── index.html        # Main HTML entry point \
│           │   ├── styles/ \
│           │   │   └── main.css \
│           │   ├── main.js \
│           │   ├── logo.svg \
│           │   ├── github-icon.svg \
│           │   └── dashboard.html \
│           ├── src/                  # Framework source code \
│           │   ├── components/ \
│           │   │   ├── Navbar.jsx \
│           │   │   ├── Sidebar.jsx \
│           │   │   └── Footer.jsx \
│           │   ├── pages/ \
│           │   │   ├── Home.jsx \
│           │   │   ├── GettingStarted.jsx \
│           │   │   ├── Features.jsx \
│           │   │   ├── Plugins.jsx \
│           │   │   ├── ApiReference.jsx \
│           │   │   ├── Examples.jsx \
│           │   │   ├── Blog.jsx \
│           │   │   ├── Changelog.jsx \
│           │   │   └── News.jsx \
│           │   ├── router/ \
│           │   │   └── index.js \
│           │   ├── styles/ \
│           │   │   └── main.css \
│           │   ├── App.jsx \
│           │   └── main.jsx \
│           ├── dist/ \
│           ├── node_modules/ \
│           ├── .env.example \
│           ├── .env.production \
│           └── .env.development \
├── templates/                     # Framework-agnostic starters \
│   ├── docs/                      # Documentation site template \
│   │   ├── dist/                  # Built assets directory \
│   │   │   ├── bundle.js \
│   │   │   └── bundle.js.map \
│   │   ├── public/                # Static documentation assets \
│   │   │   └── styles/ \
│   │   │       └── main.css \
│   │   ├── src/                   # Documentation source \
│   │   │   ├── pages/             # Documentation views \
│   │   │   │   ├── ApiReference.vue \
│   │   │   │   ├── Blog.vue \
│   │   │   │   ├── Examples.vue \
│   │   │   │   ├── Features.vue \
│   │   │   │   ├── Home.vue \
│   │   │   │   └── Plugins.vue \
│   │   │   ├── router/            # Vue router config \
│   │   │   │   └── index.js \
│   │   │   ├── styles/            # Component styles \
│   │   │   │   └── main.css \
│   │   │   └── main.js            # Vue initialization \
│   │   ├── App.vue                # Root Vue component \
│   │   └── [config files]         # Build tool configs \
│   ├── react/                     # React starter kit \
│   │   ├── src/                   # React source \
│   │   │   ├── components/        # Presentational components \
│   │   │   ├── styles/            # React styling \
│   │   │   │   └── App.scss       # Sass stylesheet \
│   │   │   ├── App.jsx            # Root component \
│   │   │   └── main.js            # ReactDOM render \
│   │   └── [config files]         # React-specific configs \
│   └── vue/                       # Vue starter kit \
│       ├── public/                # Vue static assets \
│       │   └── index.html         # Mount point \
│       ├── src/                   # Vue source \
│       │   ├── components/        # Vue components \
│       │   │   └── HelloWorld.vue # Example component \
│       │   ├── App.vue            # Root Vue instance \
│       │   └── main.js            # Vue initialization \
│       └── [config files]         # Vue build configs \
├── plugins/                       # Framework extensions \
│   ├── css-modules.js             # CSS Modules support \
│   ├── css.js                     # CSS processing \
│   ├── scss.js                    # Sass compilation \
│   ├── typescript.js              # TypeScript transpilation \
│   ├── react.js                   # React specific transforms \
│   └── vue.js                     # Vue single-file components \
├── dist/                          # Final build artifacts \
│   ├── bundle.js                  # Minified production bundle \
│   ├── main.css                   # Optimized CSS output \
│   └── assets/                    # Processed static assets \
│       ├── logo.svg               # Optimized vector logo \
│       ├── github-icon.svg        # Minified SVG \
│       └── images/                # Compressed images \
├── [Root Config Files]            # Project configuration \
│   ├── banana.config.js           # Framework-specific settings \
│   ├── package.json               # NPM package manifest \
│   ├── tailwind.config.js         # Tailwind CSS config \
│   ├── postcss.config.js          # PostCSS plugins \
│   ├── vite.config.js             # Vite build config \
│   └── README.md                  # Project documentation \
├── [Supporting Files]             # Auxiliary project files \
│   ├── .env                       # Local environment variables \
│   ├── .gitignore                 # Version control exclusions \
│   ├── yarn.lock                  # Yarn dependency tree \
│   ├── registry.js                # Plugin registry API \
│   └── marketplace.js             # Plugin discovery system


```

# 📁 Project Structure Guide

## Directory & File Overview

| Location | File/Folder | Purpose |
|----------|------------|---------|
| **public/** | `index.html` | Main HTML entry point |
|  | `styles/main.css` | Global CSS (processed by Tailwind) |
|  | `main.js` | Development entry point |
|  | `logo.svg` | Application logo |
|  | `github-icon.svg` | GitHub navigation icon |
|  | `dashboard.html` | Performance monitoring page |
| **src/** | `components/` | Reusable React components |
|  | ↳ `Navbar.jsx` | Top navigation component |
|  | ↳ `Sidebar.jsx` | Side navigation component |
|  | ↳ `Footer.jsx` | Page footer component |
|  | `pages/` | Application page components |
|  | ↳ `Home.jsx` | Landing page |
|  | ↳ `GettingStarted.jsx` | Documentation page |
|  | ↳ `Features.jsx` | Features showcase |
|  | ↳ `Plugins.jsx` | Plugins documentation |
|  | ↳ `ApiReference.jsx` | API documentation |
|  | ↳ `Examples.jsx` | Code examples |
|  | ↳ `Blog.jsx` | Blog posts |
|  | ↳ `Changelog.jsx` | Version history |
|  | ↳ `News.jsx` | Project announcements |
|  | `router/` | Routing configuration |
|  | ↳ `index.js` | Route definitions |
|  | `styles/` | Global styles |
|  | ↳ `main.css` | Tailwind CSS file |
|  | `App.jsx` | Root application component |
|  | `main.jsx` | React entry point |
| **plugins/** | `css.js` | CSS processing plugin |
|  | `typescript.js` | TypeScript support |
|  | `react.js` | React JSX transformer |
|  | `vue.js` | Vue single-file components |
| **dist/** | `bundle.js` | Production JavaScript bundle |
|  | `main.css` | Optimized CSS output |
|  | `assets/` | Static production assets |
|  | ↳ `logo.svg` | Optimized logo |
|  | ↳ `github-icon.svg` | Optimized GitHub icon |
|  | `images/` | Optimized image assets |
| **Root Files** | `server.js` | Development server script |
|  | `build.js` | Production build script |
|  | `banana.config.js` | BananaJS configuration |
|  | `package.json` | Project manifest |
|  | `tailwind.config.js` | Tailwind configuration |
|  | `postcss.config.js` | PostCSS plugins |
|  | `README.md` | Project documentation |

## Key Directories

1. **public/**  
   - Contains static assets served directly
   - Files copied as-is during build

2. **src/**  
   - Main application source code
   - Follows component-based architecture

3. **plugins/**  
   - Custom build processors
   - Extend core functionality

4. **dist/**  
   - Generated production assets
   - Never edit manually (auto-generated)

> 💡 Pro Tip: Use `banana analyze` to visualize your project structure!




### Basic React Project Template for BananaJS

```bash

banana-react-template/\
├── public/\
│   ├── index.html\
│   ├── favicon.ico\
│   └── manifest.json\
├── src/\
│   ├── components/\
│   │   ├── Navbar.jsx\
│   │   ├── Footer.jsx\
│   ├── pages/\
│   │   ├── Home.jsx\
│   │   ├── About.jsx\
│   ├── App.jsx\
│   ├── main.jsx\
│   ├── styles/\
│   │   ├── main.css\
├── .gitignore\
├── package.json\
├── README.md\
├── banana.config.js\
└── tailwind.config.js\

```