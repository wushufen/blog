# eval函数会影响js压缩效果

## 原因
最近写的一个框架发现压缩后内部函数名没有被压缩，分析发现是因为代码里的 `eval` 函数。
Uglify, YUI, JsMin 都是如此。

## 解决方法
把`eval`调用改为`window.eval`用 Uglify 压缩可以神奇的避免这个情况。 YUI, JsMin 仍然不行。
