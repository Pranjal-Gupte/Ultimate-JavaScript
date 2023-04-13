# Chapter 8 - Arrays and Array's Methods

Arrays are variables which can store multiple values in it. For example.
```js
const words = ["hello", "world", "welcome"];
const fruits = ["apple", "banana", "mango"];
```
Here `words` and `fruits` are arrays. These arrays are storing 3 values in it.

## Creating Array

You can create arrays with two ways:

### 1. Using an array literal

The easiest way to create an array is by using array literal `[]`. For example,

```js
const array1 = ["eat", "sleep", "code", "repeat"];
```

### 2. Using the new keyword

You can also create an array using JavaScript's `new` keyword.

```js
const array2 = new Array("eat", "sleep", "code", "repeat");
```

In both of the above examples, we have created an array having four elements.

> **Note: It is recommended to use array literal to create an array.**

Here are more examples of array:

```js
// empty array
const myList = [];

// array of numbers
const numberArray = [2, 4, 6, 8];

// array of strings
const stringArray = ['eat', 'work', 'sleep'];

// array with mixed data types
const newData = ['work', 'exercise', 1, true];
```

You can also store arrays, functions and other objects inside an array. For example,

```js
const newData = [
    {'task1': 'exercise'},
    [1, 2 ,3],
    function hello() { console.log('hello')}
];
```

## Accessing Elements of an Array

You can access elements of an array using indexes (0, 1, 2, ...). For example,

```js
const myArray = ['h', 'e', 'l', 'l', 'o'];

// first element
console.log(myArray[0]);  // "h"

// second element
console.log(myArray[1]); // "e"
```

-----

[![indexesInfo](https://cdn.programiz.com/sites/tutorial2program/files/javascript-array-indexing.png)]()

> **Note: Array's index starts with 0, not 1.**

-----

## Finding the length

You can easily get the length of an array by using length method. For example,

```js
let numbers = [1, 7, 8, 9, 5];

console.log(numbers.length); // 5
```

## Change the Elements of an Array

You can also add elements or change the elements by accessing the index value.

```js
let dailyActivities = [ 'eat', 'sleep'];

// this will add the new element 'exercise' at the 2 index
dailyActivities[2] = 'exercise';

console.log(dailyActivities); // ['eat', 'sleep', 'exercise']
```

## Array Methods

In JavaScript, there are various array methods available that makes it easier to perform useful calculations.   
Some of the commonly used JavaScript array methods are:

| Method      | Description                                                                            |
| ----------- | -------------------------------------------------------------------------------------- |
| concat()    | joins two or more arrays and returns a result                                          |
| indexOf()   | searches an element of an array and returns its position                               |
| find()      | returns the first value of an array element that passes a test                         |
| findIndex() | returns the first index of an array element that passes a test                         |
| forEach()   | calls a function for each element                                                      |
| includes()  | checks if an array contains a specified element                                        |
| push()      | adds a new element to the end of an array and returns the new length of an array       |
| unshift()   | adds a new element to the beginning of an array and returns the new length of an array |
| pop()       | removes the last element of an array and returns the removed element                   |
| shift()     | removes the first element of an array and returns the removed element                  |
| sort()      | sorts the elements alphabetically in strings and in ascending order in numbers         |
| slice()     | selects the part of an array and returns the new array                                 |
| splice()    | removes or replaces existing elements and/or adds new elements                         |
| toString()  | converts an array to a string of (comma separated) array values                        |
| join()      | joins all array elements into a string but in addition you can specify the separator   |
| reverse()   | reverses the elements in an array                                                      |

### Example: JavaScript Array Methods

```js
let array1 = ['eat', 'sleep', 'code', 'repeat'];
let array2 = ['again'];
let array3 = [1, 3, 4, 9, 8];
let array4 = ["E", "A", "D", "B", "C"];
let array5 = [5, 9, 8, 3, 0, 1, 6, 2, 4, 7];
let array6 = ["JavaScript", 1, "a", 3];
let array7 = ['JavaScript', 'is', 'fun'];
let primeNumbers = [2, 3, 5, 7, 9, 11];
let numbers = [1, 2, 3, 4, 5];

// concatenating two arrays
const arrayConcat = array1.concat(array2);
console.log(arrayConcat); // ['eat', 'sleep', 'code', 'repeat', 'again']

// finding the index position of string
const position = array1.indexOf('code');
console.log(position);

// finding the first even number from an array

// function to check even number
function isEven(element) {
  return element % 2 == 0; // we'll study more on functions in detail in upcoming chapters
}

// get the first even number
let evenNumber = array3.find(isEven);
console.log(evenNumber); // 4

// finding the first odd number from an array

// function that returns odd number
function isOdd(element) {
  return element % 2 !== 0;
}

// returns the index of the first odd number in the array
let firstOdd = array3.findIndex(isOdd);

console.log(firstOdd); // 0

// computing square of each number using forEach()

// function to compute square of each number
function computeSquare(element) {
  console.log(element * element);
}

console.log(array3.forEach(computerSquare)); // 1 9 16 81 64

// checking if sleep is included

const checkInclude = array1.includes("sleep");
console.log(checkInclude); // true

// add an element at the end

const addElementAtEnd = array1.push("restart");
console.log(addElementAtEnd); // ['eat', 'sleep', 'code', 'repeat', 'restart']

// add an element at the beginning of an element

const addElementAtBeginning = array1.unshift("start");
console.log(addElementAtBeginning); // ['start', 'eat', 'sleep', 'code', 'repeat']

// remove last element from an array

const removeLastElement = array1.pop();
console.log(removeLastElement); // ['eat', 'sleep', 'code']

// remove first element from an array

const removeFirstElement = array1.shift();
console.log(removeFirstElement); // ['sleep', 'code', 'repeat']

// sort alphabets and numbers (in ascending order)

const sortAlphabets = array4.sort();
console.log(sortAlphabets); // ['A', 'B', 'C', 'D', 'E']

const sortNumbers = array5.sort();
console.log(sortNumbers); // [0, 1, 2, 3, 4, 5, 6, 7 , 8, 9]

// create another array by slicing numbers from index 3 to 5

const slicedArray = array5.slice(3, 7);
console.log(slicedArray); // [3, 0, 1, 6]

// replace 1 element from index 4 by 13
const removedElement = primeNumbers.splice(4, 1, 13);
console.log(removedElement); // [9]
console.log(primeNumbers); // [2, 3, 5, 7, 13, 11]

// returns a string with elements of the array separated by commas
let itemsString = array6.toString();

console.log(itemsString); // JavaScript,1,a,3

// join all elements of array using space

let joinedMessage = array7.join(" ");
console.log(joinedMessage); // JavaScript is fun

// reversing the numbers array

let reversedArray = numbers.reverse();
console.log(reversedArray);
```

## Looping through Arrays

Arrays can be looped through using the classical JavaScript for loop or through some other methods discussed below.

- forEach() loop
- map()
- filter()
- reduce()
- Array.from()

## forEach() method

The `forEach` element method executes a provided function for each element of an array.

## forEach() Syntax

The syntax if the `forEach()` method is:

```js
arr.forEach(callback(currentValue), thisArg);
```

Here, `arr` is an array.

## forEach() Parameters

The `forEach()` method takes in,

- `callback` - The function to execute on every array element. It takes in:
  
  - `currentValue` - The current element being passed from the array.

- `thisArg` (optional) - Value to use as `this` when executing `callback`. By default, it is undefined.

## forEach() Return Value

> **Notes:**   
> - **`forEach()` does not change the original array.**
> - **`forEach()` executes `callback` once for each array element in order.**
> - **`forEach()` does not execute `callback` for array element without variables.**

### Example 1: Printing Contents of an Array

```js
function printElements(element, index) {
    console.log('Array Element ' + index + ': ' + element);
}

const prices = [1800, 2000, 3000, , 5000, 500, 8000];

// forEach does not execute for elements without values
// in this case, it skips the third element as it is empty
prices.forEach(printElements);

/*
Output:
Array Element 0: 1800
Array Element 1: 2000
Array Element 2: 3000
Array Element 4: 5000
Array Element 5: 500
Array Element 6: 8000
*/
```

### Example 2: Computing Squares of Numbers in an Array

```js
let numbers = [2, 3, 5, 9, 8];

// function to compute square of each number
function computeSquare(element) {
  console.log(element * element);
}

// compute square root of each element
numbers.forEach(computeSquare);

/*
Output:
4
9
25
81
64
*/
```

## map() Method

The `map()` method creates a new array with the results of calling a function for every array element.

## map() Syntax

The syntax of the `map()` method is:

```js
arr.map(callback(currentValue), thisArg);
```

Here, `arr` is an array.

## map() Parameters

The `map()` method takes in,

- `callback` - The function called for every array element. Its return value are added to the new array. It takes in:
  
  - `currentValue` - The current element being processed from the array.

- `thisArg` (optional) - Value to use as `this` when executing `callback`. By default, it is `undefined`.

## map() Return Value

- Returns a new array with elements as the returns values from the `callback` function for each element.

> **Notes:**
> - `map()` does not change the original array.
> - `map()` executes `callback` once for each array element in order.
> - `map()` does not execute `callback` for array elements without values.

### Example 1: Mapping Array Elements Using Custom Function

```js
const prices = [1800, 2000, 3000, 5000, 500, 8000];

let newPrices = prices.map(Math.sqrt);
// [ 42.42640687119285, 44.721359549995796, 54.772255750516614,
//   70.71067811865476, 22.360679774997898, 89.44271909999159 ]
console.log(newPrices);

// custom arrow function
const string = "JavaScript";
const stringArr = string.split(''); // array with individual string character

let asciiArr = stringArr.map(x => x.charCodeAt(0));

// map() does not change the original array
console.log(stringArr); // ['J', 'a', 'v', 'a','S', 'c', 'r', 'i', 'p', 't']

console.log(asciiArr); // [ 74,  97, 118,  97, 83,  99, 114, 105, 112, 116 ]

/*
Output
[
  42.42640687119285,
  44.721359549995796,
  54.772255750516614,
  70.71067811865476,
  22.360679774997898,
  89.44271909999159
]
[
  'J', 'a', 'v', 'a',
  'S', 'c', 'r', 'i',
  'p', 't'
]
[
   74,  97, 118,  97,
   83,  99, 114, 105,
  112, 116
]
*/
```

### Example 2: Computing Squares of Elements

```js
let numbers = [2, 4, 6, 8, 10];

// function to return the square of a number
function square(number) {
  return number * number;
}

// apply square() function to each item of the numbers list
let square_numbers = numbers.map(square);
console.log(square_numbers);

// Output: [ 4, 16, 36, 64, 100 ]
```

> **Note: `map()` assigns `undefined` to the new array if the `callback` function returns `undefined` or nothing.**

## filter() Method

The `filter()` method returns a new array with all elements that pass the test defined by the given function.

## filter() Syntax

The syntax of the `filter()` method is,

```js
arr.filter(callback(element), thisArg);
```

Here, `arr` is an array.

## filter() Parameters

The `filter()` method takes in:

- `callback` - The test function to execute on each array element; returns `true` if element passes the test, else `false`. It takes in:   

  - `element` - The current element being passed from the element.

- `thisArg` (optional) - The value to use as `this` when executing `callback`. By default, it is `undefined`.

## filter() Return Value

- Returns a new array with only elements that passed the test.

> **Notes:**
> - **`filter()` does not change the original array.**
> - **`filter()` does not execute `callback` for array elements without values.**

### Example 1: Filtering Out Values From Array

```js
const prices = [1800, 2000, null, 3000, 5000, "Thousand", 500, 8000];

function checkPrice(element) {
  return element > 2000 && !Number.isNaN(element);
}

let filteredPrices = prices.filter(checkPrice);
console.log(filteredPrices); // [ 3000, 5000, 8000 ]

// using arrow function
let newPrices = prices.filter((price) => (price > 2000 && !Number.isNaN(price)));
console.log(newPrices); // [ 3000, 5000, 8000 ]
```

Here, all the numbers **less than or equal to 2000**, are all the **non-numeric** values are filtered out.

### Example 2: Checking Even Numbers and Creating new Array

```js
let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// function to check even numbers
function checkEven(number) {
  if (number % 2 == 0)
    return true;
  else
    return false;
}

// create a new array by filter even numbers from the numbers array
let evenNumbers = numbers.filter(checkEven);
console.log(evenNumbers);

// Output: [ 2, 4, 6, 8, 10 ]
```

## reduce() Method

The `reduce()` method executes a reducer function on each element of the array and returns a single output value.

## reduce() Syntax

The syntax of the `reduce()` method is:

```js
arr.reduce(callback(accumulator, currentValue), initialValue)
```

Here, `arr` is an array.

## reduce() Parameters

The `reduce()` method takes in:

- `callback` - The function to execute on each array element (except the first element if no `initialValue` is provided). It takes in

   - `accumulator` - It accumulates the callback's return values.
   - `currentValue` - The current element being passed from the array.

- `initialValue` (optional) - A value that will be passed to `callback()` on first call. If not provided, the first element acts ass the `accumulator` on the first call and `callback()` won't execute on it.

> **Note: Calling `reduce` on an empty array without `initialValue` will throw `TypeError`.**

## reduce() Return Value

- Returns single value resulting after reducing the array.

> **Notes:**
> - `reduce()` executes the given functions for each value from left to right.
> - `reduce()` does not change the original array.
> - It is almost always safer to provide `initialValue`.

### Example 1: Sum of All Values of Array

```js
const numbers = [1, 2, 3, 4, 5, 6];

function sumReducer(accumulator, currentValue) {
  return accumulator + currentValue;
}

let sum = numbers.reduce(sumReducer);
console.log(sum) // 21

// using arrow function
let summation = number.reduce((accumulator, currentValue) => accumulator + currentValue);
console.log(summation) // 21
```

### Example 2: Joining Each Element of String Using reduce()

```js
const message = ["JavaScript ", "is ", "fun."];

// function to join each string elements
function joinStrings(accumulator, currentValue) {
  return accumulator + currentValue;
}

// reduce join each element of the string
let joinedString = message.reduce(joinStrings);
console.log(joinedString);

// Output: JavaScript is fun.
```

### Example 3: Subtracting Numbers in Array

```js
const numbers = [1800, 50, 300, 20, 100];

// subtract all numbers from first number
// since 1st element is called as accumulator rather than currentValue
// 1800 - 50 - 300 - 20 - 100

let difference = numbers.reduce((accumulator, currentValue) => accumulator - currentValue);
console.log(difference); // 1330

const expenses = [1800, 2000, 3000, 5000, 500];
const salary = 15000;

// function that subtracts all array elements from given number
// 15000 - 1800 - 2000 - 3000 - 5000 - 500

let remaining = expenses.reduce((accumulator, currentValue) => accumulator - currentValue, salary);
console.log(remaining); // 2700
```

This example clearly explains the difference between passing an `initialValue` and not passing an `initialValue`.

## Array.from() Method

The `Array.from()` method creates a new array from any array-like or iterable object.

## Array.from() Syntax

The syntax of the `Array.from()` method is:

```js
Array.from(arraylike, mapFunc, thisArg);
```

The `Array.from()` method, being a static method, is called using the `Array` class name.

## Array.from() Parameters

The `Array.from()` method can take **three** parameters:

- `arraylike` - Array-like or iterable object to convert to an array.
- `mapFunc` (optional) - Map function that is called on each element.
- `thisArg` (optional) - Value to use as
`this` when executing `maFunc`.

> **Note:** `Array.from(obj, mapFunc, thisArg)` is equivalent to `Array.from(obj).map(mapFunc, thisArg)`.

## Array.from() Return Value

- Returns a new `array` instance.

> **Note:** This method can create an array from:
> - array-like objects - The objects that have length property and have indexed elements like `String`.
> - Iterable objects like `Map` or `Set`.

### Example 1: Creating New Array From String

```js
let newArray = Array.from("abc");
console.log(newArray); // [ "a", "b", "c" ]
```

### Example 2: Array.from() Method with Array Like Objects

```js
let array1 = Array.from("JavaScript");
console.log(array1); // ['J', 'a', 'v', 'a', 'S', 'c', 'r', 'i', 'p', 't']
```

In the above example, we have used the `Array.from()` method to create a new array from the `'JavaScript'` string.

We have called the method using `Array` class as `Array.from('JavaScript')`. The method returns a new array `['J', 'a', 'v', 'a', 'S', 'c', 'r', 'i', 'p', 't']` and assigns it to `array1`.

### Example 3: Array.from() Method with Mapping Function

```js
// function that returns a new array
function createArray(arraylike, mapFunc) {
  return Array.from(arraylike, mapFunc);
}

// using arrow function for mapFunc
let result = createArray([2, 4, 6], (element) => element + 2);

console.log(result); // [ 4, 6, 8 ]
```

In the above example, we have passed a mapping function in the `Array.from()` method that increases every element of the array being created by **2**.

## Multidimensional Arrays

A multidimensional array is an array that contains another array. For example,

```js
// multidimensional array
const data = [[1, 2, 3], [1, 3, 4], [4, 5, 6]];
```

## Create a Multidimensional Array

Here is how you can create multidimensional arrays in JavaScript.

### Example 1

```js
let studentsData = [["Julia", 89], ["Sanju", 95], ["Rahul", 92]];
```

### Example 2

```js
let student1 = ["Julia", 89];
let student2 = ["Sanju", 95];
let student3 = ["Rahul", 92];

// multidimensional array
let studentsData = [student1, student2, student3];
```

Here, both example 1 and example 2 creates a multidimensional array with the same data.

## Access Elements of an Multidimensional Array

You can access the elements of a multidimensional array using indices (0, 1, 2 …). For example,

```js
let x = [
['Jack', 24],
['Sara', 23], 
['Peter', 24]
];

// access the first item 
console.log(x[0]); // ["Jack", 24]

// access the first item of the first inner array
console.log(x[0][0]); // Jack

// access the second item of the third inner array
console.log(x[2][1]); // 24
```

You can think of a multidimensional array (in this case, x), as a table with 3 rows and 2 columns.

-----

[![accessingMultidimensionalArray](https://cdn.programiz.com/sites/tutorial2program/files/multidimensional-array.png)]()

<center>Accessing multidimensional array elements</center>

-----

## Add an Element to a Multidimensional Array

You can use the Array's push() method or an indexing notation to add elements to a multidimensional array.

### Example 1: Adding an Element to Outer Array

```js
let studentsData = [['Jaani', 90], ['Soni', 94],];
studentsData.push(['Piyush', 91]);

console.log(studentsData); //[["Jack", 24], ["Sara", 23], ["Peter", 24]]
```

### Example 2: Adding Element to the Inner Array

```js
// using index notation
let studentsData = [['Jack', 24], ['Sara', 23],];
studentsData[1][2] = 'hello';

console.log(studentsData); // [["Jack", 24], ["Sara", 23, "hello"]]
```

<center>OR</center>

```js
// using push()
let studentsData = [['Jack', 24], ['Sara', 23],];
studentsData[1].push('hello');

console.log(studentsData); // [["Jack", 24], ["Sara", 23, "hello"]]
```

You can also use the Array's `splice()` method to add an element at a specified index. For example,

```js
let studentsData = [['Jack', 24], ['Sara', 23],];

// adding element at 1 index
studentsData.splice(1, 0, ['Peter', 24]);

console.log(studentsData); // [["Jack", 24], ["Peter", 24], ["Sara", 23]]
```

## Remove an Element from a Multidimensional Array

You can use the Array's `pop()` method to remove the element from a multidimensional array. For example,

### Example 1: Remove Element From Outer Array

```js
// remove the array element from outer array
let studentsData = [['Jack', 24], ['Sara', 23],];
studentsData.pop();

console.log(studentsData); // [["Jack", 24]]
```

### Example 2: Remove Element From Inner Array

```js
// remove the element from the inner array
let studentsData = [['Jack', 24], ['Sara', 23]];
studentsData[1].pop();

console.log(studentsData); // [["Jack", 24], ["Sara"]]
```

You can also use the `splice()` method to remove an element at a specified index. For example,

```js
let studentsData = [['Jack', 24], ['Sara', 23],];

// removing 1 index array item
studentsData.splice(1,1);
console.log(studentsData); // [["Jack", 24]]
```

## Iterating Over Multidimensional Array

You can iterate over a multidimensional array using the Array's `forEach()` method to iterate over the multidimensional array. For example,

```js
let studentsData = [['Jack', 24], ['Sara', 23],];

// iterating over the studentsData
studentsData.forEach((student) => {
    student.forEach((data) => {
        console.log(data);
    });
});

/*
Output: 
Jack
24
Sara
23
*/
```

The first `forEach()` method is used to iterate over the outer array elements and the second `forEach()` is used to iterate over the inner array elements.

You can also use the `for...of` loop to iterate over the multidimensional array. For example,

```js
let studentsData = [['Jack', 24], ['Sara', 23],];

for (let i of studentsData) {
  for (let j of i) {
    console.log(j);
  }
}

/*
Output:
Jack
24
Sara
23
*/
```

You can also use the `for` loop to iterate over a multidimensional array. For example,

```js
let studentsData = [['Jack', 24], ['Sara', 23],];

// looping outer array elements
for(let i = 0; i < studentsData.length; i++){

    // get the length of the inner array elements
    let innerArrayLength = studentsData[i].length;
    
    // looping inner array elements
    for(let j = 0; j < innerArrayLength; j++) {
        console.log(studentsData[i][j]);
    }
}
```

## Links

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/pranjalagupte)  
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/pranjalagupte/)

## Authors

 - [@PranjalGupte](https://github.com/Pranjal-Gupte/)