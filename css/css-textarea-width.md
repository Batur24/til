
# Textarea Width

I noticed that the actual width of textarea is longer than the container.
I found a solution on [stackoverflow](https://stackoverflow.com/questions/271067/how-can-i-make-a-textarea-100-width-without-overflowing-when-padding-is-present), below is the code

```css
.boxsizingBorder {
    -webkit-box-sizing: border-box;
       -moz-box-sizing: border-box;
            box-sizing: border-box;
}
```

Css is quite odd