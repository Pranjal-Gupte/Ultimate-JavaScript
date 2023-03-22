# Chapter 3 - Data Types

A data type, in programming, is a classification that specifies which type of value a variable has and what type of mathematical, relational or logical operations can be applied to it without causing an error.   
There are two types of Data Types in JavaScript   
1. Primitive Data Types &
2. Reference Data Types or Non-Primitive Data Types

## Primitive Data Types

Primitive Data Types is a set of basic Data Types which are primarily used in JavaScript. There are 7 Primitive Data Types in JavaScript:   
1. Null
2. Number
3. String
4. Symbol
5. Boolean
6. BigInt
7. Undefined

## Reference Data Types

Reference Data Types is a set of Data Types which are not used primarily in JavaScript. There are 4 Reference Data Types in JavaScript:
1. Object
2. Array
3. Function
4. Date

# Primitive Data Types

## String

JavaScript strings are for storing and manipulating text. A JavaScript string is zero or more characters written inside quotes.

```js
let carName1 = "Volvo XC60";  // Double quotes
let carName2 = 'Volvo XC60';  // Single quotes
let carName3 = `Volvo XC60`; // Back quotes
```

## Number

JavaScript has only one type of number. Numbers can be written with or without decimals.

```js
let x = 3.14; // A number with decimals
let y = 3; // A number without decimals
```

Extra large or extra small numbers can be written with scientific (exponent) notation:

```js
let x = 123e5; // 12300000
let y = 123e-5; // 0.00123
```

## Boolean

A JavaScript Boolean represents one of two values: **true** or **false**.   
Very often, in programming, you will need a data type that can only have one of two values, like
- YES / NO
- ON / OFF
- TRUE / FALSE
For this, JavaScript has a Boolean data type. It can only take the values **true** or **false**.

```js
const x = 10 > 9;
console.log(x); // Returns true
const y = 10 > 20;
console.log(y); // Returns false
```

## BigInt()

JavaScript `BigInt` variables are used to store big integer values that are too big to be represented by a normal JavaScript `Number`. JavaScript integers are only accurate up to 15 digits.   
To create a `BigInt`, append n to the end of an integer of call `BigInt()`:
```js
let x = 9999999999999999;
let y = 9999999999999999n;
```
```js
let x = 1234567890123456789012345n;
let y = BigInt(1234567890123456789012345);
```

## Symbol()

A JavaScript `Symbol` is a primitive datatype just like `Number`, `String`, or `Boolean`.   
It represents a unique "hidden" identifier that no other code can accidentally access.   
For instance, if different coders want to add a person.id property to a person object belonging to a third-party code, they could mix each others values.   
Using `Symbol()` to create a unique identifiers, solves this problem:

```js
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};

let id = Symbol('id');
person[id] = 140353;
// Now person[id] = 140353
// but person.id is still undefined
```

## Undefined

In JavaScript, a variable without a value, has the value `undefined`. The type is also `undefined`.
```js
let car; // Value is undefined, type is undefined
```
Any variable can be emptied, by setting the value to undefined. The type will also be undefined.
```js
car = undefined; // Value is undefined, type is undefined
```
### Empty Values

An empty value has nothing to do with `undefined`. An empty string has both a legal value and a type.
```js
let car = ""; // The value is "", the typeof is "string"
```

## Null

The `null` value indicates an empty or unknown value. It is initially a placeholder that represents "nothing". The `null` value is defined as an empty object so using typeof operator on a variable holding `null` shows it's type to be object.
```js
let number = null;
```
The code above suggests that the "number" variable is empty at the moment and may have a value later.

# Reference Data Types

## Array

An `array` is an ordered collection of data, which can hold more than one value.   
Arrays are used to store multiple values in a single variable. This is compared to a variable that can store only one value.   
Each item in an `array` has a number attached to it, called a **numeric index**, that allows you to access it. In JavaScript, arrays start at index zero and can be manipulated with various methods.

### Creating an Array

```js
const arrayName = ["item1", "item2", "item3", ...];
// Note: Arrays can more than one data type init.
const car = ["BMW", 23, true];
```

### Why Use Arrays?

If you have a list of items (a list of car names, for example), storing the cars in single variables could look like this:
```js
let car1 = "Mercedes";
let car2 = "Volvo";
let car3 = "BMW";
```
However, what if you want to loop through the cars and find a specific one? And what if you had not 3 cars, but 300?   
The solution is an array!   
An array can hold many values under a single name, and you can access the values by referring to an index number.

### Using the JavaScript Keyword new

The following example also creates an Array, and assigns values to it:
```js
const cars = new Array("Mercedes", "Volvo", "BMW");
```
The two examples above do exactly the same.   
There is no need to use `new Array()`.   
For simplicity, readability and execution speed, use the array literal method.

## Object

In real life, a car is an object.   
A car has properties like weight and color, and methods like start and stop:   
|Object| Properties | Methods |
|------------------------------------------------------------| -------- | -------- |
|[![car](https://www.w3schools.com/js/objectExplained.gif)]()| car.name = Fiat | car.start() |
| | car.model = 500 | car.drive() |
| | car.weight = 850kg | car.brake() |
| | car.color = white | car.stop() |

All cars have the same properties, but the property values differ from car to car.   
All cars have the same methods, but the methods are performed at different times.

### Creating an Object

Objects are variables, but objects can contain many values.   
This code assigns many values (Fiat, 500, white) to a variable named car:

```js
const car = {
    brand: "Fiat",
    model: 500,
    color: "white"
}
// The values are written as key:value pairs
```

## Date

JavaScript `Date` objects represent a single moment in time in a platform-independent format.

### Creating Date Objects

Date objects are created with the `new Date()` constructor.   
There are 9 ways to create a date object:
```js
new Date()
new Date(date string)

new Date(year,month)
new Date(year,month,day)
new Date(year,month,day,hours)
new Date(year,month,day,hours,minutes)
new Date(year,month,day,hours,minutes,seconds)
new Date(year,month,day,hours,minutes,seconds,ms)

new Date(milliseconds)
```

```js
// Example
const date = new Date();
```

## Function

A JavaScript `function` is a block of code designed to perform a particular task.   
A JavaScript `function` is executed when "something" invokes it (calls it).  
JavaScript functions are defined with the `function` keyword. You can use a function **declaration** or a function **expression**.

```js
function functionName(parameters) {
    // code to be executed
}
```
Declared functions are not executed immediately. They are "saved for later use", and will be executed later, when they are invoked (called upon).

## Links

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/pranjalagupte)  
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/pranjalagupte/)

## Authors
 - [@PranjalGupte](https://github.com/Pranjal-Gupte/)