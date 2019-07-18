控制台输入以下
```javascript
{}+[]
```
结果为 `0`， 是因为该语句解析 {} 为空语句块，相当于
```javascript
+[]
```
以下等同
```javascript
eval('{}+[]')
```

如果将该语句，放于表达式环境中时，会将 {} 解析为对象
```javascript
({})+[]
// 或者
result = {}+[]
```
结果为 `"[object Object]"`


## 非基本类型进行运算

非基本类型进行运算，
会判断 `valueOf` `toString` 是否返回基本类型，是则用来参与运算，否则报错。
相当于经过以下步骤：

```javascript
1 + (function(obj){
    // return obj

    var value = obj

    if(value !== Object(value)) return value

    if(typeof obj.valueOf == 'function'){
      value = obj.valueOf()
      if(value !== Object(value)) return value
    }

    if(typeof obj.toString == 'function'){
      value = obj.toString()
      if(value !== Object(value)) return value
    }

    throw TypeError('Cannot convert object to primitive value')

})({
    valueOf(){console.log('valueOf'); return {}},
    toString(){console.log('toString'); return {}}
})

```
