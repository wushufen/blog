```javascript
{
  "window.title": "${activeEditorLong}",
  "window.menuBarVisibility": "default",
  "editor.minimap.maxColumn": 25,
  "editor.minimap.showSlider": "always",
  // 缩进
  "editor.tabSize": 2,
  // 滚轮缩放
  "editor.mouseWheelZoom": true,
  // 平滑滚动
  "editor.smoothScrolling": true,
  // 自动补全记忆
  "editor.suggestSelection": "recentlyUsedByPrefix",
  // 控制是否在键入时自动显示建议。
  "editor.quickSuggestions": {
    "other": true,
    "comments": true,
    "strings": true
  },
  // 触发自动补全的时间毫秒
  "editor.quickSuggestionsDelay": 3,
  // 显示空白符
  "editor.renderWhitespace": "all",
  // 显示控制符
  "editor.renderControlCharacters": true,
  // ctrlCmd 或 alt 加鼠标多光标编辑
  "editor.multiCursorModifier": "ctrlCmd",
  // 保存自动格式化
  "editor.formatOnSave": true,
  // 保存自动格式化等待时间
  "editor.formatOnSaveTimeout": 3000,
  // 自动猜测文件编码 // 不太准
  // "files.autoGuessEncoding": true,
  // 自动保存 // 不好
  // "files.autoSave": "onFocusChange",
  // emmet tab触发补全
  "emmet.triggerExpansionOnTab": true,
  // 内置prettier格式化插件
  "prettier": {
    // js使用单引号
    "singleQuote": true,
    // 对象保留最后逗号 (js中为原样，vue中会自动加上？)
    "trailingComma": "es5",
    // 分号
    "semi": false,
  },
  // vue高亮与格式化插件
  "vetur.format.defaultFormatter": {
    // 指定格式化插件
    // "Beautify" "prettier"
    // "html": "prettier", // 格式属性全都换行了
    // "html": "Beautify",
    "js": "prettier-eslint",
    // "css": "Beautify",
    // // "scss": "prettier",
    // "less": "Beautify",
  },
  // vue文件
  "[vue]": {
    "editor.formatOnSave": true,
    // 结尾新行
    // "files.insertFinalNewline": true
  },
  "[html]": {},
  "[wxml]": {},
  "[css]": {},
  "[less]": {},
  "[scss]": {},
  "[javascript]": {},
  "[json]": {},
  "terminal.integrated.shell.windows": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
  "git.autofetch": true,
  "git.confirmSync": false,
  "git.enableSmartCommit": true,
  "files.associations": {
    "*.cjson": "jsonc",
    "*.wxss": "css",
    "*.wxs": "javascript"
  },
  "emmet.includeLanguages": {
    "wxml": "html"
  },
  "minapp-vscode.disableAutoConfig": true,
  "editor.minimap.enabled": false,
  "workbench.colorTheme": "Monokai",
  "editor.suggest.localityBonus": true,
  "breadcrumbs.enabled": false,
  "explorer.autoReveal": true,
  "terminal.integrated.cursorBlinking": true,
  "workbench.editor.highlightModifiedTabs": true,
  "merge-conflict.autoNavigateNextConflict.enabled": true,
  "gitlens.views.repositories.files.layout": "tree",
  // eslint
  "eslint.options": {
    "plugins": [
      "vue"
    ]
  },
  "eslint.validate": [
    "javascript",
    "html",
    "vue",
  ],
  "eslint.autoFixOnSave": true,
  // tinypng.com
  "tinypng.apiKey": "tN13BjNkfRqNLx11BVnhYxkRPFlmmQxQ",
}
```
