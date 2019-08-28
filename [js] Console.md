## 样式
颜色，字体，背景图片等都可以
```javascript
console.log('%c hello %c world %c!', 'background:gray; color:#fff; border-radius:3px', 'color:#0af', 'color:red')
```

## 函数调用路径
```javascript
function fun(){
  console.trace('call fun')
  // ...
}
```

## log分组
```javascript
console.group('g1')
console.log('a')
console.log('b')
console.groupEnd('g1')
```

## 以表格形式打印数组
控制台下可以直接 table()
```javascript
console.table([{id:1,name:'n1'},{id:2,name:'n2'}])
```

## 以目录形式打印对象
控制台下可以直接 dir()
```javascript
console.dir([{id:1,name:'n1'},{id:2,name:'n2'}])
```
