```javascript
(function(){try{return 变量名,true}catch(e){}}())
```
解释：
```javascript
(function(){
    try{
        return 变量名,true; // 如果已定义则不抛错，返回 true
    }catch(e){
        // 不 return 结果为 undefined ，逻辑为 false ，所以这句可省略
        return false; // 未定义抛错返回 false 。
    }
}())
```
使用：
```javascript
var a;
if( function(){try{return a,true}catch(e){}}() ){
    alert('a 已定义')
}
```

```javascript
if( ! function(){try{return xxx,true}catch(e){}}() ){
    alert('xxx 未定义！')
}
```
