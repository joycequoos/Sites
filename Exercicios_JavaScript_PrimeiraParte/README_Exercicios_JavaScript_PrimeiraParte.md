# JavaScript Exercises — Part One

[← Back to Web Development](https://github.com/joycequoos/Development)

Practical exercises on JavaScript fundamentals: data types, operators, strings, booleans, variables, and reserved words. Each folder contains an `index.html` and a `script.js` that can be run directly in the browser.

## Table of Contents

- [01 — Compiling External JavaScript](#01--compiling-external-javascript)
- [02 — Data Types: Number](#02--data-types-number)
- [03 — Arithmetic Operations](#03--arithmetic-operations)
- [04 — Special Numbers](#04--special-numbers)
- [05 — Strings (Part 1)](#05--strings-part-1)
- [06 — Strings (Part 2)](#06--strings-part-2)
- [07 — Boolean](#07--boolean)
- [08 — Boolean Comparisons](#08--boolean-comparisons)
- [09 — Logical Operators](#09--logical-operators)
- [10 — Ternary Operator](#10--ternary-operator)
- [11 — Empty Values (null / undefined)](#11--empty-values-null--undefined)
- [12 — Automatic Type Conversion](#12--automatic-type-conversion)
- [13 — Variables](#13--variables)
- [14 — Variables: var, let, const](#14--variables-var-let-const)
- [15 — Variable Naming Conventions](#15--variable-naming-conventions)
- [16 — Reserved Words](#16--reserved-words)

---

## 01 — Compiling External JavaScript

[View folder](./01_CompilarJS)

First contact with JavaScript running from an external file (`.js`) imported into the HTML, instead of being written directly on the page. Shows basic use of `console.log()` to display messages in the browser console.

```javascript
console.log('External JavaScript.');
```

---

## 02 — Data Types: Number

[View folder](./02_Number)

Use of the `typeof` operator to identify the type of a value — integer, negative number, decimal number, and string — showing how JavaScript classifies each one internally.

```javascript
console.log(typeof 12);      // number
console.log(typeof -12);     // number
console.log(typeof 1.17);    // number
console.log(typeof '1.17');  // string
```

---

## 03 — Arithmetic Operations

[View folder](./03_OperAritimeticas)

The five basic arithmetic operations: addition, subtraction, multiplication, division, and remainder (modulo).

```javascript
console.log(5 + 5);   // addition
console.log(5 * 5);   // multiplication
console.log(5 - 5);   // subtraction
console.log(20 / 2);  // division
console.log(10 % 2);  // remainder (modulo)
```

---

## 04 — Special Numbers

[View folder](./04_SpecialNumber)

Introduction to JavaScript's special numeric values: `Infinity`, `-Infinity`, and `NaN` (*Not a Number* — used when a math operation doesn't result in a valid number).

```javascript
console.log(Infinity);
console.log(-Infinity);
console.log(NaN);
```

---

## 05 — Strings (Part 1)

[View folder](./05_Strings01)

The different ways to declare a string in JavaScript — single quotes, double quotes, nested quotes (one inside the other), and template strings (backticks). Also reinforces that `Infinity` can be treated both as text and as a special numeric value.

```javascript
console.log("This is text");
console.log('This is text');
console.log('This is "some" text');
console.log("This is 'some' text");
console.log(`This is text`);
```

---

## 06 — Strings (Part 2)

[View folder](./06_Strings02)

More advanced string features: line breaks with `\n`, interpolating variables inside template strings (`${}`), and concatenating text with the `+` operator.

```javascript
console.log("This\n text \n breaks\n the line");

let sum = 10 + 10;
console.log(`The sum of 10 + 10 is ${sum}`);

console.log('String' + 'Concatenated');
console.log('String ' + 'Concatenated ' + 'with ' + 'space');
```

---

## 07 — Boolean

[View folder](./07_Boolean)

Introduction to the boolean type (`true` / `false`) and how comparison expressions automatically return a boolean value.

```javascript
console.log(true);
console.log(false);
console.log(5 > 2);    // true
console.log(10 > 100); // false
```

---

## 08 — Boolean Comparisons

[View folder](./08_CompBoolean)

All of JavaScript's comparison operators: greater than, less than, greater than or equal to, less than or equal to, equal (`==`), not equal (`!=`), and strictly equal (`===` — compares both value **and** type).

```javascript
console.log(10 > 5);              // true
console.log(50 < 100);            // true
console.log(100 >= 100);          // true
console.log(100 <= 50);           // false
console.log(50 == 50);            // true
console.log('vinicius' != 'vinicius'); // false
console.log('5' === 5);           // false — different types (string vs number)
console.log(5 === 5);             // true — same value and same type
```

---

## 09 — Logical Operators

[View folder](./09_OpLogicos)

The logical operators `&&` (AND) and `||` (OR) used to combine multiple conditions into a single boolean expression.

```javascript
console.log(10 > 5 && 50 < 100);  // true — both conditions are true
console.log(10 > 5 || 50 > 100);  // true — at least one condition is true
console.log((50 > 4));
```

---

## 10 — Ternary Operator

[View folder](./10_OpTernario)

A shorthand way of writing an `if/else` condition on a single line: `condition ? valueIfTrue : valueIfFalse`.

```javascript
console.log(10 < 7 ? 'right' : 'wrong'); // 'wrong'
```

---

## 11 — Empty Values (null / undefined)

[View folder](./11_empyValues)

Introduction to the values that represent an "absence of data" in JavaScript: `null` (an intentional absence of a value) and `undefined` (a variable that hasn't been defined yet).

```javascript
nameField == null ? 'right' : 'wrong';
```

---

## 12 — Automatic Type Conversion

[View folder](./12_ConversaoAuto)

Demonstrates *type coercion* — when JavaScript automatically converts one data type to another when performing an operation, which can produce unexpected results if not well understood.

```javascript
console.log(10 * null);       // 0 — null becomes 0 in multiplication
console.log("20" - 5);        // 15 — numeric string becomes a number in subtraction
console.log("20" + 5);        // "205" — number becomes a string in concatenation
console.log('five' * 'five'); // NaN — non-numeric text can't become a number
```

---

## 13 — Variables

[View folder](./13_Variavel)

Declaring variables with `let`, reassigning values, using them in math operations, interpolating them in template strings, and declaring multiple variables on a single line.

```javascript
let price = 5;
console.log(price);
console.log(price * price);
console.log(`The value of your purchase was ${price} dollars`);

price = 10;
console.log(`The value of your purchase was ${price} dollars`);

let num1 = 1, num2 = 2, num3 = 3;
console.log(num1 + num2 + num3);
```

---

## 14 — Variables: var, let, const

[View folder](./14_Variaveis-2)

Comparing the three ways of declaring variables in JavaScript: `var` (the old way), `let` (the modern, recommended way), and `const` (for values that cannot be reassigned).

```javascript
var variable1 = 10;
let variable2 = 20;
const variable3 = 30; // cannot be reassigned later

console.log(variable1);
```

---

## 15 — Variable Naming Conventions

[View folder](./15_conversaoVar)

Examples of valid names and best practices for naming variables in JavaScript: using `camelCase`, `$` and `_` as allowed characters, and the rule that names cannot start with a number.

```javascript
let $name = 'vinicius';
let _name = 'vinicius';
let Name = 'Vinicius';
let inputVariableName = 'vinicius';
let name$vinicius = 'vinicius';
```

---

## 16 — Reserved Words

[View folder](./16_palavrasReservadas)

A reference list of JavaScript's reserved words — terms that cannot be used as variable names because they're already part of the language's syntax (`if`, `for`, `function`, `return`, `class`, `let`, `var`, among others).

---

## Key Takeaways

- JavaScript's primitive types (`number`, `string`, `boolean`, `null`, `undefined`) and how to identify them with `typeof`
- Arithmetic, comparison, and logical operators
- Different ways to declare strings, including template strings and interpolation
- Differences between `var`, `let`, and `const`, and why `let`/`const` are preferred today
- Automatic type conversion (coercion) and how it can produce unexpected results
- Good practices for naming variables

**Next steps:** conditional structures (`if/else`, `switch`), loop structures (`for`, `while`), and functions — likely content of [Part Two](https://github.com/joycequoos/Sites/tree/main/Exercicios_JavaScript_SegundaParte).
