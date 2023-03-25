# Chapter 6 - Strings, String Properties, String Methods and Template Literals

Strings are used to store and manipulate text. String can be created using the following syntax:

```js
const str = "Hello, World!";
str.length // This property prints the length of the string (includes space)
```

Strings can also be created with single quotes

```js
let str = 'Hello, World!';
```

## Template Literals

**Template Literals** use back-ticks (``) rather than the quotes ("" or '') to define a string:
```js
let text = `Hello World`;
```
With template literals, you can use both single and double quotes inside a string:

```js
let sentence = `He's often called "Johnny"`;
```

Template literals also make it easy to write multiline strings:

```js
// using the + operator with quotes
const message1 = 'This is a long message\n' + 
'that spans across multiple lines\n' + 
'in the code.'

// using template literal makes it easy!
const message2 = `This is a long message
that spans across multiple lines
in the code.`

console.log(message1)
```

**Template literals** provide an easy way to interpolate variables and expressions into strings. The method is called string **interpolation**.   

Syntax is:

```js
`${variable_name}` // Note "${variable_name}" should be inside back ticks
```

Example Code of Template Literals:

```js
const name = 'Jack';
console.log(`Hello ${name}`); // Output: Hello Jack

const result = 4 + 5;

// template literals used with expressions
console.log(`The sum of 4 + 5 is ${result}`); // Output: 9

console.log(`${result < 10 ? 'Too low': 'Very high'}`) // Output: Too low
```

## Escape Sequence Characters

If you try to print the following script, JavaScript will misunderstand it!

```js
let name = 'Adam D'Angelo';
```

To solve this problem, we can use single quote's escape sequence character.

```js
let name = 'Adam D\'Angelo';
```

Similarly we can use `\"` inside a string with double quotes.   
Other escape sequence characters are as follows:   

- `\n` -> New Line
- `\t` -> Tab
- `\r` -> Carriage Return
- `\b` -> Backspace
- `\f` -> Formfeed
- `\v` -> Vertical Tab   

and more....

## Index in JavaScript

Each element will have a unique position that identifies it. That position is called the element's **index**.  
**Note: Index in JavaScript always starts with 0 (it doesn't starts with 1).**

Example:

```js
let sentence = "JavaScript is cool";
// Here "J" will have index of "0", a of "1", v of "2", a of "3".....
```

### Access String Characters

You can access the characters in a string in two ways.

One way is to treat strings as an array. For example,

```js
const a = 'hello';
console.log(a[1]); // "e"
```

Another way is to use the method `charAt()`. For example,

```js
const a = 'hello';
console.log(a.charAt(1)); // "e"
// We will see more about charAt(), just scroll down and you will get it
```

## String Properties and Methods

In JavaScript, strings are immutable. That means the characters of a string cannot be changed. For example,


```js
let a = 'hello';
a[0] = 'H';
console.log(a); // "hello"
```

However, you can assign the variable name to a new string. For example,

```js
let a = 'hello';
a = 'Hello';
console.log(a); // "Hello"
```

Here are some common and highly used string methods:

| Method                  | Description                                               |
| ----------------------- | --------------------------------------------------------- |
| length                  | Returns the length of the string                          |
| slice(start, end)       | Returns a part of string                                  |
| substring(start, end)   | Returns a part of string                                  |
| replace(value1, value2) | Replaces a specified value with another value in a string |
| toUpperCase()           | Returns the passed string in upper case                   |
| toLowerCase()           | Returns the passed string in lower case                   |
| concat()                | Joins two or more strings                                 |
| trim()                  | Removes white spaces from both sides of a string          |
| trimStart()             | Removes white spaces only from the start of the string    |
| trimEnd()               | Removes white spaces only from the end of the string      |
| charAt(index)           | Returns the character at the specified index              |
| split()                 | Converts the string to an array of strings                |

Example of each methods:

```js
const text1 = 'hello';
const text2 = 'world';
const text3 = '     JavaScript    ';
const text4 = 'Apple, Banana, Kiwi';
const text5 = 'HELLO WORLD';

// getting the length of a string
console.log(text1.length); // 5

// slicing the string
const result1 = text1.slice(1, 3);
console.log(result1); // el

// returning a part of string
const result2 = text4.substring(7, 13);
console.log(result2); // Banana

// replacing string with string
const result3 = text1.replace("hello", "Hi");
console.log(result3); // Hi

// converting the text to uppercase
const result4 = text1.toUpperCase();
console.log(result4); // HELLO

// converting the text to lowercase
const result5 = text5.toLowerCase();
console.log(result5); // hello world

// concatenating two strings
const result6 = text1.concat(', ', text2);
console.log(result6); // hello, world

// trimming all white spaces from both sides
const result7 = text3.trim();
console.log(result6); // JavaScript

// trimming all white spaces from start
const result8 = text3.trimStart();
console.log(result8); // JavaScript    

// trimming all white spaces from end
const result9 = text3.trimEnd();
console.log(result9); //      JavaScript

// returning char at index 6
const result10 = text5.charAt(6);
console.log(result10); // W

// converting string to an array
const result11 = text4.split();
console.log(result11); // ['Apple Banana Kiwi']
```

## String Search Methods

String search methods are methods of string which are used to search in strings with strings.   
Some search methods are:

| Method        | Description                                                                             |
|---------------|---------------------------------------------------------------------------------------- |
| indexOf()     | Returns the index of the first occurrence of a string in a string                       |
| lastIndexOf() | Returns the index of the last occurrence of a specified text in a string                |
| search()      | Searches a string for a string and returns the position of the match (first occurrence) |
| includes()    | Returns true if a string contains a specified value else false                          |
| startsWith()  | Returns true if a string begins with a specified value else false                       |
| endsWith()    | Returns true if a string ends with a specified value else false                         |

Example of each methods:

```js
const text1 = "Please locate where 'locate' occurs!";

//  first occurrence of locate
const result1 = text1.indexOf("locate"); 
console.log(result1); // 7

// last occurrence of locate
const result2 = text1.lastIndexOf("locate");
console.log(result2); // 21

// first occurrence of locate
const result3 = text1.search("locate");
console.log(result3); // 7

// checks if where is included in text1
const result4 = text1.includes("where");
console.log(result6); // true

// checks if text1 starts with Ple
const result5 = text1.startsWith("Ple");
console.log(result7); // true

// checks if text1 ends with rs!
const result6 = text1.endsWith("rs!");
console.log(result8); // true
```

## Links

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/pranjalagupte)  
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/pranjalagupte/)

## Authors
 - [@PranjalGupte](https://github.com/Pranjal-Gupte/)