# NPM and NVM Commands Guide

A comprehensive reference guide for NPM (Node Package Manager) and NVM (Node Version Manager) commands.

## Table of Contents
- [NPM Commands](#npm-commands)
- [NVM Commands](#nvm-commands)

## NPM Commands

### Package Management

#### Installation
- `npm install` - Installs all dependencies listed in `package.json`
- `npm install <package-name>` - Installs a specific package
- `npm install -g <package-name>` - Installs a package globally
- `npm install <package-name> --save-dev` - Installs a package as a development dependency

#### Uninstallation & Updates
- `npm uninstall <package-name>` - Removes the specified package
- `npm update` - Updates all project dependencies
- `npm outdated` - Shows packages that need updating

#### Package Information
- `npm list <package-name>` - Shows installed version of a package
- `npm view <package-name>` - Displays package details
- `npm list -g --depth=0` - Lists globally installed packages

### Project Management

#### Initialization
- `npm init` - Creates a new `package.json` file interactively
- `npm init -y` - Creates a `package.json` file with default values

#### Version Management
- `npm version <patch|minor|major>` - Updates version in `package.json`
  - `patch`: 1.0.0 → 1.0.1
  - `minor`: 1.0.0 → 1.1.0
  - `major`: 1.0.0 → 2.0.0

#### Scripts
- `npm run <script-name>` - Runs a custom script defined in `package.json`

### System Commands
- `npm -v` - Shows npm version
- `node -v` - Shows Node.js version
- `npm cache clean --force` - Clears npm cache

### Security
- `npm audit` - Scans for security vulnerabilities
- `npm audit fix` - Automatically fixes vulnerabilities

## NVM Commands

### Installation
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

### Version Management
- `nvm list` - Shows all installed Node.js versions
- `nvm install <version>` - Installs specified Node.js version
- `nvm use <version>` - Switches to specified version
- `nvm alias default <version>` - Sets default Node.js version
- `nvm uninstall <version>` - Removes specified Node.js version
- `nvm current` - Shows active Node.js version
- `nvm ls-remote` - Lists available Node.js versions for installation

## Examples

```bash
# Install Express package
npm install express

# Install Nodemon globally
npm install -g nodemon

# Switch to Node.js version 18
nvm use 18

# Set Node.js 18 as default
nvm alias default 18
```

## Notes
- Always check `package.json` for project-specific scripts and dependencies
- Use `npm audit` regularly to check for security vulnerabilities
- Consider using `--save-dev` for development-only dependencies

---
*For more detailed information, visit the official [NPM Documentation](https://docs.npmjs.com/) and [NVM GitHub Repository](https://github.com/nvm-sh/nvm).*
