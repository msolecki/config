### Add to your dev dependencies:

`yarn add @hookooekoo/eslint-config --dev`

## Prettier Config

Add configuration to package.json

```json
"prettier": "@hookooekoo/eslint-config/prettier.json"
```

## Stylelint Config

Add configuration to package.json

```json
"stylelint": {
    "extends": "@hookooekoo/eslint-config/stylelint.js"
}
```

## PostCSS Config

Create postcss.config.js in your project with content below:

```json
const postcssConfig = require('@hookooekoo/eslint-config/postcss');

module.exports = postcssConfig;
```

## Typescript Config

Add configuration to tsconfig.json. 

We have 2 separate configurations:
- @hookooekoo/eslint-config/tsconfig.json - for all API/backend projects
- @hookooekoo/eslint-config/tsconfig-next.json - for next websites

All options with path are relative so you should set those options in your project tsconfig.json file

```json
{
  "extends": "@hookooekoo/eslint-config/tsconfig.json",
  "compilerOptions": {
    "outDir": "./out",
    "baseUrl": ".",
    "paths": {
      "@/*": [
        "./src/*"
      ],
    }
  },
  "include": [
    "./next-env.d.ts",
    "./src/**/*.ts",
    "./src/**/*.tsx",
  ],
  "exclude": [
    "./out/**/*",
    "./node_modules/**/*"
  ]
}
```

## Eslint Config

#### API Config

Add configuration to package.json

```json
"eslintConfig": {
    "extends": "@hookooekoo/eslint-config"
},
```

#### NextJS Config

Add configuration to package.json

```json
"eslintConfig": {
    "extends": "@hookooekoo/eslint-config/next"
},
```
