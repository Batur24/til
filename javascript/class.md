
# ES6 class

ES6新增的class使得用js来写OOP很方便

```javascript
class Test{
    constructor(name){
        this.name = name
    }

    changeName(newName){
        this.name = newName
    }
}
t = new Test("batur");
console.log(t.name); //batur
t.changeName("MY")
console.log(t.name); //MY
```
