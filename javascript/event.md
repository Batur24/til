
# Javascript Event

NodeJs的events模块
`on`和`addListener`方法类似于jQuery中的`on`  
字符串"hello"是一个触发事件, `myEvent.emit("hello
")`匹配触发事件, 执行后面的函数, 打印"world"

```javascript
const event = require('events');
let myEvent = new event.EventEmitter();

myEvent.on("hello", function (msg) {
  console.log(msg)
});

myEvent.emit("hello", "world") //world
```


