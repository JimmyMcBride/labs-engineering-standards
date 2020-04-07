# Setting Up ESLint And Prettier

Setting up linters and code formatters is really important to group projects.
When people are doing things like using different kinds of quotes, or people are
following different semicolon rules, code can become a confusing mess real quick.
Adding things like code formatters and linters can be really beneficial to building
a uniform and readable code base.

## Install ESLint and Prettier VS Code Extensions

Make sure every team member has
[prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
and [eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
VS Code extension's installed.

> It's recommended to turn format on save on. Click on prettier link above and
> search for "Format On Save" for instructions on setting that up in vs code.
> Also, check out section "Linter Integration". 🔥

## Add .rc Files, Scripts, and Dependencies

Now we need to add dependencies to our project with some rc files! Woo hoo! 👏

In the root of your project's directory run;
`yarn add eslint prettier eslint-config-prettier eslint-plugin-prettier`
or `npm i eslint prettier eslint-config-prettier eslint-plugin-prettier`.

> Note: For react apps, add `eslint-plugin-react` to dependencies as well!

Then we can add a file named `.eslintrc.js` with the following content for a
react app.

```javascript
module.exports = {
  env: {
    commonjs: true,
    browser: true,
    es6: true,
    node: true,
  },
  extends: [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:prettier/recommended",
  ],
  parserOptions: {
    ecmaFeatures: {
      jsx: true,
    },
    ecmaVersion: 2018,
    sourceType: "module",
  },
  plugins: ["react", "prettier"],
  rules: {},
  overrides: [
    {
      files: ["**/*.test.js"],
      env: {
        jest: true,
      },
    },
  ],
};
```

For node repos, add this version.

```javascript
module.exports = {
  env: {
    node: true,
    commonjs: true,
    es6: true,
  },
  extends: ["eslint:recommended", "plugin:prettier/recommended"],
  parserOptions: {
    ecmaFeatures: {
    ecmaVersion: 2018,
    sourceType: "module",
  },
  plugins: ["prettier"],
  rules: {},
  overrides: [
    {
      files: ["**/*.test.js"],
      env: {
        jest: true,
      },
    },
  ],
};
```

Then we can add a .prettierrc.js with the following content
for both React and Node projects.

```javascript
module.exports = {
  trailingComma: "es5",
  tabWidth: 2,
  semi: true,
  singleQuote: true,
};
```

Then we can add some scripts to our `package.json`.

```json
{
  "scripts": {
    "lint": "eslint .",
    "lint:fix": "eslint --fix .",
    "format": "prettier --write \"**/*.+(js|jsx|json|yml|yaml|css|md)\""
  }
}
```
