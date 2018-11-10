# NodeJS

## What is NodeJs ?
The makers of NodeJS took javascript which normally config to a browser.And they allow it to ran on your computer.<br /> 
Normally javascript rans in the browser. It's can only access your web page.<br />
But when you give it  environment to ran on a machine.<br />They took google chorme [V8 engine](https://en.wikipedia.org/wiki/Chrome_V8).And now V8 ran your machine. <br />So now you can access the files on your computers, which normally can do with javascript.<br />You can listen to [network traffic](https://en.wikipedia.org/wiki/Network_traffic) on your computer. <br />You can listen to http request, your machine gets and send back a file.<br />You can access Data Bases directly.<br />


When you ran on the commend line `node` ,you actually running a process that running on your computer.<br />There is no `window` object on a `nodejs` process because there is no `window`.<br />There is a `global` object.<br />For example: in the browser : 
```javascript
var a = 1;
window.a 
```
in NodeJs
```javascript
var a = 1;
global.a 
```
There is no also `document` object. Javascript has a global `document` object which is my `html` that thing build upon.<br />That thing tied to a `process`  which is the actual program process that running right now.<br />So i have a `process` object. 


### What you do with Node ?
- utilities on your machine.
* gulp , grunt or listen to file system changing and will do libery load.
- a web server (express , koa).
* instead of using ruby on rails, php , python. Will use express framwork for nodejs