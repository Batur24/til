

## -p 
Show the patch introduced with each commit.


## 一行显示日志
    git log --pretty=oneline


## 自定义格式/图标显示
    git log --pretty=format:"%h - %an, %ar : %s"
    git log --pretty=format:"%h %s" --graph


参考： https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History
