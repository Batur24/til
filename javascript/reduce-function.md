
# Javascript reduce function

```javascript
var sum = [0, 1, 2, 3].reduce(function(a, b) {
    return a + b
}, 0)
// sum 6
```

Arrow方式更加简洁
```javascript
let evens = [2,4,6,8,10]
let sum = evens.reduce((x,y) => x+y, 0)
// sum 30
```
