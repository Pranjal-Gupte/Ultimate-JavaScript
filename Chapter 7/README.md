# Chapter 7 - Loops and Functions

We use loops program repeated actions. For example - If you are given a task of building numbers from 1 to 100, it will be very hectic to do it manually, loops help us automate such process.

## Types of loops

We have five types of loops in JavaScript. These are:

| Loop          | Description                                 |
| ------------- | ------------------------------------------- |
| for loop      | loops a block of code number of times       |
| for in loop   | loops through the keys of an object         |
| for of loop   | loops through the values of an object       |
| while loop    | loops a block on a specific condition       |
| do-while loop | while loop variant which runs at least once |

## The for loop

The syntax of a for loop looks something like this,

```js
for (initialExpression; condition; updateExpression) {
    // code to be executed
}
```

1. The **initialExpression** initializes and/or declares variables and executes only once.
1. The **condition** is evaluated.
    - If the condition is `false`, the `for` loop is terminated.
    - If the condition is `true`, the block of code inside of the `for` loop is executed.
1. The **updateExpression** updates the value of **initialExpression** when the condition is `true`.
1. The **condition** is evaluated again. This process continues until the condition is `false`.

### Example: Display Numbers from 1 to 5

```js
// program to display numbers from 1 to 5
const n = 5;

// looping from i = 1 to 5
// in each iteration, i is increased by 1
for (let i = 1; i <= n; i++) {
    console.log(i);     // printing the value of i
}
```

Here is how this program works.

| Iteration | Variable                 | Condition: i <= n | Action                                       |
| --------- | ------------------------ | ----------------- | -------------------------------------------- |
| 1st       | `i = 1`<br><br>`n = 5`   | `true`            | `1` is printed.<br>`i` is increased to **2** |
| 2nd       | `i = 2`<br><br>`n = 5`   | `true`            | `2` is printed.<br>`i` is increased to **3** |
| 3rd       | `i = 3`<br><br>`n = 5`   | `true`            | `3` is printed.<br>`i` is increased to **4** |
| 4th       | `i = 4`<br><br>`n = 5`   | `true`            | `4` is printed.<br>`i` is increased to **5** |
| 5th       | `i = 5`<br><br>`n = 5`   | `true`            | `5` is printed.<br>`i` is increased to **6** |
| 6th       | `i = 6`<br><br>`n = 5`   | `false`           | The loop is terminated                       |


> **Quick Quiz: Write a sample for loop of your choice**

-----

[![flowChartOfForLoop](https://cdn.programiz.com/sites/tutorial2program/files/javascript-for-loop.png)]()

Flowchart of JavaScript for loop

-----

## The for...in loop

The syntax of for in loop looks like this,

```js
for(key in object) {
    // code to be executed
}
```

In each iteration of the loop, a `key` is assigned to the key variable. The loop continues for all object properties.

> **Note: Once you get the keys, you can easily find their corresponding values.**

### Example 1: Iterate through an Object

```js
const student = {
    name: 'Pranjal',
    class: 10,
    age: 15
}

// using for...in
for (let key in student) {

    // display the properties
    console.log(`${key} => ${student[key]}`); // name => Pranjal class => 10 age => 15
}
```
In the above program, the `for...in` loop is used to iterate over the `student` object and print all its properties.

- The Object key is assigned to the variable `key`.
- `student[key]` is used to access the value of `key`.

### Example 2: Update Values of Properties

```js
const salaries = {
    "Jack": 24000,
    "Bob": 34000,
    "Oggy": 55000
}

// using for...in loop
for (let i in salaries) {

    // add currency symbol
    let salary = "$" + salaries[i];

    // display the values
    console.log(`${i}: ${salary}`); // Jack: $24000 Bob: $34000 Oggy: $55000
}
```

> **Quick Quiz: Write a sample program demonstrating for...in loop.**

> **Note: for...in loop also works with arrays but we don't use it because JavaScript has blessed us with for...of loop.**

## The for...of loop

The syntax of the for...of loop is,

```js
for (element of iterable) {
    // code to be executed
}
```

- iterable - an iterable object (array, set, strings, etc.)
- element - items in the iterable.

In plain English, you can read the above code as: for every element in the iterable, run the body of the loop.

### Example 1: for...of with Arrays

```js
// defining an array
const students = ["John", "Sara", "Jack"];

//using for...of loop
for (let elements of students) {

    // display the value of students(array)
    console.log(elements); // John Sara Jack
}
```

In the above program, the `for...of` loop is used to iterate over the `students` array object and display al its values.

### Example 2: for...of with Strings

```js
// defining a string
const name = "John";

// using for...of loop
for (let i of name) {
    console.log(name); // J o h n
}
```

> **Quick Quiz: Write a sample programs demonstrating for...of loops.**

## for...of Vs for...in

| for...of                                                                  | for...in                                                                                                                       |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| The `for...of` loop is used to iterate through the values of an iterable. | The `for...in` loop is used to iterate through the keys of an object.                                                          |
| The `for...of` loop cannot be used to iterate over an object.             | You can use`for...in` to iterate over an iterable such arrays and strings but you should avoid using `for...in` for iterables. |

## The while loop

The syntax of while loop is:

```js
while(condition) {
    // code to be executed
}
```

1. A `while` loop evaluates the **condition** inside the parentheses `()`.
1. If the **condition** evaluates to `true`, the code inside the `while` loop is executed.
1. The **condition** is evaluated again.
1. The process continues until the **condition** is `false`.
1. When the **condition** evaluates to `false`, the loop stops.
1. If the **condition** never becomes false, the loop will never end and this will crash the runtime.

### Example 1: Display numbers from 1 to 5

```js
// program to display numbers from 1 to 5
// initialize the variable
let i = 1, n = 5;

// while loop from i = 1 to 5
while (i <= n) {
    console.log(i);
    i += 1;
}
/*Output: 
1
2
3
4
5
*/
```

Here is how the program works

| Iteration | Variable           | Condition: i <= n | Action                                         |
| --------- | ------------------ | ----------------- | ---------------------------------------------- |
| 1st       | `i = 1`<br><br>`n = 5` | `true`            | `1` is printed. `i` is increased to **2**. |
| 2nd       | `i = 2`<br><br>`n = 5` | `true`            | `2` is printed. `i` is increased to **3**. |
| 3rd       | `i = 3`<br><br>`n = 5` | `true`            | `3` is printed. `i` is increased to **4**. |
| 4th       | `i = 4`<br><br>`n = 5` | `true`            | `4` is printed. `i` is increased to **5**. |
| 5th       | `i = 5`<br><br>`n = 5` | `true`            | `5` is printed. `i` is increased to **6**. |
| 6th       | `i = 6`<br><br>`n = 5` | `false`           | The loop is terminated.                    |

### Example 2: Sum of Positive Numbers Only

```js
// program to find the sum of positive numbers
// if the user enters a negative numbers, the loop ends
// the negative number entered is not added to sum

let sum = 0;

// take input from the user
let number = parseInt(prompt('Enter a number: '));

while(number >= 0) {

    // add all positive numbers
    sum += number;

    // take input again if the number is positive
    number = parseInt(prompt('Enter a number: '));
}

// display the sum
console.log(`The sum is ${sum}.`);

/*
Output:
Enter a number: 2
Enter a number: 5
Enter a number: 7
Enter a number: 0
Enter a number: -3
The sum is 14.
*/
```

In the above program, the user is prompted to enter a number.   
Here, `parseInt()` is used because `prompt()` takes input from the user as a string. And when numeric strings are added, it behaves as a string. For example, `'2' + '3' = '23'`. So `parseInt()` converts a numeric string to number.   
The `while` loop continues until the user enters a negative number. During each iteration, the number entered by the user is added to the `sum` variable.   
When the user enters a negative number, the loop terminates. Finally, the total sum is displayed.

> **Quick Quiz: Write a sample program demonstrating while loop.** 

-----

[![whileLoopFlowChart](https://cdn.programiz.com/sites/tutorial2program/files/javascript-while-loop.png)]()

-----

## The do...while loop

The syntax of do...while loop is,

```js
do {
    // code do be executed
} while(condition)
```

1. The body of the loop is executed at first. Then the **condition** is evaluated.
1. If the **condition** evaluates to `true`, the body of the loop inside the `do` statement is executed again.
1. The **condition** is evaluated once again.
1. If the **condition** evaluates to `true`, the body of the loop inside the `do` statement is executed again.
1. This process continues until the **condition** evaluates to `false`. Then the loop stops.

> **Note: `do...while` is similar to `while` loop. The only difference is that in `do...while` loop, the body of loop is executed at least once.**

### Example 3: Display Numbers from 1 to 5

```js
// program to display numbers
let i = 1;
const n = 5;

// do...while loop from 1 to 5
do {
    console.log(i);
    i++;
} while(i <= n);
/*
Output:
1
2
3
4
5
*/
```

Here is how the program works

| Iteration | Variable           | Condition: i <= n | Action                                     |
| --------- | ------------------ | ----------------- | ------------------------------------------ |
|           | `i = 1`<br>`n = 5` | not checked       | `1` is printed. `i` is increased to **2**. |
| 1st       | `i = 2`<br>`n = 5` | `true`            | `2` is printed. `i` is increased to **3**. |
| 2nd       | `i = 3`<br>`n = 5` | `true`            | `3` is printed. `i` is increased to **4**. |
| 3rd       | `i = 4`<br>`n = 5` | `true`            | `4` is printed. `i` is increased to **5**. |
| 4th       | `i = 5`<br>`n = 5` | `true`            | `5` is printed. `i` is increased to **6**. |
| 5th       | `i = 6`<br>`n = 5` | `false`           | The loop is terminated.                    |

### Example 2: Sum of Positive Numbers

```js
// to find the sum of positive numbers
// if the user enters negative number, the loop terminates
// negative number is not added to sum

let sum = 0;
let number = 0;

do {
    sum += number;
    number = parseInt(prompt('Enter a number: '));
} while(number >= 0)

console.log(`The sum is ${sum}.`);

/*
Output:
Enter a number: 2
Enter a number: 4
Enter a number: -500
The sum is 6.
*/
```

Here, the `do...while` loop continues until the user enters a negative number. When the number is negative, the loop terminates; the negative number is not added to the `sum` variable.

-----

[![doWhileLoopFlowChart](https://cdn.programiz.com/sites/tutorial2program/files/javascript-do-while-loop.png)]()

-----

## for Vs while Loop

A `for` loop is usually used when the number of iterations is known. For example,

```js
// this loop is iterated 5 times
for (let i = 1; i <=5; ++i) {
   // body of loop
}
```

And `while` and `do...while` loops are usually used when the number of iterations are unknown. For example,

```js
while (condition) {
    // body of loop
}
```

## Functions

A function is a block of code that performs a specific task.   
Suppose you need to create a program to create a circle and color it. You can create two functions to solve this problem:

- A function to draw circle.
- A function to color circle.

Dividing a complex problem into smaller chunks makes your program easy to understand and reusable.   
JavaScript also has a huge number of inbuilt functions. For example, `Math.sqrt()` is a function to calculate the square root of a number.

## Declaring Function

The syntax to declare a function is:

```js
function nameOfFunction() {
    // code to be executed
}
```

- A function is declared using the `function` keyword.
- The basic rules of naming a function are similar to naming a variable. It is better to write a descriptive name for your function. For example, if a function is used to add two numbers, you could name the function`add` or `addNumbers`.
- The body of the function is written in `{}`.

For example,

```js
// declaring a function named greet()
function greet() {
    console.log("Hello there");
}
```

## Calling a Function

In the above program, we have declared a function named `greet()`. To use that function, we need to call it.   
Here's how you can call the above `greet()` function.

```js
// function call
greet();
```

-----

[![workingOfFunctions](https://www.programiz.com/sites/tutorial2program/files/javascript-function-example1.png)]()

Working of a Function

-----

### Example 1: Display Some Text

```js
// program to print a text
// declaring a function
function greet() {
    console.log("Hello there!");
}

// calling the function
greet();

/*
Output: Hello World
*/
```

## Function Parameters

A function can also be declared with parameters. A parameter is a value that is passed when declaring a function.

-----

[![workingOfFunctionsWithParameters](https://www.programiz.com/sites/tutorial2program/files/javascript-function-with-parameter.png)]()

Working of Functions with Parameters

-----

### Example 2: Function with Parameters

```js
// program to print the text
// declaring a function
function greet(name) {
    console.log("Hello " + name + " :)");
}

// variable name can be different
let name = prompt("Enter a name: ");

// calling function
greet(name);

/*
Output:
Enter a name: John Doe
Hello John Doe :)
*/
```

In the above program, the `greet` function is declared with a `name` parameter. The user is prompted to enter a name. Then when the function is called, an argument is passed into the function.

> **Note: When a value is passed when declaring a function, it is called `parameter`. And when the function is called, the value is passed is called `argument`.**

### Example 3: Add Two Numbers

```js
// program to add two numbers using a function
// declaring a function
function add(a, b) {
    console.log(a + b);
}

// calling functions
add(3,4);
add(2,9);

/*
Output:
7
11
*/
```

In the above program, the `add` function is used to find the sum of two numbers.

- The function is declared with two parameters `a` and `b`.
- The function is called using its name and passing two arguments **3** and **4** in one and **2** and **9** in another.

Notice that you can call a function as many times as you want. You can write one function and then call it multiple times with different arguments.

## Function Return

The `return` statement can be used to return the value to a function call.

The `return` statement denotes that the functions has ended. Any code after `return` is not executed.

If nothing is returned, the function returns an `undefined` value.

-----

[![workingOfFunctionWithReturnStatement](https://www.programiz.com/sites/tutorial2program/files/javascript-return-statement.png)]()

Working of Function with return statement

-----

### Example 4: Sum of Two Numbers

```js
// program to add two numbers
// declaring a function
function add(a, b) {
    return a + b;
}

// take input from the user
let number1 = parseFloat(prompt("Enter first number: "));
let number2 = parseFloat(prompt("Enter second number: "));

// calling function
let result = add(number1,number2);

// display the result
console.log("The sum is " + result);

/*
Output:
Enter first number: 3.4
Enter second number: 4
The sum is 7.4
*/
```

In the above program, the sum of the numbers is returned by the function using the `return` statement. And that value is stored in the `result` variable.

## Benefits of using a Function

- Function makes the code reusable. You can declare it once and use it multiple times.
- Function makes the program easier as each small task is divided into a function.
- Function increases readability.

## Function Expressions

In Javascript, functions can also be defined as expressions. For example,

```js
// program to find the square of a number
// function is declared inside the variable
let x = function (num) { return num * num };
console.log(x(4));

// can be used as variable value for other variables
let y = x(3);
console.log(y);

/*
Output:
16
9
*/
```

In the above program, variable `x` is used to store the function. Here the function is treated as an expression. And the function is called using the variable name.

The function above is called an anonymous function.

> **Note: In ES2015(ES6), JavaScript expressions are written as arrow functions.**

## Arrow Function

Arrow function is one of the features introduced in the ES6 version of JavaScript. It allows you to create functions in a cleaner way compared to regular functions. For example,

This function,

```js
// function expression
let x = function(x, y) {
    return x * y;
}
```

can be written as

```js
// using arrow function
let x = (x, y) => x * y;
```

using an arrow function.

## Arrow Function Syntax

The syntax of the arrow function is:

```js
let myFunction = (arg1, arg2, ...argN) => {
    statement(s)
}
```

Here,

- `myFunction` is the name of the function.
- `arg1, arg1, ...argN` are the function arguments.
- `statement(s)` is the function's body.

If the body has single statement or expression, you can write arrow function as follows,

```js
let myFunction = (arg1, arg2, ...argN) => expression
```

> **Fun Fact: `...` is an operator named `spread`. We will use this operator in next chapter. But here we have used it as 'so on...'.**

### Example 1: Arrow Function with No Argument

If a function doesn't take any argument, then you should use empty parentheses. For example,

```js
let greet = () => console.log("Hello");
greet();
```

### Example 2: Arrow Function with One Argument

If a function has only one argument, you can omit the parentheses. For example,

```js
let greet = x = console.log(x);
greet("Hello");
```

### Example 3: Arrow Function as an Expression

You can also dynamically create a function and use it as an expression. For example,

```js
let age = 5;

let welcome = (age < 18) ?
  () => console.log('Baby') :
  () => console.log('Adult');

welcome(); // Baby
```

### Example 4: Multiple Arrow Function

If a function body has multiple statements, you need to put them inside curly brackets `{}`. For example,

```js
let sum = (a, b) => {
    let result = a + b;
    return result;
}

let result1 = sum(5,7);
console.log(result1); // 12
```

## Things You Should Avoid With Arrow Functions

### 1. You should not use arrow function to create methods inside object

```js
let person = {
    name: 'Jack',
    age: 25,
    sayName: () => {

        // this refers to the global .....
        //
        console.log(this.age);
    }
}

person.sayName(); // undefined
```

### 2. You cannot use an arrow function as a constructor.

```js
let Foo = () => {};
let foo = new Foo(); // TypeError: Foo is not a constructor
```

## Links

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/pranjalagupte)  
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/pranjalagupte/)

## Authors

 - [@PranjalGupte](https://github.com/Pranjal-Gupte/)