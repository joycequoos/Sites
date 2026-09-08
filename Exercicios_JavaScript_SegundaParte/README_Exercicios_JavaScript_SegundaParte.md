# JavaScript Exercises — Part Two

[← Back to Web Development](https://github.com/joycequoos/Development)

Continuation of the [Part One exercises](https://github.com/joycequoos/Sites/tree/main/Exercicios_JavaScript_PrimeiraParte), now moving on to built-in functions, conditional structures, loops, custom functions, scope, closures, recursion, arrays, and objects.

## Table of Contents

**Built-in functions**
- [17 — Structure of a Function](#17--structure-of-a-function)
- [18 — prompt()](#18--prompt)
- [19 — alert()](#19--alert)
- [20 — The Math Object](#20--the-math-object)

**Conditional structures**
- [21 — if](#21--if)
- [22 — if / else](#22--if--else)
- [23 — if / else if / else](#23--if--else-if--else)
- [24 — Nested Conditionals (if inside if)](#24--nested-conditionals-if-inside-if)
- [31 — switch](#31--switch)

**Loops**
- [25 — while](#25--while)
- [26 — do...while](#26--dowhile)
- [27 — for](#27--for)
- [28 — break](#28--break)
- [29 — continue](#29--continue)
- [30 — Incrementing (`+=` and `++`)](#30--incrementing--and-)

**Functions**
- [32 — Defining Functions](#32--defining-functions)
- [33 — More Function Examples](#33--more-function-examples)
- [34 — Function Scope](#34--function-scope)
- [35 — Arrow Function](#35--arrow-function)
- [36 — Optional Arguments](#36--optional-arguments)
- [37 — Default Arguments](#37--default-arguments)
- [38 — Closure](#38--closure)
- [39 — Recursion](#39--recursion)

**Data structures**
- [40 — Array](#40--array)
- [41 — Methods and Objects](#41--methods-and-objects)

---

## 17 — Structure of a Function

[View folder](./17_estruturaFuncoes)

Introduction to the concept of calling (invoking) a function with arguments, even before learning how to create it — showing the basic invocation syntax.

```javascript
functionName(a, b);
```

---

## 18 — prompt()

[View folder](./18_built-in_prompt)

Use of the native `prompt()` function, which opens a dialog box in the browser to capture a text input from the user and store it in a variable.

```javascript
let color = prompt('What is your favorite color?');
console.log(color);
```

---

## 19 — alert()

[View folder](./19_Built-in-alert)

Use of the native `alert()` function to display a message in a pop-up window, combined with variable interpolation in a template string.

```javascript
let name = 'Joyce';
alert(`My name is ${name}`);
```

---

## 20 — The Math Object

[View folder](./20_Built-in_math)

Native methods of the `Math` object for common math operations: `Math.max()` (highest value), `Math.min()` (lowest value), `Math.round()` (rounding), and `Math.ceil()` (rounding up).

```javascript
let number = Math.max(1, 15, 50, 7);   // 50
let number2 = Math.min(1, 15, 50, 7);  // 1
let rounded = Math.round(2.57);        // 3
let roundedUp = Math.ceil(2.27);       // 3
```

---

## 21 — if

[View folder](./21_Estrutura_Condicionais)

Basic `if` conditional structure, testing two variables (`ticket` and `age`) independently, without `else`.

```javascript
let ticket = false;
let age = 20;

if (ticket == true) {
  console.log('Welcome');
}
if (age >= 18) {
  console.log('Go ahead and join the party');
}
```

---

## 22 — if / else

[View folder](./22_Estrutura_Condicional_Else)

Same scenario as the previous exercise, now using `else` to handle the opposite case within the same structure, avoiding repeating the logic in two separate `if` blocks.

```javascript
if (ticket == true) {
  console.log('Welcome');
} else {
  console.log('Go back home');
}
```

---

## 23 — if / else if / else

[View folder](./23_Estrutura_CondicionalElseIF)

Chaining multiple conditions with `else if`, combining logical operators (`&&`) to test more than one variable in the same condition.

```javascript
if (ticket == true && age >= 18) {
  console.log('Welcome, go ahead and join the party.');
} else if (ownersChild) {
  console.log('Go ahead, and say hi to the boss for me.');
} else {
  console.log('Go back home');
}
```

---

## 24 — Nested Conditionals (if inside if)

[View folder](./24_condicional_if_com_if)

An `if` inside another `if`, used to validate a secondary rule (the guest's age) only after the main condition has already been met.

```javascript
if (ticket == true && age >= 18 && hasGuest == true) {
  if (guestAge >= 18) {
    console.log('Welcome, go ahead and join the party.');
  } else {
    console.log("Unfortunately, your guest can't come in.");
  }
} else if (ownersChild) {
  console.log('Go ahead, and say hi to the boss for me.');
} else {
  console.log('Go back home');
}
```

---

## 31 — switch

[View folder](./31_condicional_switch)

The `switch/case` structure as an alternative to a long chain of `else if`, useful when comparing the same variable against several possible values. `break` prevents execution from "falling through" to the next `case`, and `default` covers the case that doesn't match any option.

```javascript
switch (breed) {
  case 'Bigol':
    console.log('The breed is Bigol');
    break;
  case 'Hotweiller':
    console.log('The breed is Hotweiller');
    break;
  default:
    console.log('No breed found');
}
```

---

## 25 — while

[View folder](./25_laco_while)

A `while` loop: repeats a block of code while the condition is true. Used here to count down from 20 to 1.

```javascript
let count = 20;
while (count > 0) {
  console.log(count);
  count = count - 1;
}
```

---

## 26 — do...while

[View folder](./26_laco_do_while)

A variant of `while` in which the block is executed **at least once** before the condition is checked — the difference becomes clear when comparing the file's two examples (counting down and counting up).

```javascript
let count = 10;
do {
  count = count - 1;
  console.log(count);
} while (count > 0);
```

---

## 27 — for

[View folder](./27_laco_for)

The `for` loop, the most commonly used one for repetitions with a fixed number of steps. The second example shows the most common real-world use: iterating over an array using the index (`i`) and the `.length` property.

```javascript
for (let i = 0; i < 10; i = i + 1) {
  console.log(i);
}

let names = ['Vinicius', 'João', 'Andressa', 'Ricardo'];
for (let i = 0; i < names.length; i = i + 1) {
  console.log(names[i]);
}
```

---

## 28 — break

[View folder](./28_break)

The `break` keyword stops the loop completely as soon as the condition is met — here, the loop stops the moment `i` reaches 5.

```javascript
for (let i = 0; i <= 10; i = i + 1) {
  if (i == 5) {
    console.log('Loop stopped');
    break;
  }
  console.log(i);
}
```

---

## 29 — continue

[View folder](./29_continue)

The `continue` keyword skips only the current iteration and moves on to the next one, without stopping the entire loop — unlike `break`.

```javascript
for (let i = 0; i <= 10; i = i + 1) {
  if (i == 7) {
    console.log('We skipped: ' + i);
    continue;
  }
  console.log(i);
}
```

---

## 30 — Incrementing (`+=` and `++`)

[View folder](./30_Incrementacao)

Two equivalent ways to increment a variable on each pass through the loop: `i += 1` (add and reassign) and `i++` (the increment operator, a shorter and more common form).

```javascript
for (let i = 0; i < 10; i += 1) { console.log(i); }
for (let i = 0; i < 10; i++) { console.log(i); }
```

---

## 32 — Defining Functions

[View folder](./32_Definindo_funcao)

Three ways to declare and use functions: a function with no return value (just performs an action), a function with `return` (gives back a value that can be used later), and an anonymous function assigned to a constant (function expression).

```javascript
function printConsoleMessage() {
  console.log('This is a function');
}
printConsoleMessage();

function sum(a, b) {
  return a + b;
}
console.log(sum(1, 5));

const registerUser = function (name) {
  console.log(name);
};
registerUser('Josi');
```

---

## 33 — More Function Examples

[View folder](./33_MaisFuncao)

Two more elaborate functions: one that validates a condition (legal age) and another that combines a function with a `for` loop to generate a number's multiplication table.

```javascript
function verifyAge(number) {
  if (number >= 18) {
    console.log('You are already an adult');
  } else {
    console.log('You are still a child');
  }
}
verifyAge(15);

function multiplicationTable(number) {
  for (let i = 1; i <= 10; i++) {
    console.log(`${number} X ${i} = ${number * i}`);
  }
}
multiplicationTable(8);
```

---

## 34 — Function Scope

[View folder](./34_Escopo_Funcao)

Demonstrates variable scope: a global variable (`number = 100`), a local variable with the same name inside a function (which doesn't conflict with the global one), and a block-scoped variable inside an `if`.

```javascript
let number = 100; // global variable

function numberFn() {
  let number = 350; // local variable, same name, different scope
  console.log(number);
}
numberFn();

if (1 == 1) {
  let number = 1000; // scope restricted to the if block
  console.log(number);
}
```

---

## 35 — Arrow Function

[View folder](./35_Arrow_Function)

A modern, shorter syntax for writing functions (`=>`), assigned to a constant — an alternative to the traditional functions seen in exercise 32.

```javascript
const animal = (name) => {
  console.log(name);
};
animal('Dog');

const sum = (number) => {
  console.log(number + 5);
};
sum(10);
```

---

## 36 — Optional Arguments

[View folder](./36_ArgumentosOpcionais)

Manual argument validation: the function checks whether any parameter was not passed (`undefined`) before running the main logic.

```javascript
const vehicle = (name, brand) => {
  if (name == undefined || brand == undefined) {
    console.log('Both arguments must be provided.');
  } else {
    console.log(name, brand);
  }
};
vehicle('c4 Pallas'); // brand was not provided
```

---

## 37 — Default Arguments

[View folder](./37_Argumentos_Default)

JavaScript's native way of setting a default value for a parameter, used automatically when the argument is not provided in the function call.

```javascript
function createRouterLogin(username, password = 'hjuioplkn') {
  console.log(username, password);
}
createRouterLogin('Josi'); // uses the default password
```

---

## 38 — Closure

[View folder](./38_closure)

A function that returns another function, "storing" (closing over) the value of the outer parameter even after the outer function has already finished executing — this is the basis of the *closure* concept in JavaScript.

```javascript
function storeSum(x) {
  return (y) => x + y;
}

let sum1 = storeSum(10);
console.log(sum1(5)); // 15 — "remembers" that x = 10
```

---

## 39 — Recursion

[View folder](./39_recursion)

A function that calls itself until it reaches a stopping condition — here, it decrements the number until it finds an even value.

```javascript
function returnEvenNumber(number) {
  if (number % 2 == 0) {
    console.log('The number is even: ' + number);
  } else {
    console.log(number);
    returnEvenNumber(number - 1); // recursive call
  }
}
returnEvenNumber(39);
```

---

## 40 — Array

[View folder](./40_Array)

Creating arrays and accessing their elements by index — including the common pattern of accessing the last element with `array.length - 1`.

```javascript
const namesArray = ['Josi', 'Leandro', 'Debi', 'Tinho'];

console.log(namesArray[1]);                    // 'Leandro'
console.log(namesArray[namesArray.length - 1]); // 'Tinho' — last element
```

---

## 41 — Methods and Objects

[View folder](./41_Metodo)

Two concepts in the same exercise: an **array method** (`toLocaleUpperCase()`, which turns a string into uppercase) and a **literal object**, with properties (`breed`, `legs`, `illness`, `color`) and its own method (`bark()`).

```javascript
const animalArray = ['Dog', 'Bird', 'Cat'];
console.log(animalArray[2].toLocaleUpperCase()); // 'CAT'

const Dog = {
  breed: 'Labrador',
  legs: 4,
  illness: false,
  color: 'White',
  bark() {
    console.log('Woof Woof');
  },
};

console.log(Dog.breed);
Dog.bark();
```

---

## Key Takeaways

- Native browser functions: `prompt()`, `alert()`, and the `Math` object
- Complete conditional structures: `if`, `if/else`, `else if`, nested conditionals, and `switch`
- Loops: `while`, `do...while`, `for`, and flow control with `break` and `continue`
- Function declarations (traditional, function expression, and arrow function)
- Variable scope (global, function, and block)
- Intermediate concepts: default/optional arguments, closures, and recursion
- Arrays and objects: index access, string methods, and literal objects with their own properties and methods

**Next steps:** more advanced array methods (`map`, `filter`, `reduce`, `forEach`), DOM manipulation, and events — to connect JavaScript logic with real interactions on the page.
