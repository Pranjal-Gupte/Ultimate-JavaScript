# Chapter 1 - Console Logs, Errors, Warnings And More

Being a scripting language, JavaScript cannot run on its own. In fact, the browser is responsible for running JavaScript code. When a user requests an HTML page with JavaScript in it, the script is sent to the browser and it is up to the browser to execute it.   
The main advantage of JavaScript is that all modern web browsers support JavaScript. So, you do not have to worry about whether your site visitor uses Internet Explorer, Google Chrome, Firefox or any other browser. JavaScript will be supported.

## Writing First Program
```js
console.log("Hello World");
```
This program writes (logs) a message to the console. The method is highly useful for testing purposes.  
**Note: When testing console methods, be sure to have the console view visible. Press F12 in your browser and select "Console" tab to open the console view.**

## Warning

You can create and display your own warning in console by typing the following:
```js
console.warn("This is a warning");
```

## Clear

You can clear your console by typing the following: 
```js
console.clear();
```

## Time and Time End

The `time()` method starts a timer in the console view. The `time()` method allows you to time code for testing purposes.
```js
console.time();
console.log("Some thing in between time and timeEnd");
console.timeEnd();
```
**Note: You can run many timers at the same time. Use the label parameter to name different timers.**
```js
console.time(label);
```
Which is the fastest, the for loop or the while loop?
```js
console.time("for loop");
for (let i = 0; i < 1000000; i++) {
  // some code
}
console.timeEnd("for loop");

let i = 0;
console.time("while loop");
while (i < 1000000) {
  i++
}
console.timeEnd("while loop");
// This is an example of console.time() with label. You can run this code can see which one is the fastest.
```

## Error

You can create  and display your own error in console by typing the following:
```js
console.error("This is a error");
```

## Table

The `table()` method writes a table to the console.
```js
console.table(tabledata, tablecolumns)
```

## Comments
JavaScript comments can be used to explain JavaScript code, and to make it more readable. JavaScript comments can also be used to prevent execution, when testing alternative code.

### Single Line Comments
```js
// This is a single line comment
// It is denoted by two forward slashes
// Single
// Line
// Comment
```

### Multiline Comments
```js
/* This
is a 
multiline 
comment */

/* This is denoted by
one forward slash then two stars and
then one forward slash*/
```

## Links

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/pranjalagupte)  
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/pranjalagupte/)

## Authors
 - [@PranjalGupte](https://github.com/Pranjal-Gupte/)