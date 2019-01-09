## doc
http://eslint.cn/


## install
```
npm i eslint -g
npm i eslint-plugin-html eslint-plugin-vue -g
```

## run
```
eslint file.js
``


## config
`.eslintrc.json`
```json
{
  "parserOptions": {
    "sourceType": "module"
  },
  "env": {
    "browser": true,
    "node": true
  },
  "plugins": [
    "html",
    "vue"
  ],
  "extends": "eslint:recommended",
  "rules": {
    "indent": [
      2,
      2
    ],
    "semi": [
      1,
      "never"
    ],
    "quotes": [
      1,
      "single"
    ],
    "eqeqeq": 1
  },
  "globals": {}
}
```
