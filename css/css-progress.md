
# Progress

I found that when set `<progress>` color, no matter `color` or `background-color`, the color isn't working. And the default color in `chrome` and `firefox` is different.

Then from [this thread](https://stackoverflow.com/questions/18368202/how-to-set-color-for-css3-html5-progress-element) different browsers imprement this funciton differently.

```css
    progress::-moz-progress-bar { background: blue; }   /*firefox*/
    progress::-webkit-progress-value { background: blue; } /*chrome & safari*/
    progress { color: blue; } /*IE10*/
```

if we need to combine `id` or `class`, just simply change progress to `id` or `class`.