# @zeix/stylelint-config

Zeix Stylelint config optimized for SCSS and Prettier.

- extends: [```stylelint-config-recommended-scss```](https://github.com/stylelint-scss/stylelint-config-recommended-scss), [```stylelint-config-prettier```](https://github.com/prettier/stylelint-config-prettier)
- plugins: [```stylelint-order```](https://github.com/hudochenkov/stylelint-order)


## Usage

### Install
```npm i @zeix/stylelint-config --save-dev```

### Config
Create a ```.stylelint.config.js``` file and add an extends key.

```js
module.exports = {
  extends: ['@zeix/stylelint-config'],
};
```

[Documentation for the extends option](https://stylelint.io/user-guide/configure/#extends)
