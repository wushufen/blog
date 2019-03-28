## #!/usr/bin/env bash
首行声明bash脚本，`bash`可以换成`python` `node`等语言
```bash
#!/usr/bin/env bash
```

## 变量
不分类型，可理解为都是字符串，“=”左右不能有空格
```bash
v1=string
v2="this is a string"
v3="
multiple
string
"
```

## 字符串拼接
```bash
v4="$v1${v2}abc"
```

## echo 输出
```bash
echo $v3 # 不加双引号，输出换行会变成空格
```
```bash
echo "$v3"
```
```bash
echo -e "\033[31mERROR\033[0m" # 输出红色的`ERROR`
```


## 直接运行命令
```bash
# code...
git add .

```

## 运行命令，把输出返回给变量
```bash
string=$(git diff --cached --name-only)
string=`git diff --cached --name-only`
```

## 测试
没有bool类型，if语句接收测试，测试为真返回0，假返回1。
一般单`[  ]`跟`[[  ]]`结果一样，但`[`会有不准的情况。
`[ -n $string ]`返回的结果不对，要用`[[  ]]`。
`[  ]`变量为空串时会报错，须给变量加双引号。
```bash
[[ -f $file ]]
```
```bash
echo $?
```

## if
```bash
if [[  ]]; then
else
fi
```

## for
```bash
for line in $lines; do
  echo $line
done
```

## |
管道。把前一个输出作为后一个命令的输入
```bash
v="
a
b
c
"
rs=$(echo "$v" | egrep "a|c")
```

## xargs
有些命令不能接收管道的参数，可通过`xargs`来传递
```bash
echo "js.js" | xargs eslint --fix
```

## exit
退出。正常退出`exit 0`，非常正常退出返回非0。


## egrep
`egrep "reg" $file`
正则过滤每行。等于`grep -E`。`$file`须为文件，但管道可接收字符串







