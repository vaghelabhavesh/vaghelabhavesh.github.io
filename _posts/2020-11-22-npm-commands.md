---
layout: post
comments: true
title: "Some useful npm commands"
categories: blog
author:
- Bhavesh Vaghela
meta: "Springfield"
---

### What is npm?
npm is a package manager for the JavaScript programming language. It is the default package manager for [Node.js](https://www.npmjs.com/). Recently I completed a learning path [Build JavaScript applications with Node.js](https://docs.microsoft.com/en-in/learn/paths/build-javascript-applications-nodejs/) and found some basic and useful npm commands which were very helpful to me, so I thought of sharing.

Here are some useful npm commands.

- To create a package.json in interactive mode, you can use the npm init command.

  **`npm init`**

 - To create a package.json in non interactive mode, use the npm init -y command.

	**`npm init -y`**

- To get full detailed list of all the commands, type npm --help.

  **`npm --help`**

- To install any package, you can use npm install command followed by package name.

  **`npm install <package name>`**

- To install a package for development only which wont be shipped with production build, try the npm install with save-dev parameter. It also adds an entry in devDependencies in package.json.

  **`npm install <package name> --save-dev`**

- To install a package for production, try with production parameter. It adds an entry in dependencies in package.json.

  **`npm install <package name> --production`**
 
- To install a package in global directory instead of project's node_modules directory, use the g parameter.

  **`npm install <package name> -g`**
  
- To take care of fetching the dependency and carrying out the command, and clean up so it is not saved (or do not take up space) in node_modules folder, try the following command.

  **`npx <name of package>`**

- To list all the packages that your project is depending on, try the npm list command. It uses dependencies section from package.json. Use depth=0 for first level dependencies and depth=1 for 2nd level dependencies and so on.

  **`npm list --depth=<depth>`**

- To uninstall a package you use the uninstall command. It will remove the package from the manifest file and also from the node_modules directory.

  **`npm uninstall <name of dependency>`**

- To remove all dependencies in the node_modules directory that are not listed as dependencies in the manifest file, you can try the prune command.

  **`npm prune`**

- To list all the outdated packages, use the outdated command

  **`npm outdated`**

- To list vulnerabilities by different severity levels, high, and low for all the packages used in your project, use audit command

  **`npm audit`**

- To fix the vulnerabilities found by audit, try the audit command with fix.

  **`npm audit fix`**

- To fix the vulnerabilities found by audit forcefully, try the force parameter.

  **`npm audit fix --force`**
 
- To install the latest version, use @latest with npm install command.

  **`npm install node-fetch@latest lodash@latest`** 

- The following instruction will update to the latest patch version. If you only want the patch version to update, you would specify like this ~1.0.0. What this instruction says is equal or great to in the same range. 

  **`~1.1.1 or 1.1.x`** 

- The following instruction will update only the minor version. 

  **`^1.1.1 or 1.x.1`** 
 
- The following instruction will update to the highest major version. 

  **`*1.1.1 or x.0.0`**
 
- The package-lock.json guarantees exact installs. 

- The following command starts debugger that comes bundled with Node.js. 

  **`node inspect myscript.js`**

### Wrap up
These were some basic and useful nom commands that can get you started with npm.

Happy Coding.
	
