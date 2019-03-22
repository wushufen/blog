## eslint
本地安装或全局安装eslint，全局安装不可保证队友安装

## .git/hoooks/pre-commit
`.git/hoooks/pre-commit`不受版本控制，须手动复制，或可通过`npm run dev`脚本写入
```bash
#!/usr/bin/env bash
if [ -f ".githook" ];then . ".githook";fi
```

## .githook
校验脚本。自定义的名字，放于根目录。通过`pre-commit`引用。或者直接写入`pre-commit`
```bash
#!/usr/bin/env bash

# eslint exists
eslint="./node_modules/.bin/eslint"
if [ ! -f "$eslint" ]; then
  eslint="eslint"
  if [ ! -n "$(command -v eslint)" ]; then
    # has not eslint
    exit 0
  fi
fi


# files
files=`git diff --cached --name-only | grep -E '(.js|vue)$'`


# -deleted
for file in $files; do
  if [ ! -f "$file" ]; then
    files=${files//$file/""}
  fi
done


# has not files to eslint
if [ -z "$files" ]; then
  exit 0
fi


# fix
# add again
rs=$($eslint $files --fix --format visualstudio)
git add $files


# echo error warning with color
rs=${rs//": error "/"\033[31m [error] \033[0m"}
# rs=${rs//": warning "/"\033[33m [warning] \033[0m"}


# # reject
if [[ "$rs" = *"[error]"* ]]; then
  echo -e "$rs"
  echo -e "\033[31m  ERROR  \033[0m"
  exit 1
fi

```
