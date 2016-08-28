# Prototype

普通的object没有prototype属性
函数object有prototype属性

```javascript

var aObj = {}
aObj.hasOwnProperty("prototype") //false

var bObj = function(){}
bObj.hasOwnProperty("prototype") //true

```
