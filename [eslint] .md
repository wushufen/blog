## doc
http://eslint.cn/


## install
```
npm i eslint -g
npm i eslint-plugin-vue -g
```

## run
```
eslint file
``
--fix
```
eslint file --fix
```

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
    "vue"
  ],
  "extends": [
    "eslint:recommended",
    "plugin:vue/recommended"
  ],
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
    "comma-dangle": [
      1,
      "only-multiline"
    ],
    "object-curly-newline": [
      1,
      {
        "multiline": true
      }
    ],
    "object-property-newline": [
      1,
      {
        "allowMultiplePropertiesPerLine": true
      }
    ],
    "eqeqeq": 1
  },
  "globals": {}
}
```


## vscode
```json
{
  "eslint.options": {
    "plugins": [
      "vue"
    ]
  },
  "eslint.validate": [
    "javascript",
    "html",
    "vue"
  ],
  "eslint.autoFixOnSave": true,
  "vetur.format.defaultFormatter.js": "prettier-eslint",
}
```
