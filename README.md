# NPM and NVM Commands Reference Guide

A comprehensive guide for NPM (Node Package Manager) and NVM (Node Version Manager) commands with examples and outputs.

## Table of Contents
- [NPM Commands](#npm-commands)
- [NVM Commands](#nvm-commands)

## NPM Commands

### Package Management

#### Installation

**Text Example**: Install all dependencies listed in your package.json file
```bash
npm install
```
**Output**:
```
added 1270 packages, and audited 1271 packages in 30s
found 0 vulnerabilities
```

**Text Example**: Install Express.js for your web application
```bash
npm install express
```
**Output**:
```
+ express@4.18.2
added 57 packages, and audited 58 packages in 3s
found 0 vulnerabilities
```

**Text Example**: Install Nodemon globally for automatic server restarting
```bash
npm install -g nodemon
```
**Output**:
```
+ nodemon@3.0.3
added 118 packages in 4s
```

**Text Example**: Install Jest for testing in development environment
```bash
npm install --save-dev jest
```
**Output**:
```
+ jest@29.7.0
added 316 packages, and audited 317 packages in 12s
found 0 vulnerabilities
```

### Uninstallation & Updates

**Text Example**: Remove Express.js from your project
```bash
npm uninstall express
```
**Output**:
```
removed 57 packages, and audited 1214 packages in 3s
found 0 vulnerabilities
```

**Text Example**: Update all packages to their latest versions
```bash
npm update
```
**Output**:
```
changed 10 packages, and audited 1271 packages in 5s
found 0 vulnerabilities
```

**Text Example**: Check which packages need updating
```bash
npm outdated
```
**Output**:
```
Package     Current  Wanted  Latest  Location
express     4.17.1   4.17.3  4.18.2  project
nodemon     2.0.15   2.0.22  3.0.3   project
```

### Package Information

**Text Example**: Check the installed version of Express
```bash
npm list express
```
**Output**:
```
project@1.0.0
└── express@4.18.2
```

**Text Example**: View detailed information about Express package
```bash
npm view express
```
**Output**:
```
express@4.18.2 | MIT | deps: 30 | versions: 262
Fast, unopinionated, minimalist web framework for node.
...
```

**Text Example**: List all globally installed packages
```bash
npm list -g --depth=0
```
**Output**:
```
/usr/local/lib
├── npm@9.8.1
├── nodemon@3.0.3
└── create-react-app@5.0.1
```

### Project Management

**Text Example**: Initialize a new Node.js project interactively
```bash
npm init
```
**Output**:
```
package name: (project)
version: (1.0.0)
description:
entry point: (index.js)
...
```

**Text Example**: Initialize a project with default values
```bash
npm init -y
```
**Output**:
```
Wrote to /path/to/project/package.json:
{
  "name": "project",
  "version": "1.0.0",
  ...
}
```

**Text Example**: Increment the minor version of your package
```bash
npm version minor
```
**Output**:
```
v1.1.0
```

### Security

**Text Example**: Check for known vulnerabilities in dependencies
```bash
npm audit
```
**Output**:
```
found 0 vulnerabilities in 1271 packages
```

**Text Example**: Automatically fix vulnerabilities
```bash
npm audit fix
```
**Output**:
```
fixed 0 of 0 vulnerabilities in 1271 packages
```

## NVM Commands

### Installation
**Text Example**: Install NVM on macOS/Linux
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

### Version Management

**Text Example**: See all installed Node.js versions
```bash
nvm list
```
**Output**:
```
->     v18.19.0
       v16.20.2
       v14.21.3
```

**Text Example**: Install Node.js version 18.19.0
```bash
nvm install 18.19.0
```
**Output**:
```
Downloading and installing node v18.19.0...
Now using node v18.19.0 (npm v10.2.3)
```

**Text Example**: Switch to Node.js version 16.20.2
```bash
nvm use 16.20.2
```
**Output**:
```
Now using node v16.20.2 (npm v8.19.4)
```

**Text Example**: Set Node.js 18.19.0 as the default version
```bash
nvm alias default 18.19.0
```
**Output**:
```
default -> 18.19.0 (-> v18.19.0)
```

**Text Example**: Check currently active Node.js version
```bash
nvm current
```
**Output**:
```
v18.19.0
```

**Text Example**: View available Node.js versions for installation
```bash
nvm ls-remote
```
**Output**:
```
...
       v18.19.0
       v19.9.0
       v20.10.0
...
```

## Common Issues and Troubleshooting

**Text Example**: Clear NPM cache to resolve dependency issues
```bash
npm cache clean --force
```
**Output**:
```
npm WARN using --force Recommended protections disabled.
```

**Text Example**: Reload NVM in current terminal
```bash
source ~/.nvm/nvm.sh
```
**Output**:
```
nvm > Successfully reloaded
```
