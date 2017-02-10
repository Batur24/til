
# cherry-pick

在一个分支commit之后，另一个分支要同步这个commit
```
git checkout A
git commit -m "Fixed the bug x"
git checkout B
git cherry-pick A
```

[参考](http://stackoverflow.com/questions/7259135/git-commit-to-multiple-branches-at-the-same-time/18529576#18529576)
