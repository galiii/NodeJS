# Read Files with Node.js

JavaScript was only available in the browser, so font-enf developers may only familiar with the [FileReader API](https://www.htmlgoodies.com/beyond/javascript/read-text-files-using-the-javascript-filereader.html#fbid=PfBQ7GOxcEB) <br />

Node.js has its own set of libraries meant for Handling OS and filessystem tasks, like opening and reading files.<br />

There 2 ways you can open and read file using `fs` module:
* Load all the contents at once (buffering)
* Incrementally load contents (streaming)

### Buffering Contents with fs.readFile
it isn't necessarily the bedt or most effcient


#### Using fs.readFileSync
the `readFileSync` function read data from file in a synchronous manner.<br />This function blocks the rest of the code from executing until all the data is read from a file.<br />The function is particularly useful when your application has to load configuration settings before it can perform any other tasks.

```javascript

```

If you print the object `rawdata` to the console
```javascript
<Buffer 5b 0a 20 20 20 20 7b 0a 20 20 20 20 20 20 20 20 22 6e 61 6d 6522 3a 20 22 47 61 6c 69 22 2c 0a 20 20 20 20 20 20 20 20 22 67 65 6e 64 65 72 22 3a 20 ... >
```

However we want to read the the file in uts JSON format, not the raw hex data.

`JSON.parse` this function handels parsing the raw data, converts it to ASCII text, and parses the actual JSON data in th a JavaScript object.
```javascript
let students = JSON.parse(rawsdata);
```
### Using require 
Another approach is to use the global `require` method to read and parse JSON files. This is the same method you use to load Node modules, but it can also be used to load JSON

```javascript
'use strict';

let jsonData = require('./db/students.json');

console.log(jsonData);
```
It Works exactly like the `readFileSync` code we showed above, but it is a globally available method yhat you can use anywhere, which has its advantages.



