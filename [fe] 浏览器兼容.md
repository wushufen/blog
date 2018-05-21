* 浏览器统计 http://tongji.baidu.com/data/browser

* ie7.js
* boxsizing.htc
* ie-css3.htc
* css expression ie6-7
* css behavior ie6-9

## ios
### 字体异常变大
```css
.parent{
  overflow: auto;
}
.child{
  float: left; // 或者 inline-block
  // 文字不换行长于宽度
  // 字体小于 20
}
```
解决
```css
.child{
  max-width: 100%;
}
```
### overflow 滑动不顺畅
解决
```css
.el{
  overflow: auto;
  -webkit-overflow-scrolling: touch; // <------------==
}
```
