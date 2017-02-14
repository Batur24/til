
# Javascript md5

To compute the md5 digest of a string or file, we can use npm package `md5`

## Install
```
npm install md5
```

## Usage

To compute the md5 digest of a string

```javascript
var md5 = require('md5')
console.log(md5('message'));
```

It can also compute the md5 digest of a file
```javascript
var fs = require('fs');
var md5 = require('md5');

fs.readFile('package.json', function(err, buf){
    console.log(md5(buf));
})
```

## Link
[node-md5](https://github.com/pvorb/node-md5)



