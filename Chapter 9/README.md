# Chapter 9 - Conditional Statements and Switch Case

In programming, there may arise situations where you have to run a block of code among more than one alternative. For example, assigning grades **A**, **B**, **C** based on the marks obtained by students.  
In such situations, you can use JavaScript `if...else` statement to create a program that can make decisions.

In JavaScript, there are three forms of the `if...else` statement.

1. **if** Statement.
1. **if...else** Statement.
1. **if...else if...else** Statement.

## JavaScript if Statement

The syntax of the `if` statement is:

```js
if (condition) {
  // code to be executed
}
```

The `if` statement evaluates the condition inside the parenthesis `()`.

1. If the condition is evaluated to `true`, the code inside the body of `if` is executed.
1. If the condition is evaluated to `false`, the code inside the body of `if` is skipped.

> **Note: The code inside `{ }` is the body of `if` statement.**

---

[![workingOfIfStatement](https://cdn.programiz.com/sites/tutorial2program/files/js-if-statement_0.png)]()

<center>Working of the <code>if</code> Statement</center>

---

### Example 1: if Statement

```js
// check if the number is positive

const number = parseInt(prompt("Enter a number: "));

// check if the number is greater than 0
if (number > 0) {
  // the body of the if statement
  console.log("The number is positive");
}
console.log("The if statement is easy");
```

#### Output 1

```
Enter a number: 2
The number is positive
The if statement is easy
```

Suppose the user entered **2**. In this case, the condition `number > 0` evaluates to `true`. And, the body of the `if` statement is executed.

#### Output 2

```
Enter a number: -1
The if statement is easy
```

Suppose the user entered **-1**. In this case, the condition `number > 0` evaluates to `false`. Hence, the body of the `if` statement is skipped.

Since `console.log("The if statement is easy");` is outside the body of the `if` statement, it is always executed.

## JavaScript if...else Statement

An `if` statement can have an optional `else` clause. The syntax of `if...else` statement is:

```js
if (condition) {
  // code to be executed if condition is true
} else {
  // code to be executed if condition is false
}
```

The `if...else` statement evaluates the **condition** inside the parenthesis.

If the condition is evaluated to `true`,

1. The code inside the body of `if` is executed.
1. The code inside the body of `else` is skipped from execution.

If the condition is evaluated to `false`,

1. The code inside the body of `else` is executed.
1. The code inside the body of `if` is skipped from execution.

---

[![workingOfIfElseStatement](https://cdn.programiz.com/sites/tutorial2program/files/js-if-else-statement.png)]()

<center>Working of the <code>if...else</code> Statement</center>

---

### Example 2: if...else Statement

```js
// check if the number is positive or negative/zero

const number = parseInt(prompt("Enter a number: "));

// check if number is greater than 0
if (number > 0) {
  console.log("The number is positive");
}
// if number is not greater than 0
else {
  console.log("The number is either negative or 0");
}

console.log("The if...else statement is easy");
```

#### Output 1

```
Enter a number: 2
The number is positive
The if...else statement is easy
```

Suppose the user entered **2**. In this case, the condition `number > 0` evaluates to `true`. Hence, the body of the `if` statement is executed and the body of the `else` is skipped.

#### Output 2

```
Enter a number: -10
The number is either negative or 0
The if...else statement is easy
```

Suppose the user entered **-10**. In this case, the condition `number > 0` evaluates to `false`. Hence, the body of the `else` statement is executed and the body of the `if` statement is skipped.

## JavaScript if...else if Statement

The `if...else` statement is used to execute a block of code amon two alternatives. However, if you need to make a choice between two or more than two alternatives,<br>The `if...else if...else` statement can be used.

Syntax of the `if...else if...else` statement is:

```js
if (condition1) {
  // code block 1
} else if (condition2) {
  // code block 2
} else {
  // code block 3
}
```

- If **condition1** evaluates to `true`, the **code block 1** is executed.
- If **condition1** evaluates to `false`, then **condition2** is evaluated.
  - If the **condition2** is evaluated to `true`, the **code block 2** is executed.
  - If the **condition2** is evaluated to `false`, the **code block 3** is executed.

---

[![workingOfIfElseIfElseStatement](https://cdn.programiz.com/sites/tutorial2program/files/js-if-else-if-statement_0.png)]()

<center>Working of <code>if...else if...else</code> Statement</center>

---

### Example 3: if...else if...else Statement

```js
// check if the number is positive, negative or zero
const number = parseInt(prompt("Enter a number: "));

// check if the number is greater than 0
if (number > 0) {
    console.log("The number is positive");
}
// check if the number is 0
else if (number == 0) {
    console.log("The number is zero");
}
// check if the number is less than 0
else {
    console.log("The number is nthe condition `number >= 0` evaluates to `true`, and the control of the program goes inside the outer `if` statement.
    egative");
}
console.log("The if...else if...else statement is easy");
```

#### Output

```
Enter a number: 0
The number is 0
The if...else if...else statement is easy
```

Suppose the user entered **0**, then the first test condition `number > 0` evaluates to `false`. Then, the second test condition `number == 0` evaluates to `true` and its corresponding block is executed.

## Nested if...else Statement

You can also write `if...else` statement inside `if...else` statement. This is known as **nested if...else** statement.

### Example 4: Nested if...else Statement

```js
// check if the number is positive, negative or zero
const number = parseInt(prompt("Enter your number: "));

if (number >= 0) {
  if (number == 0) {
    console.log("The number is zero");
  } else {
    console.log("The number is positive");
  }
} else {
  console.log("The number is negative");
}
```

#### Output 5

```
Enter a number: 5
The number is positive
```

Suppose the user entered **5**. In this case, the condition `number >= 0` evaluates to `true`, and the control of the program goes inside the outer `if` statement.  
Then, the test condition, `number == 0`, of the inner `if` statement is evaluated. Since it's `false`, the `else` clause of the inner `if` statement is executed.

> **Note: As you can see, nested `if...else` makes our logic more complicated and we should try avoiding using nested `if...else` whenever possible.**

## Body of if...else with only one statement

If the body of `if...else` has only one statement, we can omit `{ }` in our programs. For example, you can replace...

```js
const number = 2;

if (number > 0) {
  console.log("The number is positive");
} else {
  console.log("The number is negative");
}
```

with

```js
const number = 2;

if (number > 0) console.log("The number is positive");
else console.log("The number is negative");
```

## More on decision making

In certain places, a ternary operator can replace `if...else` statement. If you need to make a choice between more than one alternatives based on a given test condition, the `switch` statement can be used.

## Ternary Operator

A ternary operator evaluates the condition and executes a block of code based on the condition.  
The syntax is:

```js
condition ? expression1 : expression2;
```

The ternary operator evaluates the test condition.

- If the condition is `true`, **expression1** is executed.
- If the condition is `false`, **expression2** is executed.

The ternary operator takes **three** operands, hence, the name is ternary operator. It is also known as conditional operator.

### Example 1: JavaScript Ternary Operator

Let's write a program to determine if a student is passed or failed in exam based on marks obtained.

```js
// program to check pass or fail

let marks = parseInt(prompt("Enter your marks: "));

// check the condition
let result = marks >= 40 ? "Passed" : "Failed";

console.log(`You ${result} the exam`);
```

#### Output 1

```
Enter your marks: 80
You Passed the exam
```

Suppose the user enters **80**. Then the condition `marks >= 40` is checked which evaluates to `true`. So the first expression `Passed` is assigned to the `result` variable.

#### Output 2

```
Enter your marks: 30
You Failed the exam
```

Suppose the user enters **30**. Then the condition `marks >= 40` evaluates to `false`. So the second expression `Failed` is assigned to the `result` variable.

## Ternary Operator Used instead of if...else

In JavaScript, a ternary operator can be used to replace certain types of `if...else` statements. For example...

You can replace this code

```js
// check the age to determine the eligibility of vote
let age = 15;
let result;

if (age >= 18) {
    result = "You are eligible for voting";
} else {
    result = "You are not eligible for voting";
}
console.log(result);
```

with

```js
// ternary operator to check the eligibility of vote
let age = 15;
let result;

result = (age >= 18) ? "You are eligible for voting" : "You are not eligible for voting";
console.log(result);
```

The output of both program will be the same

#### Output

```
You are not eligible for voting
```

## Nested ternary operators

You can also nest one ternary operator as an expression inside another ternary operator. For example,

```js
// program to check if number is positive, negative or zero
let a = 3;
let result = (a >= 0) ? (a == 0 ? "zero" : "positive") : "negative";
console.log(`The number is ${result}.`);
```

#### Output

```
The number is positive.
```

> **Note: You should try to avoid nested ternary operators whenever possible as they make your code hard to read.**

## JavaScript switch Statement

The JavaScript `switch` statement is used in decision making.   
The `switch` statement evaluates an expression and executes the corresponding body that matches the expression's result.   
The syntax of the `switch` statement is:

```js
switch (variable/expression) {
    case value1:
        // body of case 1
        break;
    
    case value2:
        // body of case 2
        break;

    case valueN:
        // body of case N
        break;

    default:
        // body of default
}
```

The `switch` statement evaluates a variable/expression inside parenthesis `()`.

- If the result of the expression is equal to `value1`, its body is executed.
- If the result of the expression is equal to `value2`, its body is executed.
- This process goes on. If there is no matching case, the `default` body executes.

> **Notes:**
> - The `break` statement is optional. If the `break` statement is encountered, the `switch` statement ends.
> - If the `break` statement is not used, the cases after the matching case are also executed.
> - The `default` clause is also optional.

## Flowchart of switch Statement

[![flowchartOfSwitchStatement](https://cdn.programiz.com/sites/tutorial2program/files/javascript-switch-statement.png)]()

<center>Flowchart of JavaScript <code>switch</code> statement</center>

### Example 1: Simple Program Using switch Statement

```js
// program using switch statement
let a = 2;

switch (a) {
    case 1:
        a = 'one';
        break;
    case 2:
        a = 'two';
        break;
    default:
        a = 'not found';
        break;
}

console.log(`The value is ${a}`);
```

#### Output

```
The value is two
```

In the above program, an expression `a = 2` is evaluated with a `switch` statement.

- The **expression's** result is evaluated with `case 1` which results in `false`.
- Then the `switch` statement goes to the second case. Here, the **expression's** result matches with `case 2`. So `The value is two` is displayed.
- The `break` statement terminates the block and control flow of the program jumps to outside of the `switch` block.

### Example 2: Simple Calculator

```js
// the program for simple calculator
let result;

// take the operator
let operator = prompt('Please choose an operator ( either + - * /): ');

// take the operand input
const number1 = parseInt(prompt("Enter your first number: "));
const number2 = parseInt(prompt("Enter your second number: "));

switch (operator) {
    case '+':
        result = number1 + number2;
        console.log(`${number1} + ${number2} = ${result}`);
        break;
    case '-':
        result = number1 - number2;
        console.log(`${number1} - ${number2} = ${result}`);
        break;
    case '*':
        result = number1 * number2;
        console.log(`${number1} * ${number2} = ${result}`);
        break;
    case '/':
        result = number1 / number2;
        console.log(`${number1} / ${number2} = ${result}`);
        break;

    default:
        console.log('Invalid operator');
        break;
}
```

#### Output

```
Please choose an operator ( either + - * /): +
Enter your first number: 4
Enter your second number: 6
4 + 6 = 10
```

In the above program, the user is asked to enter either **+**, **-**, **&#42;**, **/** and two operands. Then, the `switch` statement executes cases based on the user input.

## JavaScript switch With Multiple Choice

In a JavaScript switch statement, cases can be grouped to share the same code.

### Example 3: switch With Multiple Case

```js
// multiple case switch program
let fruit = 'apple';
switch(fruit) {
    case 'apple':
    case 'mango':
    case 'pineapple':
        console.log(`${fruit} is a fruit.`);
        break;
    default:
        console.log(`${fruit} is not a fruit.`);
        break;
}
```

#### Output

```
apple is a fruit.
```

In the above program, multiple cases are grouped. All the grouped cases share the same code.   
If the value of the `fruit` variable had value `mango` or `pineapple`, the output would have been the same.

## break Statement

The `break` statement is used to terminate the loop immediately when it is encountered.

The syntax of the `break` is:

```js
break [label];
```

> **Note: label is optional and rarely used.**

## Working of the break Statement

[![flowchartOfTheBreakStatement](https://cdn.programiz.com/sites/tutorial2program/files/javascript-break-statement.png)]()

### Example 1: break with for Loop

```js
// program to print the value of i
for (let i = 1; i <= 5; i++) {
    // break condition     
    if (i == 3) {
        break;
    }
    console.log(i);
}
```

#### Output

```
1
2
```

In the above program, the `for` loop is used to print the value of `i` in each iteration. The `break` statement is used as:

```js
if (i == 3) {
  break;
}
```

This means when `i` is equal to **3**, the `break` statement terminates the loop. Hence, the output doesn't include values greater than or equal to 3.

> **Note: The `break` statement is almost always used with decision-making statements.**

### Example 2: break with while Loop

```js
// program to find the sum of positive numbers
// if the user enters a negative numbers, break ends the loop
// the negative number entered is not added to sum

let sum = 0, number;

while(true) {

    // take input again if the number is positive
    number = parseInt(prompt('Enter a number: '));

    // break condition
    if(number < 0) {
        break;
    }

    // add all positive numbers
    sum += number;

}

// display the sum
console.log(`The sum is ${sum}.`);
```

#### Output

```
Enter a number: 1
Enter a number: 2
Enter a number: 3
Enter a number: -5
The sum is 6.
```

In the above program, the user enters a number. The `while` loop is used to print the total sum of numbers entered by the user.

Here the `break` statement is used as:

```js
if(number < 0) {
    break;
}
```

When the user enters a negative number, here `-5`, the `break` statement terminates the loop and the control flow of the program goes outside the loop.

Thus, the `while` loop continues until the user enters a negative number.

## break with Nested Loop

When `break` is used inside of two nested loops, `break` terminates the inner loop. For example,

```js
// nested for loops

// first loop
for (let i = 1; i <= 3; i++) {

    // second loop
    for (let j = 1; j <= 3; j++) {
        if (i == 2) {
          break;
        }
        console.log(`i = ${i}, j = ${j}`);
    }
}
```

#### Output

```
i = 1, j = 1
i = 1, j = 2
i = 1, j = 3
i = 3, j = 1
i = 3, j = 2
i = 3, j = 3
```

In the above program, when `i == 2`, `break` statement executes. It terminates the inner loop and control flow of the program moves to the outer loop.

Hence, the value of `i = 2` is never displayed in the output.

## JavaScript Labeled break

When using nested loops, you can also terminate the outer loop with a `label` statement.

However labeled `break` is rarely used in JavaScript because this makes the code harder to read and understand.

## The continue Statement

The `continue` statement is used to skip the current iteration of the loop and the control flow of the program goes to the next iteration.

The syntax of the continue statement is:

```js
continue [label];
```

> **Note: label is optional and rarely used.**

## Working of JavaScript continue Statement

[![workingOfContinueStatement](https://cdn.programiz.com/sites/tutorial2program/files/working-javascript-continue-statement.png)]()

<center>Working of JavaScript Statement<code>continue</code></center>

## continue with for Loop

In a `for` loop, `continue` skips the current iteration and control flow jumps to the **updateExpression**.

### Example 1: Print the value of i

```js
// program to print the value of i
for (let i = 1; i <= 5; i++) {

    // condition to continue    
    if (i == 3) {
        continue;
    }

    console.log(i);
}
```

#### Output

```
1
2
3
4
5
```

In the above program, `for` loop is used to print the value of `i` in each iteration.

Notice the `continue` statement inside the loop.

```js
if(i == 3) {
    continue;
}
```

This means

- When `i`is equal to **3**, the `continue` statement skips the third iteration.
- Then, `i` becomes **4** and the test **condition** and `continue` statement is evaluated again.
- Hence, **4** and **5** are printed in the next two iterations.

> **Note: The `continue` statement is almost always used with decision making statements.**

> **Note: The `break` statement terminates the loop entirely. However, the `continue` statement only skips the current iteration.**

## continue with while Loop

In a `while` loop, `continue` skips the current iteration and control flow of the program jumps back to the `while` condition.

The `continue` statement works in the same way for `while` and `do...while` loops.

### Example 2: Calculate Positive Number

```js
// program to calculate positive numbers only
// if the user enters a negative number, that number is skipped from calculation

// negative number -> loop terminate
// non-numeric character -> skip iteration

let sum = 0;
let number = 0;

while (number >= 0) {

    // add all positive numbers
    sum += number;

    // take input from the user
    number = parseInt(prompt('Enter a number: '));

    // continue condition
    if (isNaN(number)) {
        console.log('You entered a string.');
        number = 0; // the value of number is made 0 again
        continue;
    }

}

// display the sum
console.log(`The sum is ${sum}.`);
```

#### Output

```
Enter a number: 1
Enter a number: 2
Enter a number: hello
You entered a string.
Enter a number: 5
Enter a number: -2
The sum is 8.
```

In the above program, the user enters a number. The `while` loop is used to print the total sum of positive numbers entered by the user.

Notice the use of the `continue` statement.

```js
if (isNaN(number)) {
    continue;
}
```

- When the user enters a non-numeric number/string, the `continue` statement skips the current iteration. Then the control flow of the program goes to the **condition*** of `while` loop.
- When the user enters a number less than **0**, the loop terminates.
- In the above program, `isNaN()` is used to check if the value entered by a user is a number or not.

## continue with Nested Loop

When `continue` is used inside of two nested loops, `continue` skips the current iteration of the inner loop. For example,

```js
// nested for loops

// first loop
for (let i = 1; i <= 3; i++) {

    // second loop
    for (let j = 1; j <= 3; j++) {
        if (j == 2) {
          continue;
        }
        console.log(`i = ${i}, j = ${j}`);
    }
}
```

#### Output

```
i = 1, j = 1
i = 1, j = 3
i = 2, j = 1
i = 2, j = 3
i = 3, j = 1
i = 3, j = 3
```

In the above program, when the `continue` statement executes, it skips the current iteration in the inner loop and control flow of the program moves to the **updateExpression** of the inner loop.

Hence, the value of `j = 2` is never displayed in the output.

## JavaScript Labeled continue

When using nested loops, you can skip the current iteration and the control flow of the program can be passed to a `label` statement's **updateExpression**.

But labeled `continue` is rarely used in JavaScript because this makes the code harder to read and understand.

## Links

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/pranjalagupte)  
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/pranjalagupte/)

## Authors

 - [@PranjalGupte](https://github.com/Pranjal-Gupte/)