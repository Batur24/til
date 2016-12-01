
# Iterm2 Change Profile From Command Line

在zshrc/bashrc文件中加入下面这个函数:
```
it2prof() { echo -e "\033]50;SetProfile=$1\a" }
```
在命令行切换profile: it2prof pfofileName


参考: https://coderwall.com/p/s-2_nw/change-iterm2-color-profile-from-the-cli
