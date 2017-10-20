

## Array

### Remove Duplicate

```js
  let fruites = ["banana","banana"]
  fruites = Array.from(new Set(fruits));
  // ["banana"]
```

### Remove False Element
```js
    let fruites = ["banana","banana",null,"",undefined]
    fruites.filter(item => item);
    // ["banana","banana"]
```