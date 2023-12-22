**Setting Up Node.js App with ESBuild: A Step-by-Step Guide**

**1. Tool Overview:**

- ESBuild, a high-performance bundler, is explored for bundling Node.js apps, commonly known for frontend bundling with frameworks like Vite.

**2. Configuring Project:**

- Utilizes essential tools:
  - ESBuild for bundling.
  - Pnpm for package management.
  - Node.js for execution.
  - TypeScript for type safety.
  - ES Modules as the module system.
  - npm-run-all for running multiple scripts.

**3. Initial Setup:**

- Initializes an empty repository with `npm init -y` to create a package.json file.
- Sets `"type": "module"` in package.json to instruct Node.js to use ES Modules.
- Installs dependencies using pnpm: `pnpm add -D typescript esbuild @types/node npm-run-all`.
- Creates a tsconfig.json file with TypeScript configuration for ESBuild compatibility.
- Adds a .gitignore file to exclude node_modules and dist directories.

**4. Project Structure:**

- Creates a src folder for source code.
- Adds an index.ts file in src with a basic example: `console.log("Hello, world!");`

**5. Script Setup:**

- **lint script:** Configures a TypeScript lint script treating TypeScript as a linter for code correctness.
- **build script:** Sets up an ESBuild script to bundle the code for production in dist/index.js using ES Modules.
- **start script:** Defines a script to run the bundled code using Node.js.
- **dev script:** Creates a comprehensive development script to simultaneously watch for TypeScript errors, rerun the application, and rebundle it using npm-run-all.

**6. Development Workflow:**

- Initiates development workflow using `pnpm dev`, ensuring parallel execution of type checking, bundling, and code execution.

**7. Final Thoughts:**

- Concludes the guide, highlighting the achieved fully functional ESBuild/Node setup capable of handling diverse Node.js applications, from express servers to Lambdas.
