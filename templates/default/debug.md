# Debug error assistant.

BananaJS Debugging Guide
BananaJS provides robust debugging tools to help identify and resolve issues throughout your development workflow.


# Core Debugging Features
1. Built-in Debug Mode
bash
banana dev --debug
Enables:

Extended error stack traces

Dependency resolution logging

Build process instrumentation

Real-time build metrics

2. Debug Output Levels
Control verbosity with log levels:

bash
banana build --log-level=verbose
# Levels: silent | error | warn | info | verbose | debug
3. Component Debugging
Mark components for debugging:


```bash
jsx
// React/Vue components
<MyComponent banana-debug="props,state"/>
Outputs:
Prop changes
State updates
Lifecycle events
Render timing
Debugging Tools
1. Error Visualization
Error Overlay Example

In-browser error overlays

Click-to-source functionality

Suggested fixes for common issues
```


2. Performance Profiling
```bash
banana profile build
Generates:

Build timeline waterfall chart

Plugin execution times

Bundle composition analysis
```


3. Dependency Debugging

```bash
banana debug:deps
Outputs:
Dependency tree visualization
Version conflict detection
Circular dependency warnings
Debug Configuration
```



```bash
Add to banana.config.js:

javascript
export default {
  debug: {
    components: true,  // Component debugging
    build: false,      // Build process logging
    runtime: 'errors'  // 'all' | 'errors' | 'warnings'
  }
}
```

Browser DevTools Integration
Install BananaJS DevTools extension

# Access panels for:
Banana-specific component inspection
State management debugging
Build artifact exploration
Common Debug Scenarios

1. CSS Debugging
```bash
banana inspect:css
Generates:
CSS source mapping
Specificity graphs
Unused rule detection
```

2. Build Failures

```bash
banana build --debug-cache
Cache integrity checking

Step-by-step build replay

Isolated module rebuilding
```
3. Runtime Errors

```bash
javascript
// Enable error tracking
window.__BANANA_DEBUG__ = {
  captureErrors: true,
  logLimit: 50
}
```