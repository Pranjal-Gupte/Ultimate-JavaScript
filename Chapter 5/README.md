# Chapter 5 - Type Conversion and Coercion

In programming, type **Conversion** is the process of converting data of one type to another type. For Example: Converting `String` data to `Number`.   
There are two types of type conversion in JavaScript.

- Implicit Conversion - Automatic type conversion.
- Explicit Conversion - Manual Type Conversion

We can convert the following in JavaScript:

- Strings to Numbers
- Numbers to Strings
- Dates to Numbers
- Numbers to Dates
- Booleans to Numbers
- Numbers to Booleans

## JavaScript Implicit Conversion
In certain situations, JavaScript automatically converts one data type to another (to the right type). This is known as implicit conversion.

### Example 1: Implicit Conversion to String
```js
// numeric string used with + gives string type
let result;

result = '3' + 2; 
console.log(result) // "32"

result = '3' + true; 
console.log(result); // "3true"

result = '3' + undefined; 
console.log(result); // "3undefined"

result = '3' + null; 
console.log(result); // "3null"
```

**Note: When a number is added to a string, JavaScript converts the number to a string before concatenation.**

### Example 2: Implicit Conversion to Number

```js
// numeric string used with - , / , * results number type

let result;

result = '4' - '2'; 
console.log(result); // 2

result = '4' - 2;
console.log(result); // 2

result = '4' * 2;
console.log(result); // 8

result = '4' / 2;
console.log(result); // 2
```

### Example 3: Non-numeric String Results to NaN

```js
// non-numeric string used with - , / , * results to NaN

let result;

result = 'hello' - 'world';
console.log(result); // NaN

result = '4' - 'hello';
console.log(result); // NaN
```

### Example 4: Implicit Boolean Conversion to Number

```js
// if boolean is used, true is 1, false is 0

let result;

result = '4' - true;
console.log(result); // 3

result = 4 + true;
console.log(result); // 5

result = 4 + false;
console.log(result); // 4
```

**Note: JavaScript Considers 0 as `false` and all non-zero number as `true`. And, if `true` is converted to number, the result is always 1.**

### Example 5: null Conversion to Number

```js
// null is 0 when used with number
let result;

result = 4 + null;
console.log(result);  // 4

result = 4 - null;
console.log(result);  // 4
```

### Example 6: undefined used with number, boolean or null

```js
// Arithmetic operation of undefined with number, boolean or null gives NaN

let result;

result = 4 + undefined;
console.log(result);  // NaN

result = 4 - undefined;
console.log(result);  // NaN

result = true + undefined;
console.log(result);  // NaN

result = null + undefined;
console.log(result);  // NaN
```

## JavaScript Explicit Conversion

You can also convert one data type to another as per your needs. The type conversion that you do manually is known as explicit type conversion.   
In JavaScript, explicit type conversions are done using built-in methods. Here are some common methods of explicit conversions.

### 1. Convert to Number Explicitly

To convert numeric strings and boolean values to numbers, you can use `Number()`. For example, 
```js
let result;

// string to number
result = Number('324');
console.log(result); // 324

result = Number('324e-1')  
console.log(result); // 32.4

// boolean to number
result = Number(true);
console.log(result); // 1

result = Number(false);
console.log(result); // 0
```

In JavaScript, empty strings and `null` values returns 0, For example,

```js
let result;
result = Number(null);
console.log(result);  // 0

let result = Number(' ')
console.log(result);  // 0
```

If a string is an invalid number, the result will be `NaN`. For example,

```js
let result;
result = Number('hello');
console.log(result); // NaN

result = Number(undefined);
console.log(result); // NaN

result = Number(NaN);
console.log(result); // NaN
```

> **Note: You can also generate numbers from strings using `parseInt()`, `parseFloat()`, unary operator `+` and `Math.floor()`. For example,**
>
> ```js
> let result;
> result = parseInt('20.01');
> console.log(result); // 20
>
> result = parseFloat('20.01');
> console.log(result); // 20.01
>
> result = +'20.01';
> console.log(result); // 20.01
>
> result = Math.floor('20.01');
> console.log(result); // 20
> ```

### 2. Convert to String Explicitly

To convert other data types to strings, you can use either `String()` or `toString()`. For example, 

```js
//number to string
let result;
result = String(324);
console.log(result);  // "324"

result = String(2 + 4);
console.log(result); // "6"

//other data types to string
result = String(null);
console.log(result); // "null"

result = String(undefined);
console.log(result); // "undefined"

result = String(NaN);
console.log(result); // "NaN"

result = String(true);
console.log(result); // "true"

result = String(false);
console.log(result); // "false"

// using toString()
result = (324).toString();
console.log(result); // "324"

result = true.toString();
console.log(result); // "true"
```

> **Note: `String()` takes `null` and `undefined` and converts them to string. However, `toString()` gives error when `null are passed`.**

### 3. Convert to Boolean Explicitly

To convert other data types to a boolean, you can use `Boolean()`. In JavaScript, `undefined`, `null`, `0`, `NaN`, `""` converts to `false`. For example,

```js
let result;
result = Boolean('');
console.log(result); // false

result = Boolean(0);
console.log(result); // false

result = Boolean(undefined);
console.log(result); // false

result = Boolean(null);
console.log(result); // false

result = Boolean(NaN);
console.log(result); // false
```

All other values give `true`. For example, 

```js
result = Boolean(324);
console.log(result); // true

result = Boolean('hello');
console.log(result); // true

result = Boolean(' ');
console.log(result); // true
```

## JavaScript Type Conversion Table

The table shows the conversion of different values to String, Number, and Boolean in JavaScript.

| Value       | String Conversion | Number Conversion | Boolean Conversion |
| ----------- | ----------------- | ----------------- | ------------------ |
| 1           | "1"               | 1                 | `true`             |
| 0           | "0"               | 0                 | `false`            |
| "1"         | "1"               | 1                 | `true`             |
| "0"         | `"0"`             | 0                 | `true`             |
| "ten"       | `"ten"`           | `NaN`             | `true`             |
| `true`      | "true"            | 1                 | `true`             |
| `false`     | "false"           | 0                 | `false`            |
| `null`      | "null"            | 0                 | `false`            |
| `undefined` | "undefined"       | `NaN`             | `false`            |
| ''          | ""                | 0                 | `false`            |
| ' '         | " "               | 0                 | `true`             |

You will learn about the conversion of objects and arrays to other data types in later tutorials.

## Links

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/pranjalagupte)  
[![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/pranjalagupte/)

## Authors
 - [@PranjalGupte](https://github.com/Pranjal-Gupte/)