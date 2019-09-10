新建 `~/.bash_profile`

添加
```bash
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_HOME/emulator
```

运行使其生效
```bash
source $HOME/.bash_profile
```

检验
```bash
echo $ANDROID_HOME
```
