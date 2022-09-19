# Node Ecosystem

<https://www.sitepoint.com/an-introduction-to-node-js>

**How would you describe Node to a non-technical friend?**

Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

**What does it mean that Node is a JavaScript runtime?**

 The creator of Node (Ryan Dahl) took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.

  It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.

**What is Node used for?**

Designed to automate the process of developing a modern JavaScript application.

## Introducing npm, the JavaScript Package Manager

npm -v  checks your Node package version.

## Installing a Package Locally

npm init -y

Next, use npm to install the lodash package and save it as a project dependency:

npm install lodash --save

### Installing a package globally

npm install -g jshint

You should now see a number of ES6-related errors. If you want to fix them up, add  jshint esversion: 6
to the top of the index.js file, re-run the command and linting should pass.

## A Comparison of JavaScript Linting Tools

<https://www.sitepoint.com/comparison-javascript-linting-tools/>

There are many linters available for JavaScript, but how do you choose which one to use? Let’s take a look at both the features and the pros and cons of four popular alternatives: 

**JSLint

Pros
Comes configured and ready to go (if you agree with the rules it enforces)

Cons
JSLint doesn’t have a configuration file, which can be problematic if you need to change the settings
Limited number of configuration options, many rules cannot be disabled
You can’t add custom rules
Undocumented features
Difficult to know which rule is causing which error.

**JSHint

Pros
Most settings can be configured
Supports a configuration file, making it easier to use in larger projects
Has support for many libraries out of the box, like jQuery, QUnit, NodeJS, Mocha, etc.
Basic ES6 support

Cons
Difficult to know which rule is causing an error
Has two types of option: enforcing and relaxing (which can be used to make JSHint stricter, or to suppress its warnings). This can make configuration slightly confusing
No custom rule support

**JSCS

Pros
Supports custom reporters, which can make it easier to integrate with other tools
Presets and ready-made configuration files can make it easy to set up if you follow one of the available coding styles
Has a flag to include rule names in reports, so it’s easy to figure out which rule is causing which error
Can be extended with custom plugins

Cons
Only detects coding style violations. JSCS doesn’t detect potential bugs such as unused variables, or accidental globals, etc.
Slowest of the four, but this is not a problem in typical use

**ESLint

Pros
Flexible: any rule can be toggled, and many rules have extra settings that can be tweaked
Very extensible and has many plugins available
Easy to understand output
Includes many rules not available in other linters, making ESLint more useful for detecting problems
Best ES6 support, and also the only tool to support JSX
Supports custom reporters

Cons
Some configuration required
Slow, but not a hindrance
