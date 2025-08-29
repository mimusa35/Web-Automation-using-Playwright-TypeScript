# Playwright_TypeScript_Automation
A Playwright project for automating web application testing using TyoeScript. This repository includes setup instructions, example test scripts, and commands for executing automated browser-based tests efficiently. Automation testing can save time and is best for running headless browser tests (Firefox, Chrome), producing results faster.

# Project Overview
This repository demonstrates how to use Playwright with TyoeScript for testing web applications. It provides a step-by-step guide to installation, setup, writing tests, using the Playwright test generator (CodeGen), and executing tests.

# Prerequisites
1. **Node.js Environment**
   - Install Node.js: [Download Node.js](https://nodejs.org/en)
   - Verify installation:
     ```bash
     node -v
     npm -v
     ```
2. **VS Code Editor**
   - Install VS Code: [Download VS Code](https://code.visualstudio.com/download)
3. **Create Project Folder**
   - Create a folder on your local machine and open it in VS Code.

# Installation Process
1. Open the VS Code terminal and run the following command to initialize a Playwright project:
   ```bash
   npm init playwright@latest
   ```


# Folder Structure

```
project-folder/   
├── src/tests/e2e                     # Folder containing test files  
│   ├── example.spec.js               # example test script   
│   ├── login.spec.js                 # login script  
├── .gitignore                        # Ignored files and folders  
├── package-lock.json                 # Lockfile for dependency management  
├── package.json                      # Node project management file  
├── playwright.config.js              # Playwright configuration file  
└── Readme.md                         # Project documentation
```

# Running Tests
Use the following commands to execute your tests:
1. Run all tests on all browsers in headless mode:
   ```bash
   npx playwright test
   ```
2. Run a specific test file:
   ```bash
   npx playwright test HomePage.spec.js
   ```
3. Run a specific test file on Chromium browser in headed mode:
   ```bash
   npx playwright test login.spec.js --project=chromium --headed
   ```
4. Debug tests:
   ```bash
   npx playwright test --debug
   ```
5. Generate an HTML report:
   ```bash
   npx playwright show-report
   ```

# Writing Tests with CodeGen (Test Generator)
The Playwright test generator helps record and generate tests automatically. You can use the following methods to generate and save your test scripts:
1. Run the following command to launch the Playwright Inspector and browser for recording:
   ```bash
   npx playwright codegen 
   ```
2. Save to a specific test file:
   ```bash
   npx playwright codegen --output tests/CodeGen.spec.js  
   ```
3. Generate tests targeting JavaScript:
   ```bash
   npx playwright codegen --target=javascript    
   ```
4. Open the browser in a specific mode, like Chromium:
   ```bash
   npx playwright codegen --browser=chromium      
   ```
5. Emulate a device during test generation, e.g., iPhone 13:
   ```bash
   npx playwright codegen --device="iPhone 13"      
   ```
6. Customize viewport size for recording:
   ```bash
   npx playwright codegen --viewport-size="1280,720"        
   ```

# Resources
- [Playwright Official Documentation](https://playwright.dev/)
- [Node.js Official Website](https://nodejs.org/en)
- [VS Code Official Website](https://code.visualstudio.com/)