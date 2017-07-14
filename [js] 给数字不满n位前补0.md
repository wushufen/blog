```javascript
n = 123;
m = 5;
String(n).length>m?
n:
(n/Math.pow(10, m)).toFixed(m).slice(2)
```
