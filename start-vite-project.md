# Developer Configuration Checklist

This repository contains configuration files and tools for kickstarting developer projects, including Vite, ESLint, Prettier, and TypeScript.

## Steps to Start a Vite Project

### 1. Initial Setup

- [ ] **Check the version of Node.js and update if needed:**  
       Ensure your Node.js version is at least **14.18+** to support Vite.

  ```bash
  node -v
  ```

  If your version is outdated, download the latest stable version from nodejs.org.

- [ ] **Navigate to the project folder:**

  ```bash
  cd /path/to/your/project-folder
  ```

- [ ] **Initialize a new Vite project:**
  ```bash
  npm create vite@latest .
  ```
  During the setup, you will be prompted to:

* Name the project.
* Select a framework (e.g., React, Vue, or vanilla JavaScript).
* Choose between TypeScript and JavaScript.

- [ ] **Install dependencies:**

  ```bash
  npm install
  ```

- [ ] **add** vite.config.ts **for deployment (optional):**

  ```typescript
  import { defineConfig } from "vite";

  export default defineConfig({
    base: "/repo-name/",
  });
  ```

### 2. Add Sass Support

- [ ] **Install Sass:**

```bash
npm install sass --save-dev
```

- [ ] **Organize CSS/SCSS files:**
- Create a src/scss folder.
- Add an src/scss/main.scss file for your global styles.
- Add normlize/reset.

- [ ] **Install Normalize.css:**

```bash
npm install normalize.css
```

- [ ] **Import Normalize.css in Your SCSS File:**
      Open src/scss/main.scss and add the following:

```scss
@import "~normalize.css/normalize.css";
```

-[ ] **Import SCSS in Your Project:**
Import your main.scss file in your entry file (e.g., main.ts or main.js):

```typescript
import "./scss/main.scss";
```

### 3. Add TypeScript Support

If you chose TypeScript during Vite's setup, skip this step. Otherwise:

- [ ] **Add TypeScript support:**

  ```bash
  npm install --save-dev typescript @types/node
  ```

- [ ] **Initialize TypeScript configuration:**

  ```bash
  npx tsc --init
  ```

- [ ] **Update the tsconfig.json file.**

### 4. Configure ESLint and Prettier

- [ ] **Install ESLint for code linting:**

  ```bash
  npm install eslint --save-dev
  npx eslint --init
  ```

- [ ] **Install Prettier for code formatting:**

  ```bash
  npm install prettier eslint-config-prettier eslint-plugin-prettier --save-dev
  ```

- [ ] **Configure** .eslintrc **and** .prettierrc:
- Example .eslintrc:
  ```json
  {
    "extends": ["eslint:recommended", "plugin:prettier/recommended"],
    "env": {
      "browser": true,
      "node": true,
      "es2020": true
    }
  }
  ```
- Example .prettierrc:
  ```json
  {
    "singleQuote": true,
    "semi": false
  }
  ```
