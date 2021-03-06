# @zeix/stylelint-config

Zeix Stylelint config optimized for SCSS and Prettier.

- extends: [`stylelint-config-standard-scss`](https://github.com/stylelint-scss/stylelint-config-standard-scss), [`stylelint-config-prettier`](https://github.com/prettier/stylelint-config-prettier)
- plugins: [`stylelint-order`](https://github.com/hudochenkov/stylelint-order)

To see the rules that this config uses, please read the [config itself](https://github.com/zeixcom/stylelint-config/blob/master/index.js).

## Installation

`npm i @zeix/stylelint-config --save-dev`

## Usage

Create a `stylelint.config.js` file and add an extends key.

```js
module.exports = {
  extends: ["@zeix/stylelint-config"],
};
```

[Documentation for the extends option](https://stylelint.io/user-guide/configure/#extends)

## Extending the config

Simply add a "rules" key to your config, then add your overrides and additions there.

For example, to turn off the scss/at-if-no-null rule:

```js
module.exports = {
  extends: ["@zeix/stylelint-config"],
  rules: {
    "scss/at-if-no-null": null,
  },
};
```

## BEM

Projects using the BEM methodology may add the following rule to check selectors accordingly:

```js
module.exports = {
  extends: ["@zeix/stylelint-config"],
  rules: {
    "selector-class-pattern": [
      "^(?:(?:o|c|u|t|s|is|has|_|js|qa)-)?[a-zA-Z0-9]+(?:-[a-zA-Z0-9]+)*(?:__[a-zA-Z0-9]+(?:-[a-zA-Z0-9]+)*)?(?:--[a-zA-Z0-9]+(?:-[a-zA-Z0-9]+)*)?(?:\\[.+\\])?$",
      {
        resolveNestedSelectors: true,
      },
    ],
  },
};
```
