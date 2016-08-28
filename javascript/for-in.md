
# for...in

这个有点像python的for循环.
```javascript
var obj = {"a":1,"b":2,"c":3}

for(var prop in obj){
    console.log(prop, obj[prop])
}
//a,1
//b,2
```

但是涉及到prototype,就有点复杂了.  
for会把prototype的属性也会遍历出来.

```javascript
var obj = {"a":1,"b":2,"c":3};
function play(){
    this.fun = "it's fun"
}
play.prototype = obj;
var newObj = play();

console.log(newObj) //{fun: "it\'s fun"}
for(var prop in newObj){
    console.log(prop, obj[prop])
}
//a,1
//b,2
//fun,"it\'s fun"
```
:-(  

[参考](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)

