# 缓存机制

浏览器缓存机制是据http头决定的

缓存就是浏览器保存在硬盘或内存中的文件，包括http响应头

http响应头写明了该文件在什么时候过期

如果本地有缓存并且没有过期，则叫【强缓存】

如果本地有缓存但是过期了，则浏览器向服务器发送请求时，请求头上带上该文件信息，服务器判断该文件是否已修改，没有则返回304，该过程叫【协商缓存】

## 缓存是否过期
```
HTTP响应头
  date:             响应时 服务器时间
  expires:          Http1.0 标准，写明过期时间（服务器），可能与客户端有偏差
  Cache-Control:    Http1.1 标准
    max-age:        过期时长（秒）， date + max-age 为过期时间，优先于 expires
    no-cache:       向服务器确认资源是否被更改
    no-store:       绝对禁止缓存
```

## 协商缓存判断文件是否已修改
(1) 优先于 (2)

### (1) If-None-Match == Etag ? 304 : 200
```
HTTP请求头
If-None-Match:      文件指纹
```
```
HTTP响应头
Etag:               文件指纹（md5或其它）
```

### (2) If-Modified-Since == Last-modified ? 304 : 200
```
HTTP请求头
If-Modified-Since:  上次修改时间
```
```
HTTP响应头
Last-modified:      修改时间
```

## chrome 查看缓存文件信息
```
chrome://chrome-urls/
   chrome://cache
```
