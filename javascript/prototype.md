# Prototype

每个object都有prototype属性  
但是普通的object用hasOwnProperty,显示没有prototype属性  
而函数object有prototype属性  
普通函数可以通过__proto__设置prototype  

```javascript

var aObj = {}
aObj.hasOwnProperty("prototype") //false

var bObj = function(){}
bObj.hasOwnProperty("prototype") //true

aObj.__proto__.test = "a test"
aObj.test //'a test'

```
[参考1 stackoverflow](http://stackoverflow.com/questions/572897/how-does-javascript-prototype-work)  
[参考2 mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/prototype)
