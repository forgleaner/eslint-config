﻿# eslint-config

[![build][travis-image]][travis-url]
[![commitizen][commitizen-image]][commitizen-url]
[![prettier][prettier-image]][prettier-url]
[![download][download-image]][download-url]
[![npm][npm-image]][npm-url]
[![semantic][semantic-image]][semantic-url]

[npm-image]: https://img.shields.io/npm/v/@fatesigner/eslint-config.svg?color=blue&logo=npm
[npm-url]: https://npmjs.com/package/@fatesigner/eslint-config
[travis-image]: https://travis-ci.com/fatesigner/eslint-config.svg?color=green&token=i21P7stb8bZPNjZakvsi&branch=master
[travis-url]: https://travis-ci.com/fatesigner/eslint-config
[download-image]: https://img.shields.io/npm/dw/@fatesigner/eslint-config.svg?color=yellowgreen
[download-url]: https://npmjs.com/package/@fatesigner/eslint-config
[commitizen-image]: https://img.shields.io/badge/commitizen-friendly-green.svg
[commitizen-url]: http://commitizen.github.io/cz-cli/
[prettier-image]: https://img.shields.io/badge/styled_with-prettier-ff69b4.svg?logo=prettier
[prettier-url]: https://github.com/prettier/prettier
[semantic-image]: https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?style=flat-square
[semantic-url]: https://opensource.org/licenses/MIT

eslint插件配置，包含js、ts、vue通用规则

**基于 [eslint-config-standard](https://github.com/standard/eslint-config-standard).**

## Install
```bash
npm i @fatesigner/eslint-config -D

// install peerDependencies
npm i eslint prettier -D
npm i @babel/eslint-parser @babel/core @babel/preset-env @babel/preset-react -D
npm i @typescript-eslint/parser @typescript-eslint/eslint-plugin -D
```

## 使用
添加以下代码到 `.eslintrc.js`
```javascript
const eslint = require('@fatesigner/eslint-config');

module.exports = {
  root: true,
  overrides: [eslint]
}
```

## 添加对 ts 和 vue 类型文件的规则支持
添加以下代码到 `.eslintrc.js`
```javascript
// javascript
const eslint = require('@fatesigner/eslint-config');

// typescript
const tslint = require('@fatesigner/eslint-config/ts');

// vue
const vuelint = require('@fatesigner/eslint-config/vue');

module.exports = {
  root: true,
  overrides: [eslint, tslint, vuelint]
};
```

## 或者可以在您的项目中使用此插件针对 [prettier](https://github.com/prettier/prettier) 的部分配置
添加以下代码到 `package.json`
```javascript
{ 
  ...
  "prettier": "@fatesigner/eslint-config/.prettierrc"
}
```
