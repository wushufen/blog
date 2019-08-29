```javascript
new Date().getTime().toString(36) +''+ Math.random().toString(36).substr(2, 10)
// jzv26il3zy5w0b1zfd
```

```javascript
var getUid = (function(){
  var last
  var inc = 0

  return function getUid(){
    var now = Date.now()

    if(now == last){
      inc += 1
    } else {
      last = now
      inc = 0
    }

    var uid = now.toString(36) // 8
      + (1000000 + inc).toString(36).substr(-3) // 3
      + Math.random().toString(36).substr(-4) // 4

    return uid
  }
})()
```
