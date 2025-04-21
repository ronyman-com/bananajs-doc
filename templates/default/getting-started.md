🍌 Getting Started with BananaJS
Prerequisites
Before you begin, ensure your system has:

Node.js (v18.00 or higher)

bash
node --version
npm (v9.x or higher) or yarn (v1.22+) or bun (v1.0+)

Git (for version control)

💡 Need help installing? Visit our environment setup guide

Installation
Install the BananaJS CLI globally:

bash
npm install -g @ronyman/bananajs
Alternative package managers:

bash
yarn global add @ronyman/bananajs  # Using Yarn
bun install -g @ronyman/bananajs   # Using Bun
Verify installation:

bash
banana --version
Creating Your First Project
Choose from our curated templates:

```bash
banana create my-app --template react     # React + Vite
banana create my-app --template vue      # Vue 3 + Pinia
banana create my-docs --template docs    # Documentation site
banana create my-api --template firebase # Firebase backend
banana create my-lib --template empty    # Minimal setup
```

## 🏗️ Project Templates

### Template Comparison

| Template    | Includes                          | Best For                  |
|-------------|-----------------------------------|---------------------------|
| `react`     | Vite, React 18, TailwindCSS       | SPAs, Web Apps            |
| `vue`       | Vue 3, Vite, Pinia                | Rapid Prototyping         |
| `docs`      | Markdown, Search, Dark Mode       | Documentation             |
| `firebase`  | Auth, Firestore, Functions        | Fullstack Applications    |
| `empty`     | Barebones setup                   | Custom Configurations     |

## 📁 Project Structure

Your new BananaJS project follows this intuitive structure:

Key directories explained:
- `src/assets`: Store images, fonts, and other static media
- `src/components`: Contains reusable Vue/React components
- `src/pages`: Houses route-based page components
- `public`: Files that get copied directly to build output


```bash
my-app/
├── src/
│   ├── assets/       # Static assets (images, fonts)
│   ├── components/   # Reusable UI components
│   ├── pages/        # Application views/routes
│   └── main.js       # Application entry point
├── banana.config.js  # BananaJS configuration
├── package.json      # Project dependencies
└── README.md         # Project documentation

```

Launching Development
Navigate to your project:

bash
cd my-app
Install dependencies:

```bash
npm install
# or
yarn install
# or
bun install
Start the development server:
```

```bash
banana dev
Automatically opens browser at http://localhost:5000
```


Features hot module replacement (HMR)
Includes error overlays
Next Steps
Explore CLI commands
Configure your project
Add plugins
Deploy your app
Having trouble? Visit our troubleshooting guide or join our community.