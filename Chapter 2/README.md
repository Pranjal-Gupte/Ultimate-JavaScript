# Chapter 2 - Variables var, let and const

Just like we have to follow some rules while speaking English (The Grammar), we have some rules to follow while writing a JavaScript program. The set of these rules is called a **syntax**.

## What is a variable?

A variable is a container that stores a value. This is very similar to the container used to store rice, wheat, oats, etc. (Treat this as an analogy).   
The value of a JavaScript variable can be changed during the execution of a program.
```js
var a = 7;
let a = 7;
// Here "a" is identifier "=" is assignment operator and "7" is liberal. 
// This is how we declare a variable.
```

## Rules for choosing variable names

- Letters, digits, underscores and "$" sign is allowed.
- Must begin with a $, _, or a letter.
- JavaScript reserved words cannot be used as variable name.
- Mango and mango are different variables (case sensitive).

## How to declare variables?

We can declare variables using `var`, `let` and `const`.

## Variable var

Creating a variable using `var` keyword.

```js
var x = "Mango";
var y = 10;
var z = 12.5;
```
The `var` statement declares a function-scoped or globally-scoped variable, optionally initializing it to a value.   
The `var` keyword is used in all JavaScript code from 1995 to 2015.   
The `let` and `const` keywords were added to JavaScript in 2015.
If you want your code to run in older browsers, you must use `var`.

## Variable const

```js
const pi = 3.14;
const pi2 = 22/7;

const x = "Hello";
x = "Hi"; // Gives error
```

- Variables defined with `const` keyword cannot be Redeclared, Reassigned and has Block Level Scope.
- Always declare a variable with `const` when you know that the value should not be changed.
- Use `const` when you declare:  
    - A new Array.
    - A new Object.
    - A new Function.
    - A new RegExp.
    - Getting Elements

## Variable let

```js
let x = "Hi";
let y = 100;
let z = 12.3;

x = "Hello"; // Will not give error like "const"
```

- Variables defined with `let` cannot be redeclared, must be declared before use and has block level scope.

### Cannot be redeclared
With `let` you cannot do this.
```js
let x = 10;

let x = 10;
```

With `var` you can
```js
var x = 100;
var x = 100;
```

### Block Scope
 
- Variables declared inside a `{ }` block cannot be accessed from outside the block.

- Variables declared inside a `{ }` blocks are known as **Function Scope**. Variables declared outside a block is known as **Global Scope**.

```js
{
    let x = 10;
}
// x cannot be used here
```
- Variables declared with the `var` keyword can **NOT** have block scope.
- Variables declared inside a `{ }` block can be accessed from outside the block.
```js
{
    var x = 100;
}
// x can be used here
```

### Redeclaring variables

Redeclaring a variable using the `var` keyword can impose problems.   
Redeclaring a variable inside a block will also redeclare the variable outside the block:


```js
var x = 10;
// Here x is 10

{
var x = 2;
// Here x is 2
}

// Here x is 2
```

Redeclaring a variable using the `let` keyword can solve this problem.   
Redeclaring a variable inside a block will not redeclare the variable outside the block:
```js
let x = 10;
// Here x is 10

{
let x = 2;
// Here x is 2
}

// Here x is 10
```

### Redeclaring

With `let` redeclaring in a same block is **NOT** allowed:
```js
var x = 2;   // Allowed
let x = 3;   // Not allowed

{
let x = 2;   // Allowed
let x = 3;   // Not allowed
}

{
let x = 2;   // Allowed
var x = 3;   // Not allowed
}
```

Redeclaring a variable with `let`, in another block, **IS** allowed:
```js
let x = 2;   // Allowed

{
let x = 3;   // Allowed
}

{
let x = 4;    // Allowed
}
```

## var VS let

1. `var` is globally scoped variable while `let` is block scoped variable.
2. `var` can be updated and redeclared.
3. `let` can be updated but cannot be redeclared.
4. `const` can neither be updated nor be redeclared.
5. `var` variables are initialized with undefined whereas `let` and `const` variables are not initialized.
6. `const` must be initialized during declaration, unlike `let` and `var`.

## Common Programming Case Types

- camelCase
- kebab-case
- snake_case
- PascalCase
- MACRO_CASE
- Train-Case
- flatcase
- UPPERFLATCASE
- camel_Snake_Case

## Links

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/pranjalagupte)  
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/pranjalagupte/)

## Authors
 - [@PranjalGupte](https://github.com/Pranjal-Gupte/)