# Developer Configuration Checklist

This repository contains configuration files and tools for kickstarting developer projects, including Vite, ESLint, Prettier, and TypeScript.

## Steps to Start a Vite Project

### 1. Initial Setup
- [ ] Control the version of Node.js and update if needed:
```bash
node -v
```  
- [ ] Initialize a new Vite project:
```bash
npm create vite@latest .
```

- [ ]  Navigate to the project folder:
```bash
cd <project-name>
```

- [ ]  Install dependencies:
```bash
npm install
```
### 2. Add Sass Support
- [ ] Install Sass:
```bash
npm install sass --save-dev
```

- [ ] Update your SCSS files and organize them (example below):
 - Create a src/scss folder.
 - Add an src/scss/main.scss file for your global styles.

- [ ] Import SCSS in your project (e.g., in main.ts or main.js)

### 3. Add TypeScript Support
- [ ]  Add TypeScript support:
```bash
npm install --save-dev typescript @types/node
```

- [ ] Initialize TypeScript configuration:
```bash
npx tsc --init
```

- [ ] Update the tsconfig.json file.

### 4. Configure ESLint and Prettier

- [ ] Add ESLint for code linting:
```bash
npm install eslint --save-dev
npx eslint --init
```

- [ ]  Add Prettier for code formatting:
```bash
npm install prettier eslint-config-prettier eslint-plugin-prettier --save-dev
```

- [ ] Configure .eslintrc and .prettierrc
