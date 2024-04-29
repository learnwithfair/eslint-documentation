# ESLint

Thanks for visiting my GitHub account!

<img src="https://images.credly.com/images/e6eebd0c-6a17-4c06-b172-02ca9f6beb06/eslint.png" height="200px" width = "180px"/> 
- A linter - tool for identifying and reporting programmatic, stylistic errors.
- ESLint does static error checking before running the program

### 2. Example of Popular Linters

- [JSLint](https://www.jslint.com/)
- [ESLint](https://eslint.org/)
- [JSHint](https://jshint.com/)

### 3. Prerequisities for setting up ESLint

- install Node.js
- install VSCode (as we will use VSCode)

## Required Software (Download)

- VS Code, Download ->https://code.visualstudio.com/download
- Node-js, Download-> https://nodejs.org/en/download

### 4. Installing & using ESLint

1. Create package.json: `npm init`
2. Install and configure eslint as dev dependency: `npm init @eslint/config`
3. Initialize eslint: `eslint --init` and follow steps:

   - How would you like to use ESLint? To check syntax and find problems
   - How would you like to use ESLint? None of these
   - How would you like to use ESLint? None of these
   - Does your project use TypeScript? › No
   - Where does your code run? Browser

4. Go to `.eslintrc.json` file and make add your necessary adjustments
   Example

   ```json

   following codes will activate the recommended rules which can be changed inside the rules object.
     {
      "extends": "eslint:recommended"
     }

    <!-- first value is error level, it can have 3 values: off/0, warn/1, error/2 -->
    Example of ESLint rules
    "rules": {
        "quotes": ["error", "double"]
    }

    More Examples of ESLint rules
   "rules": {
       "no-var": "error",
       "eqeqeq": "error",
       "no-unused-vars": "error",
       "default-case": "error",
       "no-console": "error",
       "camelcase": "error",
       "consistent-return": "error",
       "func-style": "error",
       "max-depth": ["error", 2],
       "max-lines": ["error", 25],
       "prefer-arrow-callback": "error",
       "prefer-const": "error",
       "no-useless-return": "error",
       "no-plusplus": "error",
       "quotes": ["error", "single"]
     }

   ```

5. add some codes in a js file for testing the eslint. I have created a file called app.js and added the following codes for testing purpose

   ```javascript
   var username = "anisul Islam";
   var password = "12345";
   var occupation = "full stack web developer";
   const user_presentaddress = "lala";

   var a = 6;
   a++;

   console.log(occupation);

   const validateUser = (pwd) => {
     if (password == pwd) {
       return true;
     }
   };

   console.log(validateUser(12345));

   switch (foo) {
     case 1:
       console.log(foo);
       break;

     case 2:
       console.log(foo);
       break;
   }

   const foo = true;
   if (foo) {
     if (foo) {
       if (foo) {
         console.log("hi");
       }
       console.log("hi");
     }
     console.log("hi");
   }

   setTimeout(function () {}, 1000);
   ```

6. make some changes in setting.json

   format on save and validate js codes: add the following codes in settings.json

   ```
    "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
    },
    "eslint.validate": ["javascript"]
   ```

7. Run the eslint: `eslint fileName.js` and check the erros
8. Fix automatically fixable errors: `eslint fileName.js --fix`

[Facebook](http://facebook.com/learnwithfair),  [Youtube](http://facebook.com/@learnwithfair),  [Instagram](http://instagram.com/learnwithfair) 