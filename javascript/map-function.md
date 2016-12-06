
# Map function

```javascript
var numbers = [1, 4, 9]
var roots = numbers.map(Math.sqrt);
// roots [1, 2, 3]
// numbers [1, 4, 9]


var kvArray =  [{key:1, value:10},
                {key:2, value:20},
                {key:3, value:30}];

var reformattedArray = kvArray.map(function(obj){
    var rObj = {};
    rObj[obj.key] = obj.value;
    return rObj
})

// reformattedArray [{1: 10}, {2: 20}, {3: 30}]


```
