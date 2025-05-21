# BananaJS CLI Documentation
BananaJS is a powerful development toolkit that helps you scaffold, manage, and enhance your projects with simple commands. The CLI provides various utilities to accelerate your development workflow.

# Getting Started
First, check the available commands:

```bash
banana help
This displays all available commands with brief descriptions.

Application Scaffolding
Create new projects with different templates:
```

```bash
banana create-app MyFirstApp --template react     # Creates a React application
banana create-app MyFirstApp --template vue      # Creates a Vue.js application
banana create-app MyFirstApp --template docs     # Creates a documentation site
banana create-app MyFirstApp --template firebase # Creates a Firebase-powered app
banana create-app MyFirstApp --template readme   # Creates a project with a comprehensive README starter
```

## 🛠️ Template Options

| Template   | Configuration Details                                                                 | Includes                                                                 | Best For                          |
|------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------|
| `react`    | Modern React 18 + Vite setup                                                         | • Vite<br>• ESLint<br>• Prettier<br>• React Router<br>• Jest            | Single Page Applications          |
| `vue`      | Vue 3 with recommended defaults                                                      | • Vue 3<br>• Pinia<br>• Vite<br>• Vue Router<br>• Vitest                | Rapid UI Development              |
| `docs`     | Documentation site with Markdown support                                             | • Markdown<br>• Algolia Search<br>• Dark Mode<br>• Syntax Highlighting   | Technical Documentation           |
| `firebase` | Firebase-powered fullstack setup                                                     | • Authentication<br>• Firestore<br>• Functions<br>• Hosting Config      | Serverless Applications           |
| `readme`   | Professional documentation starter                                                   | • README template<br>• Contribution guidelines<br>• SEO optimization    | Open Source Projects              |

### Key Features by Template

**React Template** (`--template react`):
- Pre-configured with:
  - Vite for instant server start
  - ESLint + Prettier for code quality
  - TailwindCSS support
  - React Testing Library

**Vue Template** (`--template vue`):
- Batteries included:
  - Composition API
  - Pinia state management
  - SCSS support
  - Component auto-imports

**Docs Template** (`--template docs`):
- Documentation-ready:
  - Multi-page support
  - Responsive layout
  - Table of contents
  - Built-in search

**Firebase Template** (`--template firebase`):
- Production-ready:
  - Auth (Email/Google)
  - Firestore rules
  - Cloud Functions
  - Deployment configs

**Readme Template** (`--template readme`):
- Documentation essentials:
  - Badges section
  - Installation guide
  - Usage examples
  - License file


## ⚙️ Advanced CLI Options

### File Creation (`create-file`)
```bash
banana create-file Component.jsx        # Creates React component
banana create-file utils.ts            # Creates TypeScript file
banana create-file styles.module.css   # Creates CSS Module
banana create-folder src/components          # Creates a folder and necessary parent directories
banana create-upload -d ./public/uploads     # Opens a file dialog to upload files to specified destination
```

## Configuration
Configuration via banana.config.js for custom templates and presets

For more information about any command, use:


```bash
banana help
```