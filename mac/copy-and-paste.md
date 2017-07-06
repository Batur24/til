
# Copy and Paste

### Copy

I want to copy the path from `pwd` into clipboard, to use `pbcopy` command can achieve this.
```
pwd | pbcopy
```
alias `pbcopy` to `copy`, so know it is convenient to use copy in terminal. Not just `pwd`, `cat` or `less` can also combine with `pbcopy`.

### Paste

Likewise, there's `pbpaste` too.
```
pbpaste > test.md
```
command above can write clipboard text into `test.md`.
