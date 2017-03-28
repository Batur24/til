
# Maragin Collapsing

If a block has a margin-bottom 20px, the next one has a margin-top 10px, the margin between these two blocks is 20px, the large one counts. This is called margin collapsing.

```css
<div style="margin-bottom: 20px">
</div>
<div style="margin-bottom: 10px">
</div>

//the margin is 20px
```
