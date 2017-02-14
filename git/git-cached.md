
# Git Cached

When a file is managed, later if we want that file to be ignore, it won't work if we just put it into the `.gitignore` file. We will have to deal with the `git cached`

```
git rm -rf --cached <file>
git add <file>
git commit -m "fix ignore fiel won't work"
```
