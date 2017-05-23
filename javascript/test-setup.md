
## Tools
+ babel-register
+ mocha
+ chai
+ gulp

`babel` for translating `ES6` to normal `javascript` code, `mocha` is the test framework, `chai` is the test library, and the automation tool here is `gulp`.

The command `mocha --compilers js:babel-register` and setup in gulpfile `compilers: ['js:babel-core/register',]` is using babel to parse javascript file.

> .babelrc
```json
{
    "presets": ["es2015"]
}
```

> package.json
```json
{
  "name": "play",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "dependencies": {
    "babel-preset-es2015": "^6.24.1",
    "babel-register": "^6.24.1",
    "chai": "^3.5.0",
    "gulp-mocha": "^4.3.1",
    "gulp": "^3.9.1"
  },
  "devDependencies": {
    "babel-preset-es2015": "^6.24.1",
    "babel-register": "^6.24.1",
    "chai": "^3.5.0",
    "gulp": "^3.9.1",
    "gulp-mocha": "^4.3.1"
  },
  "scripts": {
    "test": "mocha --compilers js:babel-register"
  },
  "author": "",
  "license": "ISC"
}
```

> gulpfile.js
```js
var gulp = require('gulp'),
    mocha = require('gulp-mocha');


gulp.task('test', function(){
    return gulp.src(['test/*.js'])
	.pipe(mocha({
	        compilers: ['js:babel-core/register',]
    }));
});

gulp.task('tdd', function(){
    return gulp.watch(['src/*.js', 'test/*.js'], ['test']);
})
```

Type `gulp tdd` to watch js file change, and execute `gulp test` at the same time, which is using mocha to test code.