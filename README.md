# Getting Started with Create React App

1. Make a git repository (or clone an empty repository from a remote).

    ```sh
    mkdir -p ~/git/react-app
    cd ~/git/react-app
    git init
    ```

1. Install Yarn.

    ```sh
    npm install --global yarn
    ```

1. Create a React app.

    ```sh
    yarn create react-app .
    ```

1. Configure ESLint.

    ```sh
    $ yarn create @eslint/config
    yarn create v1.22.17
    [1/4] Resolving packages...
    [2/4] Fetching packages...
    [3/4] Linking dependencies...
    [4/4] Building fresh packages...
    success Installed "@eslint/create-config@0.1.2" with binaries:
        - create-config
    ```

    1. Choose a usage option.

        ```text
        ? How would you like to use ESLint? … 
          To check syntax only
          To check syntax and find problems
        ▸ To check syntax, find problems, and enforce code style
        ```

    1. Choose a module type.

        ```text
        ? What type of modules does your project use? … 
        ▸ JavaScript modules (import/export)
          CommonJS (require/exports)
          None of these
        ```

    1. Choose a framework.

       ```text
       ? Which framework does your project use? … 
       ▸ React
         Vue.js
         None of these
       ```

    1. Choose a TypeScript option.

       ```text
       ? Does your project use TypeScript? ‣ No / Yes
       ```

    1. Choose where the code will run.

        ```text
        ? Where does your code run? …  (Press <space> to select, <a> to toggle all, <i> to invert selection)
        ✔ Browser
          Node
        ```

    1. Choose how to define a style.

        ```text
        ? How would you like to define a style for your project? … 
        ▸ Use a popular style guide
          Answer questions about your style
        ```

    1. Choose a style guide.

        ```text
        ? Which style guide do you want to follow? … 
          Airbnb: https://github.com/airbnb/javascript
          Standard: https://github.com/standard/standard
        ▸ Google: https://github.com/google/eslint-config-google
          XO: https://github.com/xojs/eslint-config-xo
        ```

    1. Choose a config file format.

        ```text
        ? What format do you want your config file to be in? … 
          JavaScript
          YAML
        ▸ JSON
        ```

    1. Choose to install dependencies now.

        ```text
        ? Would you like to install them now with npm? ‣ No / Yes
        ```

1. Move any ESLint configuration from `package.json` to `.eslintrc.json` and add recommended extensions.

    * Delete `eslintConfig` from `package.json`.

        ```json
        "eslintConfig": {
            "extends": [
            "react-app",
            "react-app/jest"
            ]
        },
        ```

    * Add extensions to `.eslintrc.json`.

        ```json
        "extends": [
            "eslint:recommended",
            "plugin:react/recommended",
            "google",
            "react-app",
            "react-app/jest"
        ],
        ```

1. Add a `lint` script to `package.json`.

    ```json
    "scripts": {
        "start": "react-scripts start",
        "build": "react-scripts build",
        "test": "react-scripts test",
        "lint": "eslint src",
        "eject": "react-scripts eject"
    },
    ```

1. Delete `package-lock.json`, which is not required by Yarn.

    ```sh
    rm package-lock.json
    ```

1. Commit and push.
