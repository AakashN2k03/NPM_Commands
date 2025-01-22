# Complete List of Commands: NPM and NVM

## Documentation Links
- NPM Documentation: https://docs.npmjs.com/
- NVM GitHub Repository: https://github.com/nvm-sh/nvm

## NPM Commands

1. **Install dependencies**
   ```bash
   npm install
   ```
   Installs all dependencies listed in `package.json`.

2. **Install a specific package**
   ```bash
   npm install <package-name>
   ```
   Installs the specified package (e.g., `npm install express`).

3. **Install a package globally**
   ```bash
   npm install -g <package-name>
   ```
   Installs the package globally (e.g., `npm install -g nodemon`).

4. **Uninstall a package**
   ```bash
   npm uninstall <package-name>
   ```
   Removes the specified package from the project.

5. **Update all packages**
   ```bash
   npm update
   ```
   Updates all project dependencies.

6. **Check outdated packages**
   ```bash
   npm outdated
   ```
   Shows a list of packages that need to be updated.

7. **Show installed version of a package**
   ```bash
   npm list <package-name>
   ```
   Displays the installed version of the specified package.

8. **View a package's details**
   ```bash
   npm view <package-name>
   ```
   Shows details like version and description of a package.

9. **Check the npm version**
   ```bash
   npm -v
   ```
   Displays the installed version of npm.

10. **Check Node.js version**
    ```bash
    node -v
    ```
    Displays the installed version of Node.js.

11. **Run a script**
    ```bash
    npm run <script-name>
    ```
    Runs a custom script defined in `package.json`.

12. **Install dev dependencies**
    ```bash
    npm install <package-name> --save-dev
    ```
    Installs a package as a development dependency.

13. **Initialize a new project**
    ```bash
    npm init
    ```
    Creates a new `package.json` file interactively.

14. **Initialize a project with defaults**
    ```bash
    npm init -y
    ```
    Creates a `package.json` file with default values.

15. **Increment version in package.json**
    ```bash
    npm version <patch|minor|major>
    ```
    Updates the version in `package.json`:
    * `patch`: `1.0.0` → `1.0.1`
    * `minor`: `1.0.0` → `1.1.0`
    * `major`: `1.0.0` → `2.0.0`

16. **Clear npm cache**
    ```bash
    npm cache clean --force
    ```
    Clears the npm cache.

17. **Audit vulnerabilities**
    ```bash
    npm audit
    ```
    Scans for security vulnerabilities in dependencies.

18. **Fix vulnerabilities**
    ```bash
    npm audit fix
    ```
    Automatically fixes vulnerabilities.

19. **Show globally installed packages**
    ```bash
    npm list -g --depth=0
    ```
    Lists globally installed packages.

## NVM Commands

1. **Install nvm**
   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
   ```
   Installs Node Version Manager (NVM).

2. **Check installed Node.js versions**
   ```bash
   nvm list
   ```
   Lists all installed Node.js versions.

3. **Install a specific Node.js version**
   ```bash
   nvm install <version>
   ```
   Installs the specified Node.js version (e.g., `nvm install 18.14.2`).

4. **Use a specific Node.js version**
   ```bash
   nvm use <version>
   ```
   Switches to the specified version (e.g., `nvm use 16`).

5. **Set default Node.js version**
   ```bash
   nvm alias default <version>
   ```
   Sets the specified version as the default (e.g., `nvm alias default 18`).

6. **Uninstall a Node.js version**
   ```bash
   nvm uninstall <version>
   ```
   Removes the specified Node.js version.

7. **Show current Node.js version**
   ```bash
   nvm current
   ```
   Displays the currently active Node.js version.

8. **List available Node.js versions**
   ```bash
   nvm ls-remote
   ```
   Shows all available Node.js versions for installation.
