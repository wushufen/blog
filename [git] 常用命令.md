# git

## clone 从仓库克隆
```
git clone git@weili:/wd.git
```

## init 新建
```
git init
```

## remote add origin 服务器地址
```
git remote add origin git@xxx/xxx.git
```

## add 添加文件
```
git add *.html
```

## commit 提交文件
```
git commit -m 'msg'
```

## push 推送到服务器
```
git push -u origin master
```

## pull 从服务器拉下
```
git pull origin master
```

## 恢复某文件（夹）到之前版本
```
git checkout b4f4ebcfabe03eabf454540d32c00a0106ac6575 .\static\
```


## ssh
### 生成密钥对
```
ssh-keygen -t rsa -C "your_email@youremail.com"
```
公钥`xx.pub`放服务器，私钥放 `c:/user/xxx/.ssh`

### config
```
Host weili
    HostName 112.33.1.20
    User git
    Port 8000
    identityfile ~/.ssh/私钥名
```

## links 链接
https://try.github.io/levels/1/challenges/1
