非基本类型进行运算， 会判断 valueOf toString 是否返回基本类型，是则用来参与运算，否则报错。 相当于经过以下步骤：

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
