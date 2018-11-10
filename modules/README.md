# Super basics on nodejs

## How modules work on nodejs
Modules are you basically load on file in to another. 

```javascript 
//module1.js
var m2 = require('./module2'); // ./ - looking for a file in the same directory
console.log(m2);

//module2.js
var a = 1;
module.exports.a = a;
```

And then ran `node module1` <br />
The output is an object : `{ a : 1 }` <br />

```javascript
module.exports.b = 2;
```
The output now `{ a: 1, b: 2 }`

```javascript
exports.a = a; //same as module.exports.a = a;
exports.b = 2;// module.exports.b = 2;
```

Or you can overwrite the entire `module.exports` object and make it a `function`
```javascript
//module1.js
var m2 = require('./module2'); 
m2();

//module2.js
module.exports = function(){
console.log('module 2');
};

```

## npm modules
for example `npm install uderscore` <br />
`npm` allows you maintain dependencies.

## A basic web server http