```javascript
console.log(new Date('2012/12/12'))
console.log(new Date('2012/12/2'))
console.log(new Date('2012/12/02'))

console.log(new Date('2012-12-12')) // 这个会自动加8h
console.log(new Date('2012-12-2'))
console.log(new Date('2012-12-02')) // 这个会自动加8h
console.log(new Date('2012-12-02 00:00:00'))  // 这个 ios 会无效
```

```
(program):2 Wed Dec 12 2012 00:00:00 GMT+0800 (中国标准时间)
(program):3 Sun Dec 02 2012 00:00:00 GMT+0800 (中国标准时间)
(program):4 Sun Dec 02 2012 00:00:00 GMT+0800 (中国标准时间)
(program):6 Wed Dec 12 2012 08:00:00 GMT+0800 (中国标准时间)
(program):7 Sun Dec 02 2012 00:00:00 GMT+0800 (中国标准时间)
(program):8 Sun Dec 02 2012 08:00:00 GMT+0800 (中国标准时间)
(program):9 Sun Dec 02 2012 00:00:00 GMT+0800 (中国标准时间)
```
