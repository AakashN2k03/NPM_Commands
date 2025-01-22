# NPM and NVM Commands Guide

A comprehensive reference guide for NPM (Node Package Manager) and NVM (Node Version Manager) commands with examples and expected outputs.

## Table of Contents
- [NPM Commands](#npm-commands)
- [NVM Commands](#nvm-commands)
- [Official Documentation](#official-documentation)

## NPM Commands

### Package Management

#### Installation
1. Install all dependencies
```bash
npm install
```
```
added 1270 packages, and audited 1271 packages in 30s
found 0 vulnerabilities
```

2. Install specific package
```bash
npm install express
```
```
+ express@4.18.2
added 57 packages, and audited 58 packages in 3s
found 0 vulnerabilities
```

3. Install package globally
```bash
npm install -g nodemon
```
```
+ nodemon@3.0.3
added 118 packages in 4s
```

4. Install development dependency
```bash
npm install --save-dev jest
```
```
+ jest@29.7.0
added 316 packages, and audited 317 packages in 12s
found 0 vulnerabilities
```

#### Uninstallation & Updates
1. Uninstall package
```bash
npm uninstall express
```
```
removed 57 packages, and audited 1214 packages in 3s
found 0 vulnerabilities
```

2. Update packages
```bash
npm update
```
```
changed 10 packages, and audited 1271 packages in 5s
found 0 vulnerabilities
```

3. Check outdated packages
```bash
npm outdated
```
```
Package     Current  Wanted  Latest  Location
express     4.17.1   4.17.3  4.18.2  project
nodemon     2.0.15   2.0.22  3.0.3   project
```

#### Package Information
1. List package version
```bash
npm list express
```
```
project@1.0.0
└── express@4.18.2
```

2. View package details
```bash
npm view express
```
```
express@4.18.2 | MIT | deps: 30 | versions: 262
Fast, unopinionated, minimalist web framework for node.
...
```

3. List global packages
```bash
npm list -g --depth=0
```
```
/usr/local/lib
├── npm@9.8.1
├── nodemon@3.0.3
└── create-react-app@5.0.1
```

### Project Management

#### Initialization
1. Create new project
```bash
npm init
```
```
package name: (project)
version: (1.0.0)
description:
entry point: (index.js)
...
```

2. Create project with defaults
```bash
npm init -y
```
```
Wrote to /path/to/project/package.json:
{
  "name": "project",
  "version": "1.0.0",
  ...
}
```

#### Version Management
```bash
npm version minor
```
```
v1.1.0
```

#### Security
1. Audit dependencies
```bash
npm audit
```
```
found 0 vulnerabilities in 1271 packages
```

2. Fix vulnerabilities
```bash
npm audit fix
```
```
fixed 0 of 0 vulnerabilities in 1271 packages
```

## NVM Commands

### Installation
For macOS/Linux:
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

For Windows, download the nvm-setup.zip from:
https://github.com/coreybutler/nvm-windows/releases

### Version Management
1. List installed versions
```bash
nvm list
```
```
->     v18.19.0
       v16.20.2
       v14.21.3
```

2. Install specific version
```bash
nvm install 18.19.0
```
```
Downloading and installing node v18.19.0...
Now using node v18.19.0 (npm v10.2.3)
```

3. Switch version
```bash
nvm use 16.20.2
```
```
Now using node v16.20.2 (npm v8.19.4)
```

4. Set default version
```bash
nvm alias default 18.19.0
```
```
default -> 18.19.0 (-> v18.19.0)
```

5. Show current version
```bash
nvm current
```
```
v18.19.0
```

6. List available versions
```bash
nvm ls-remote
```
```
...
       v18.19.0
       v19.9.0
       v20.10.0
...
```

## Official Documentation

### NPM Documentation
- Main documentation: https://docs.npmjs.com/
- CLI Commands: https://docs.npmjs.com/cli/v10/commands
- Package.json guide: https://docs.npmjs.com/cli/v10/configuring-npm/package-json
- Dependency management: https://docs.npmjs.com/about-packages-and-modules

### NVM Documentation
- GitHub Repository: https://github.com/nvm-sh/nvm
- Installation guide: https://github.com/nvm-sh/nvm#installing-and-updating
- Usage documentation: https://github.com/nvm-sh/nvm#usage
- Windows version: https://github.com/coreybutler/nvm-windows

## Common Issues and Troubleshooting

### NPM
1. Permission errors:
```bash
npm cache clean --force
```
```
npm WARN using --force Recommended protections disabled.
```

2. Module not found:
```bash
npm install
rm -rf node_modules
npm cache clean --force
```

### NVM
1. Command not found after installation:
```bash
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

2. Version switching issues:
```bash
nvm uninstall <version>
nvm install <version>
```

## Best Practices
1. Always specify exact versions in `package.json`
2. Use `--save-exact` when installing new packages
3. Regularly update dependencies and check for vulnerabilities
4. Keep Node.js versions consistent across development team using `.nvmrc` file

## Project Setup Example
```bash
# Initialize new project
npm init -y

# Install production dependencies
npm install express mongoose dotenv

# Install development dependencies
npm install --save-dev nodemon jest

# Create .nvmrc file
node -v > .nvmrc

# Install specific Node.js version
nvm install $(cat .nvmrc)
```

---
Last updated: January 2024
