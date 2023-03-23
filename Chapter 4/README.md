# Chapter 4 - Operators And Expressions

A fragment of code that produces is called an expression. Every value written literally is an expression for example: 55 or "Pranjal".   
There are mainly Four Types of Operators in JavaScript which are:   

1. Arithmetic Operators
2. Assignment Operators
3. Comparison Operators
4. Logical Operators

## Arithmetic Operators

Arithmetic Operators are used to perform arithmetic operations on numbers. Arithmetic Operators are:   

| Operator | Description    |
|----------|----------------|
| +        | Addition       |
| -        | Subtraction    |
| *        | Multiplication |
| /        | Division       |
| %        | Modulus        |
| **       | Exponentiation |
| ++       | Increment      |
| --       | Decrement      |

Example of each Arithmetic Operators:
```js
const a = 10 + 10; // Addition Operator Adds

const b = 20 - 10; // Subtraction Operator Subtracts

const c = 20 * 2 ; // Multiplication Operator Multiplies

const d = 20 / 4 // Division Operator Divides and Gives Quotient as Output

const e = 10 % 5; // Modulus Operator Divides and Gives Remainder as Output

const f = 2 ** 3; // Exponentiation Operator Raises The First Operand To The Power Of The Second Operand.

let g = 10;
g++; // Adding 1 to 10
const gg = g; // Increment Operator Adds One | gg = 11

let h = 20;
h--; // Subtracting 1 from 10
const hh = h; // Decrement Operator Subtracts One | hh = 19
```

## Assignment Operators

Assignment operators assign values to JavaScript variables.

| Operator | Example | Same As    | Description                        |
| -------- | ------- | ---------- | ---------------------------------- |
| =        | x = y   | x = y      | Assignment Operator                |
| +=       | x += y  | x = x + y  | Addition Assignment Operator       |
| -=       | x -= y  | x = x - y  | Subtraction Assignment Operator    |
| *=       | x *= y  | x = x * y  | Multiplication Assignment Operator |
| /=       | x /= y  | x = x / y  | Division Assignment Operator       |
| %=       | x %= y  | x = x % y  | Remainder Assignment Operator        |
| **=      | x **= y | x = x ** y | Exponentiation Assignment Operator |

Example of each Assignment Operators:

```js
let a = 10; // Simple Assignment Operator assigns a value to a variable.

let x = 20;
x += 5; // Answer is 25
let text = "Hello";
text += " World"; // Answer is "Hello World"
// The Addition Assignment Operator adds a value to a variable.

let y = 10;
y -= 5; // Answer is 5
//The Subtraction Assignment Operator subtracts a value from a variable.

let z = 10;
z *= 5; // Answer is 50
// The Multiplication Assignment Operator multiplies a variable.

let p = 10;
p **= 5; // Answer is 100000
// The Exponentiation Assignment Operator raises a variable to the power of the operand.

let g = 10;
g /= 5; // Answer is 2
// The Division Assignment Operator divides a variable.

let h = 10;
g %= 5; // Answer is 0
// The Remainder Assignment Operator assigns a remainder to a variable.
```

## Comparison Operators

Comparison operators are used in logical statements to determine equality or difference between variables or values.   
Given that `x = 5`, the table below explains the comparison operators:

| Operator | Description                       | Operator's Name                   | Comparing | Returns |
| -------- | --------------------------------- | --------------------------------- | --------- | ------- | 
| ==       | Equal to                          | Equality Operator                 | x == 8    | False   |
|          |                                   |                                   | x == 5    | True    |
|          |                                   |                                   | x == "5"  | True    |
| ===      | Equal value and equal type        | Strict Equality Operator          | x === 5   | True    |
|          |                                   |                                   | x === "5" | False   |
| !=       | Not equal to                      | Inequality Operator               | x != 8    | True    |
|          |                                   |                                   | x != 5    | False   |
| !==      | Not equal value or not equal type | Strict Inequality Operator        | x !== 5   | False   |
|          |                                   |                                   | x !== "5" | True    |
|          |                                   |                                   | x !== 8   | True    |
| <        | Less than                         | Less than Operator                | x < 8     | True    |
|          |                                   |                                   | x < 1     | False   |
| >        | Greater than                      | Greater than Operator             | x > 4     | True    |
|          |                                   |                                   | x > 8     | False   |
| <=       | Less than or equal to             | Less than or Equal to Operator    | x <= 2    | False   |
|          |                                   |                                   | x <= 10   | True    |
| >=       | Greater than or equal to          | Greater than or Equal to Operator | x >= 2    | True    |
|          |                                   |                                   | x >= 8    | False   |

### Ternary Operator

Ternary Operator evaluates and executes a block of code based on the condition.   
```js
condition ? exp1 : exp2
```
Example syntax of `Ternary Operator` looks like this:

```js
const pass_or_not_pass = (marks > 32) ? "You are passed" : "You are not passed";
// If marks are greater than 32, you are passed else not.
```

## Logical Operators

Logical operators are used to determine the logic between variables or values.   
Given that `x = 6` and `y = 3`, the table below explains the logical operators:

| Operator     | Description | Example                      | Returns |
| ------------ | ----------- | ---------------------------- | ------- |
| &&           | Logical And | (x < 10 && y > 1)            | True    |
| &#124;&#124; | Logical Or  | (x == 5 &#124;&#124; x == 8) | False   |
| !            | Logical Not | !(x == y)                    | True    |

Example of each Logical Operators:

```js
let x = 5;
let y = 6;

(x > y && x == 5); // Returns False because x is smaller than y and in Logical and both values should be true
// (x < y && x == 5) Returns True

(x > y || x == 5); // Returns True because x is equal to 5 but x is not greater than y. In Logical or any one value should be true so the result will be true else false

(!true); // Returns false
(!false); // Returns true
// Logical not simply turns true to false and false to true
```

## Links

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/pranjalagupte)  
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/pranjalagupte/)

## Authors
 - [@PranjalGupte](https://github.com/Pranjal-Gupte/)
