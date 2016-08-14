

# 使用ctags，vim实现定义跳转

生成tags文件，使用ctrl+]，跳转到定义

ctags
```
    ctags -R  -f ./tags
    ctrl ]
```

## mac ctags 配置


```
# you have ctags but it does not work...
$ ctags -R --exclude=.git --exclude=log *
ctags: illegal option -- R
usage: ctags [-BFadtuwvx] [-f tagsfile] file ...

#you need to get new ctags, i recommend homebrew but anything will work
$ brew install ctags

#alias ctags if you used homebrew
$ alias ctags="`brew --prefix`/bin/ctags"

#try again!
ctags -R --exclude=.git --exclude=log *

#puts tags file into you .gitignore (probably global) and you're all set!

#PS. i was inspired to install ctags by https://workshops.thoughtbot.com/vim video by @r00k, thanks man!

```
https://gist.github.com/nazgob/1570678

## 虚拟环境配置
```
ctags -R --fields=+l --languages=python --python-kinds=-iv -f ./tags $(python -c "import os, sys; print(' '.join('{}'.format(d) for d in sys.path if os.path.isdir(d)))")
```
https://www.fusionbox.com/blog/detail/navigating-your-django-project-with-vim-and-ctags/590/
