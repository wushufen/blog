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
* 1 value.valueOf 是否函数？
  * 1.1 是：返回值为基本类型？
    * 1.1.1 是：用返回值参与运算
    * 1.1.2 否：-> 2
  * 1.2. 否：-> 2
* 2 value.toString 是否函数？
  * 2.1 是：返回为基本类型？
    * 2.1.1 是：用返回值参与运算
    * 2.1.2 否：-> 3
  * 2.2 否：-> 3
* 3 报错

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
    valueOf(){return {}},
    toString(){return {}}
})

```
