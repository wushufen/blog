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
## 修改最近commit
```
git commit --amend
```
## 撤消上次提交记录，不恢复代码
```
 git reset --soft HEAD~1
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

## branch 新建分支
查看所有分支
```
git branch -a
```
新建分支
```
git branch dev
```
将分支推送到服务器
```
git push -u origin dev
```
新建并切换分支
```
git checkout -b dev
```

## branch 合并分支
将A合并到当前
```
git merge A
```

## branch 删除分支
删除本地分支
```
git branch -D br
```
删除远程分支
```
git push origin :br
```


## 恢复某文件（夹）到之前版本
```
git checkout b4f4ebcfabe03eabf454540d32c00a0106ac6575 .\static\
```

## 忽略已添加到版本库的文件
```
$ git rm -r -f --cached **/node_modules/
```

## 配置文件
全局： `~/.gitconfig`
本地： `.git/config`


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

手册
https://github.github.com/training-kit/downloads/zh_CN/github-git-cheat-sheet/

https://try.github.io/levels/1/challenges/1

分支创建与合并
https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001375840038939c291467cc7c747b1810aab2fb8863508000

Git合并指定文件到另一个分支
https://www.cnblogs.com/phpper/p/7609238.html



## 开发流程
```javascript

       m                    
       |                    
       |-->f1               
   ?   |   |                
   |   |-->|                // test
   |-->|   |                
       |-->|                // fix && test
       |   |                
t1 <---|<--|                // publish && tag
       |                    
       |------>f2  f3?      
       |       |   |        
       |       v   |        
       |------>r<--|        // test
       |       |            
       |------>|            // fix && test
       |       |            
t2 <---|<------|            // publish && tag
       |                    
       |                    

[dev|tag]/20101122.1212/desc

==============================================

       m   d                     
       |   |                     
       |   |-->f1                
       |   |   |                 
       |   |-->|-->r1            // test
       |   |       |             // update && test
t1 <---|<--|<------|             // publish && tag
       |   |                     
       |   |---------->f2       f3?
       |   |           |        |
       |   |---------->|-->r2<--|
       |   |               |     
t2 <---|<--|<--------------|     
       |   |                     
       |   |                     


```

```
1. 开始开发
git checkout -b branchName

2. 提测修bug
git merge origin/master

3. 测完合并（重点！）
git checkout master
git pull
git merge branchName
git push

4. 处理冲突（若有）
git add .
git commit -m 'msg'
git push

5. 回归测试

5. 打标签
git tag tagName
git push origin tagName

6. 提审（记住打完标签再提，已免忘了）

7. 删除分支
git branch -d branchName
git push origin :branchName
```
