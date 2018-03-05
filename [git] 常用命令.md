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
第一次指定分支
```
git push -u origin master
```
第二次
```
git push
```

## pull 从服务器拉下
第一次指定分支
```
git pull origin master
```
第二次
```
git pull
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
生成  
`c:/user/xxx/.ssh/私钥名`  
`c:/user/xxx/.ssh/私钥名.pub`  
私钥名可改  
公钥`私钥名.pub`放服务器

### config
新建`c:/user/xxx/.ssh/config`文件
```
Host 配置1
    HostName 112.33.1.20
    User git
    identityfile ~/.ssh/私钥名
    
Host 配置2
    HostName 112.33.1.20
    User git
    Port 8000
    identityfile ~/.ssh/私钥名
```

### git clone
```
git clone git@配置1:path/to/xxx.git
```

## 问题
### early EOF
http://blog.csdn.net/djy1992/article/details/50604937

### 检出指定目录或文件
http://www.cnblogs.com/liangzai-cool/p/5821138.html

## links 链接
https://try.github.io/levels/1/challenges/1
