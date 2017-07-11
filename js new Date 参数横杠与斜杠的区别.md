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
VM389:1 Wed Dec 12 2012 00:00:00 GMT+0800 (中国标准时间)
VM389:2 Sun Dec 02 2012 00:00:00 GMT+0800 (中国标准时间)
VM389:3 Sun Dec 02 2012 00:00:00 GMT+0800 (中国标准时间)
VM389:5 Wed Dec 12 2012 08:00:00 GMT+0800 (中国标准时间)
VM389:6 Sun Dec 02 2012 00:00:00 GMT+0800 (中国标准时间)
VM389:7 Sun Dec 02 2012 08:00:00 GMT+0800 (中国标准时间)
VM389:8 Sun Dec 02 2012 00:00:00 GMT+0800 (中国标准时间)
```
