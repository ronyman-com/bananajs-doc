# BananaJS Configuration System
BananaJS uses a modular configuration system that works alongside your existing toolchain. The configuration files provide granular control over all aspects of your 


# project's behavior.

Core Configuration Files

```bash
1. banana.config.js - Main Configuration
javascript
/**
 * @type {import('bananajs').BananaConfig}
 */
export default {
  // Project metadata
  project: {
    name: 'my-app',
    version: '1.0.0',
    type: 'spa' // 'spa' | 'ssr' | 'pwa' | 'library'
  },
  // Build configuration
  build: {
    outDir: './dist',
    assetsDir: 'static',
    minify: true,
    sourcemap: true,
    
    // CSS processing options
    css: {
      tailwind: true,
      bananaCSS: true,
      purge: {
        content: ['./src/**/*.{html,js,jsx,ts,tsx}'],
        safelist: ['banana-*']
      }
    }
  },

  // Development server
  server: {
    port: 3000,
    open: true,
    hot: true
  },

  // Plugin system
  plugins: [
    '@banana/readme',
    '@banana/analytics'
  ],

  // Extends Vite configuration
  vite: {
    // Vite-specific overrides
  }
}
```


2. vite.config.js - Vite Integration

```bash

javascript
import { defineConfig } from 'vite'
import banana from 'bananajs/vite'

export default defineConfig({
  plugins: [banana()],
  
  // Vite-specific configurations
  optimizeDeps: {
    include: ['react', 'react-dom']
  },
  
  // Merge with banana.config.js
  ...(process.env.BANANA_CONFIG ? require('./banana.config.js').vite : {})
})
3. tailwind.config.js - TailwindCSS Customization
javascript
const bananaPreset = require('bananajs/presets/tailwind')

/** @type {import('tailwindcss').Config} */
module.exports = {
  presets: [bananaPreset],
  
  content: [
    './src/**/*.{html,js,jsx,ts,tsx}',
    './banana.config.js'
  ],
  
  theme: {
    extend: {
      colors: {
        banana: {
          primary: '#FFD700',
          secondary: '#4A4A4A'
        }
      }
    }
  },
  
  plugins: [
    require('@banana/tailwind-animations')
  ]
}

```
4. postcss.config.js - PostCSS Pipeline

```bash
javascript
module.exports = {
  plugins: {
    'tailwindcss/nesting': {},
    'tailwindcss': {},
    'banana-postcss': {
      themePath: './theme.config.js'
    },
    'autoprefixer': {},
    ...(process.env.NODE_ENV === 'production' ? {
      'cssnano': {
        preset: 'advanced'
      }
    } : {})
  }
}
```