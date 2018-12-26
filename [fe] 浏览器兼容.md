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
  -webkit-overflow-scrolling: touch; // <------------== 20181226 将其移至 html
}
```

### ios -webkit-overflow-scrolling: touch 动态添加内容溢出时，容器无法滑动内容
overflow:scroll 

解决

20181226:  将其移至 html
```css
html{-webkit-overflow-scrolling: touch}
```


通过css使用内容高度超过容器高度
```css
.outer {
    height: 350px;
    overflow: scroll;
    -webkit-overflow-scrolling: touch;
}
.outer:before {
    content:"";
    float: left;
    height: calc(100% + 1px);
    width: 1px;
    margin-left: -1px;
}
```
```css
.outer {
  height: 350px;
  overflow: scroll;
  -webkit-overflow-scrolling: touch;
}

.inner {
  height: calc(100% + 1px);
}
```
https://www.cnblogs.com/xiahj/p/8036419.html

