```css
[class*="icon-"] {
  display: inline-block;
  width: 1em;
  height: 1em;
  background: center no-repeat;
  background-size: contain;
  position: relative;
  overflow: hidden;
}

[class*="icon-"]:before {
  content: "";
  display: block;
  width: 100%;
  height: 100%;
  position: absolute;
  left: -500px;
  box-sizing: content-box;
  border-right: 500px solid transparent;
  filter: drop-shadow(500px 0);
  background: center no-repeat;
  background-size: contain;
}

.icon-bell:before {
  background-image: url(https://gz-static-1257236698.cos.ap-guangzhou.myqcloud.com/bnx/imgs/icon/bell.png);
}
```

通过 `filter:drop-shadow()` 投影来实现可变色的副本， `left:-500px` 隐藏原图标，但是如果元素不在可视范围内的话， `drop-shadow` 不会画出投影，通过 `border-right: 500px solid transparent` 伸出透明的可视部分使 `drop-shadow` 起作用


参考： http://www.zhangxinxu.com/wordpress/2016/06/png-icon-change-color-by-css/
