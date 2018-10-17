简写
```
i install
-g --global
-S --save
-D --save-dev
```

安装 `cnpm`
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

安装模块
```
npm i [-g,-S,-D] pack1 pack2 ...
```

已存在package.json安装
```
npm i
```

npm版本
```
npm -v
```

更新npm
```
npm i -g npm
```

查看npmjs服务器上的模块信息
```
npm view packName version
npm view packName versions
```

查看本地模块信息
```
npm ls packName
npm ls packName -g
```
