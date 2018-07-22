# Gatsby Standard - ESLint Config

[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com) [![npm](https://img.shields.io/npm/v/eslint-config-gatsby-standard.svg)](https://www.npmjs.com/package/eslint-config-gatsby-standard)

ESLint rule configuration for Gatsby Sites. This rule set is designed to closely match the Gatsby Starters while still following StandardJS. Simply install and extend to clean up your GatsbyJS code! The plugins and parser used are dependencies of this project. No need to specify them separately in your project.

This config is designed to be used in conjunction with prettier for automatic code formatting. Conflicting rules have been disabled through `eslint-config-prettier`. See the "Use With Atom" section below for a suggestion on how to implement this config with prettier for automatic linting and formatting.

`babel-eslint` is included to support new JavaScript features used in advanced Gatsby projects.

## Usage

Install the configs by running:

```sh
npm install --save-dev eslint  eslint-config-gatsby-standard
```

Then simply create a `.eslintrc.json` at your project root:

```json
{
  "extends": "gatsby-standard"
}
```

Be sure you also have an `.eslintignore` file in your project root so you won't receive unnecessary lint errors from Gatsby:

```
public
static
.cache
content
```

## Plugins Used:

- [eslint-config-standard](https://www.npmjs.com/package/eslint-config-standard)
- [eslint-plugin-standard](https://www.npmjs.com/package/eslint-plugin-standard)
- [eslint-plugin-react](https://www.npmjs.com/package/eslint-plugin-react)
- [eslint-plugin-babel](https://github.com/babel/eslint-plugin-babel)
- [eslint-config-standard-react](https://www.npmjs.com/package/eslint-config-standard-react)
- [eslint-plugin-import](https://www.npmjs.com/package/eslint-plugin-import)
- [eslint-plugin-node](https://www.npmjs.com/package/eslint-plugin-node)
- [eslint-plugin-promise](https://www.npmjs.com/package/eslint-plugin-promise)
- [eslint-config-prettier](https://www.npmjs.com/package/eslint-config-prettier)

## Use With Atom

To use with prettier just add the `.prettierrc.json` config file to the root of the project:

```json
{
  "semi": false,
  "singleQuote": true,
  "trailingComma": "es5"
}
```

If you use Atom, you can install linter-eslint to view the results of Gatsby Standard immediately.

```
apm install linter-eslint
```

Disable "Fix errors on save" and install prettier-atom:

```
apm install prettier-atom
```

Choose "ESLint Integration" in the package settings. This will use a global install of prettier-eslint but it will still follow the Gatsby Standard linting rules.

Be sure to check "Run Prettier Last" and optionally "Format Files on Save" and "Show in Status Bar." Most other code editors have similar packages to format on demand.

## License

MIT &copy; 2018 Brandon Kalinowski
