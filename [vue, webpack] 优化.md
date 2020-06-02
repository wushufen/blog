## vue-cli-service build --modern
```
vue-cli-service build --modern
```

会生成两个版本的包，现代浏览器版 `<script type="module">` 生效，旧版浏览器 `<script nomodule>` 生效
> 注意：`<script type="module">` 服务器必须 `CORS`: `Access-Control-Allow-Origin: *`
