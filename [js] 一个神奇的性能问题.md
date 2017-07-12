```javascript
var map = {}


console.time(1)
for (var i = 0; i < 1000; i++) {
    map['str' + i] = function() { /*...*/ }
}
console.timeEnd(1)


console.time(2)
for (var i = 0; i < 1000; i++) {
    map['str' + i] = function() { /*...*/ }
}
console.timeEnd(2)


console.time(3)
for (var i = 0; i < 1000; i++) {
    map['str' + i] = function() { /*...*/ }
}
console.timeEnd(3)
```
```
1: 9.138ms
2: 4427.729ms
3: 1.169ms
```
为什么第二次如此之慢？？ (chrome, node.js)
