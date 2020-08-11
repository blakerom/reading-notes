# Readings: Node Ecosystem, TDD, CI/CD

### Reading, Research, and Discussion

   1. Why would you want to run JavaScript code outside of a browser?
   A more secure way to build a server using Node.JS that can be manipulated behind the curtains.
   
   2. What is the difference between a module and a package?
   A module is a single file or library while a package is inclusive of many files that the modules can use.
   
   3. What does the node package manager do?
   Installs libraries and packages onto the computer for the modules to use.
   
   4. Provide code snippets showing 3 different ways to export a function from a node module
  
   ```js
   module.exports = aFunctionCall;
   ```
   ```js
   const aName = () => {};
   ```
   ```js
   module.exports = {function};
   ```
   
   
### Vocabulary Terms

#### Term                        #### Definition
- ecosystem                   The Node libraries and tools used to create Node.JS
- Node.js                     JavaScript Runtime Environment
- V8 Engine                   Google Chrome JavaScript runtime engine
- module                      Can be imported as needed for use of functions similar to JavaScript libraries
- package                     One or more modules or libraries
- node package manager (npm)  Package Manager for packages and modules
- server                      A program that takes and sends request responses to create a network
- environment                 The programs hardware and software surroundings
- interpreter                 Analyzes and determines the code for machine understanding
- compiler                    Transslates the code from one language to another


### Resources
https://www.w3schools.com/nodejs/default.asp
https://medium.com/techahoy/why-i-am-a-big-fan-of-node-js-ecosystem-e99319c7dfe0
https://docs.npmjs.com/
