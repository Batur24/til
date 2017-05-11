
# Tmux Conf

I found how to use navication of vim style in tmux. Just put below code in `.tmux.conf` file

```
bind h select-pane -L
bind j select-pane -D
bind k select-pane -U
bind l select-pane -R
```

the default `select-pane` is `ctrl-b`