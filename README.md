# Overview of Node.js

## Table of Contents

---

---

1. Installing Node

   - Visit the Node.js website <a href="https://nodejs.org/en/" target="_blank">here</a> and install the LTS or latest version of Node.

   ***

2. Initializing a project

   - Once node is installed you can the run the following

     `npm init`

   - This will initialize your current working directory with a package.json.

   - This will now allow you to install packages via the node package manager more information can be found in their documentation <a href="https://nodejs.org/en/" target="_blank">here</a>.

   - If you have issues with it saying `command not recognized` after this step make sure you close your terminal or editor out completely and then try again in a fresh terminal.

   ***

3. Installing an npm package
    - Now that your directory has been initialized you can now install npm packages the package I will demonstrate is called Inquirer and more info can be found <a href="https://www.npmjs.com/package/inquirer" target="_blank">here</a>.

    - To install the Inquirer package you can run the following

      ``` npm install inquirer``` 
    - this will grab inquirer from the depths of the internet and then install it in your package.json
    - Once the install is complete you will now be able to use the Inquirer package inside of any JS file in that directory.

    ---

4. Using require to implement packages
    - Now that we have a package installed it can now be used in your JS file but first you must bring it using the require module to use it.
    - To use require you will structure it like the following

      ```const variableName = require("packageName")```
    - In our case to use the inquirer package it will look something like this

      ```const inquirer = require("inquirer")```

    - Now you can reference the inquirer package using the variable created named inquirer. Here is an example of using an inquirer method.
```
    inquirer
  .prompt([
    /* Pass your questions in here */
  ])
  .then((answers) => {
    // Use user feedback for... whatever!!
  })
  .catch((error) => {
    if (error.isTtyError) {
      // Prompt couldn't be rendered in the current environment
    } else {
      // Something else went wrong
    }
  });
```