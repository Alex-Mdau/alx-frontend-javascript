ES6 Basics

This Directory  contains a collection of exercises and tasks related to ES6 (ECMAScript 2015), also known as ES6 Basics. These exercises cover various concepts and features introduced in ES6 and are designed to help you understand and practice modern JavaScript programming.
Concepts

In this project, we will cover the following concepts:

    Modern JavaScript
    Software Linter

Learning Objectives

By the end of this project, you should be able to explain the following without the help of Google:

    What ES6 is
    New features introduced in ES6
    The difference between a constant and a variable
    Block-scoped variables
    Arrow functions and function parameters default to them
    Rest and spread function parameters
    String templating in ES6
    Object creation and their properties in ES6
    Iterators and for-of loops

Requirements
General

    All your files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
    Allowed editors: vi, vim, emacs, Visual Studio Code
    All your files should end with a new line
    A README.md file, at the root of the project folder, is mandatory
    Your code should use the .js extension
    Your code will be tested using the Jest Testing Framework
    Your code will be analyzed using the linter ESLint along with specific rules that we’ll provide
    All of your functions must be exported

Setup

Follow the instructions below to set up your environment for this project:

    Install NodeJS 12.11.x:

bash

curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y

    Check NodeJS and npm versions:

bash

nodejs -v
npm -v

You should see output similar to the following:

v12.11.1
6.11.3

    Install Jest, Babel, and ESLint in your project directory:

bash

cd /path/to/project/directory
npm install --save-dev jest
npm install --save-dev babel-jest @babel/core @babel/preset-env
npm install --save-dev eslint

    Configure the following files:

    package.json
    babel.config.js
    .eslintrc.js

Refer to the provided files in the repository for the configuration details.

    Run npm install from the terminal of your project folder to install all necessary project dependencies.

Tasks

The project includes several tasks to complete. Each task is located in a separate file and covers a specific concept or feature of ES6. The tasks are as follows:

    Const or let?
    Block Scope
    Arrow Functions
    Parameter Defaults
    Rest Parameter Syntax for Functions
    The Wonders of Spread Syntax
    Take Advantage of Template Literals
    Object Property Value Shorthand Syntax
    No Need to Create Empty Objects Before Adding in Properties
    For...of Loops

Each task file contains the task description and a code template. Your goal is to modify or complete the code to meet the requirements specified in the task description.

Please refer to the individual task files for more details and execution examples.
Repository

    GitHub repository: alx-frontend-javascript
    Directory: 0x00-ES6_basic

Feel free to explore the repository for more information and access to the task files.
