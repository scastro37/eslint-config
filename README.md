This module provides useful help for setting up ESLint rules in the project.

See official documentation [here](https://eslint.org).

## Compatibility

- npm v7 or higher.

## How to use it
To use the library you just need to follow the following steps:

- Install the library with npm
```js
npm i @scastro37/eslint-config
```
- Create the file config **.eslintrc.js** and import the library:
**For poject JS(JavaScript)**
```js
module.exports = { extends: ['@scastro37/eslint-config/configJS'] };
```
**For poject TS(TypeScript)**
```js
module.exports = { extends: ['@scastro37/eslint-config/configTS'] };
```
- And download [ESLint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) in vscode.

### Rules contained in this library [more information](https://eslint.org/docs/2.0.0/rules/).
**For poject JS(JavaScript).**
```js
const RULES = {
  OFF: "off",
  ERROR: "error",
  WARN: "warn",
};

module.exports = {
  env: {
    browser: true,
    commonjs: true,
    es6: true,
    node: true,
    jest: true,
  },
  extends: [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:jsx-a11y/recommended",
    "prettier"
  ],
  settings: {
    react: {
      version: "detect",
    },
  },
  parser: "babel-eslint",
  parserOptions: {
    ecmaVersion: 8,
    ecmaFeatures: {
      jsx: true,
      experimentalObjectRestSpread: true,
    },
    sourceType: "module",
  },

  globals: {
    MyGlobal: true,
  },
  rules: {
    "no-console": RULES.WARN,
    "no-template-curly-in-string": RULES.WARN,
    "no-alert": RULES.ERROR,
    "no-eq-null": RULES.ERROR,
    "no-eval": RULES.ERROR,
    "no-implied-eval": RULES.ERROR,
    "no-iterator": RULES.ERROR,
    "no-lone-blocks": RULES.ERROR,
    "no-loop-func": RULES.ERROR,
    "no-param-reassign": RULES.ERROR,
    "no-proto": RULES.ERROR,
    "no-return-assign": RULES.ERROR,
    "no-script-url": RULES.ERROR,
    "no-self-compare": RULES.ERROR,
    "no-unused-expressions": RULES.ERROR,
    "no-useless-concat": RULES.ERROR,
    "no-undefined": RULES.ERROR,
    curly: RULES.ERROR,
    eqeqeq: RULES.ERROR,
    "no-else-return": RULES.ERROR,
    "no-useless-return": RULES.ERROR,
    "no-duplicate-imports": RULES.ERROR,
    "no-var": RULES.ERROR,
    "prefer-const": RULES.ERROR,
    "prefer-spread": RULES.WARN,
    "prefer-template": RULES.ERROR,
    "no-await-in-loop": RULES.WARN,
    "no-unreachable-loop": RULES.WARN,
  },
};
```
**For poject TS(TypeScript).**
```js
const RULES = {
  OFF: "off",
  ERROR: "error",
  WARN: "warn",
};

module.exports = {
  env: {
    browser: true,
    commonjs: true,
    es6: true,
    node: true,
    jest: true,
  },
  extends: [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:jsx-a11y/recommended",
    "plugin:@typescript-eslint/eslint-recommended",
    "plugin:@typescript-eslint/recommended",
    "prettier",
  ],
  settings: {
    react: {
      version: "detect",
    },
  },
  parser: "@typescript-eslint/parser",
  parserOptions: {
    ecmaVersion: 8,
    ecmaFeatures: {
      jsx: true,
      experimentalObjectRestSpread: true,
    },
    sourceType: "module",
  },

  globals: {
    MyGlobal: true,
  },
  rules: {
    "no-console": RULES.WARN,
    "no-template-curly-in-string": RULES.WARN,
    "no-alert": RULES.ERROR,
    "no-eq-null": RULES.ERROR,
    "no-eval": RULES.ERROR,
    "no-implied-eval": RULES.ERROR,
    "no-iterator": RULES.ERROR,
    "no-lone-blocks": RULES.ERROR,
    "no-loop-func": RULES.ERROR,
    "no-param-reassign": RULES.ERROR,
    "no-proto": RULES.ERROR,
    "no-return-assign": RULES.ERROR,
    "no-script-url": RULES.ERROR,
    "no-self-compare": RULES.ERROR,
    "no-unused-expressions": RULES.ERROR,
    "no-useless-concat": RULES.ERROR,
    "no-undefined": RULES.ERROR,
    curly: RULES.ERROR,
    eqeqeq: RULES.ERROR,
    "no-else-return": RULES.ERROR,
    "no-useless-return": RULES.ERROR,
    "no-duplicate-imports": RULES.ERROR,
    "no-var": RULES.ERROR,
    "prefer-const": RULES.ERROR,
    "prefer-spread": RULES.WARN,
    "prefer-template": RULES.ERROR,
    "no-await-in-loop": RULES.WARN,
    "no-unreachable-loop": RULES.WARN
  },
};
```
## Contributors

The original author and current lead maintainer of this module is the [@condor-labs development team](https://condorlabs.io/team).

**More about Condorlabs [Here](https://condorlabs.io/about).**

## License

[MIT](LICENSE)
