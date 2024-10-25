# Tire Service Inventory Front-End

## Development Environment

### Prerequisites

- **nvm (Node Version Manager)**: 1.1.12
  - **Note**: Used to manage Node.js versions.
- **Node.js**: v18.20.4
  - **Note**: It's not working on 20.x LTS node versions. 18.x LTS version required.
- **Yarn**: 1.22.22
  - **Note**: Preferred package manager for this project.
- **npm**: 10.9.0
  - **Note**: While Yarn is preferred, npm can also be used starting from this version.

### Project Setup

This project was created using:

```bash
npx create-next-app-ts tire-service-inventory-fe
```

### Installing Dependencies

```bash
yarn install
```

### Starting the Development Server

```bash
yarn dev
```

The app will be available at [http://localhost:3000](http://localhost:3000).

### Building for Production

```bash
yarn build
```

### Exporting Static Files

```bash
yarn export
```

### Linting

- **Check for Lint Errors**

  ```bash
  yarn lint
  ```

- **Fix Lint Errors**

  ```bash
  yarn lint:fix
  ```

---

## VS Code Configuration

### Included `.vscode` Folder

The project includes a `.vscode` folder with the following files:

#### 1. `extensions.json`

```json
{
  "recommendations": [
	"arcanis.vscode-zipfs",
	"dbaeumer.vscode-eslint",
	"esbenp.prettier-vscode"
  ]
}
```

**Purpose**:

- Recommends installing VS Code extensions that are essential for development in this project.

**Recommended Extensions**:

- **Yarn VSCode Extension** (`arcanis.vscode-zipfs`): Improves support for Yarn Plug'n'Play.
- **ESLint** (`dbaeumer.vscode-eslint`): Integrates ESLint into VS Code for real-time linting.
- **Prettier** (`esbenp.prettier-vscode`): Integrates Prettier for consistent code formatting.

#### 2. `settings.json`

```json
{
  "search.exclude": {
	"**/.yarn": true,
	"**/.pnp.*": true
  },
  "eslint.nodePath": ".yarn/sdks",
  "typescript.tsdk": ".yarn/sdks/typescript/lib",
  "typescript.enablePromptUseWorkspaceTsdk": true,
  "prettier.prettierPath": ".yarn/sdks/prettier/index.js"
}
```

**Purpose**:

- Configures VS Code to use the project's local versions of TypeScript, ESLint, and Prettier provided by Yarn PnP.
- Excludes certain Yarn-related files from search results to reduce clutter.

### Usage Instructions

1. **Open the Project in VS Code**

   - When you open the project, VS Code will detect the recommended extensions.

2. **Install Recommended Extensions**

   - A prompt will appear suggesting the installation of the recommended extensions.
   - Click **"Install All"** to install them.

3. **Benefit from Consistent Tooling**

   - The settings ensure that VS Code uses the exact versions of TypeScript, ESLint, and Prettier specified in the project.
   - This helps maintain code consistency and reduces environment-specific issues.

### Recommendations

- **Use the Workspace Versions**

  - The settings point VS Code to use the versions of tools installed in the project via Yarn PnP.
  - This avoids conflicts with globally installed versions and ensures consistency.

- **Do Not Modify the `.vscode` Settings Unnecessarily**

  - If you need to make personal adjustments, consider doing so in your user settings rather than changing the project settings.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---