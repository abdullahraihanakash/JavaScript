# JavaScript A to Z — Complete Learning & Revision Notes

> A beginner-friendly JavaScript guide, practical course, and quick revision reference. Learn the fundamentals step by step, practise with examples, and return to any section whenever you need a reminder.

JavaScript (JS) is a programming language used to create interactive websites, web applications, servers, command-line tools, and more. It runs in browsers and in environments such as [Node.js](https://nodejs.org/).

**Who is this guide for?** Complete beginners, students, and developers who want one organised place to learn and revise JavaScript.

**How to use this guide:** Read the sections in order, type every example yourself, change the values, predict the output, and practise without looking at the solution. Do not try to memorise everything in one day.

---

## Table of Contents

- [1. JavaScript at a Glance](#1-javascript-at-a-glance)
- [2. Set Up Your Environment](#2-set-up-your-environment)
- [3. Your First JavaScript Program](#3-your-first-javascript-program)
- [4. Syntax, Statements, and Comments](#4-syntax-statements-and-comments)
- [5. Variables: `let`, `const`, and `var`](#5-variables-let-const-and-var)
- [6. Data Types](#6-data-types)
- [7. Type Conversion and Type Coercion](#7-type-conversion-and-type-coercion)
- [8. Operators](#8-operators)
- [9. Strings and Template Literals](#9-strings-and-template-literals)
- [10. Numbers and Math](#10-numbers-and-math)
- [11. Conditional Statements](#11-conditional-statements)
- [12. Loops and Iteration](#12-loops-and-iteration)
- [13. Functions](#13-functions)
- [14. Scope, Hoisting, and Closures](#14-scope-hoisting-and-closures)
- [15. Arrays](#15-arrays)
- [16. Array Methods: `map`, `filter`, and `reduce`](#16-array-methods-map-filter-and-reduce)
- [17. Objects](#17-objects)
- [18. Destructuring, Spread, and Rest](#18-destructuring-spread-and-rest)
- [19. `this`, `call`, `apply`, and `bind`](#19-this-call-apply-and-bind)
- [20. Useful Built-in Objects](#20-useful-built-in-objects)
- [21. Error Handling and Debugging](#21-error-handling-and-debugging)
- [22. The DOM: JavaScript and HTML](#22-the-dom-javascript-and-html)
- [23. Events and Event Handling](#23-events-and-event-handling)
- [24. Forms and User Input](#24-forms-and-user-input)
- [25. Browser Storage](#25-browser-storage)
- [26. JSON and Working with APIs](#26-json-and-working-with-apis)
- [27. Asynchronous JavaScript](#27-asynchronous-javascript)
- [28. Promises](#28-promises)
- [29. `async` and `await`](#29-async-and-await)
- [30. The Event Loop](#30-the-event-loop)
- [31. JavaScript Modules](#31-javascript-modules)
- [32. JavaScript with Node.js](#32-javascript-with-nodejs)
- [33. Object-Oriented Programming](#33-object-oriented-programming)
- [34. Functional Programming Concepts](#34-functional-programming-concepts)
- [35. Maps, Sets, Iterators, and Generators](#35-maps-sets-iterators-and-generators)
- [36. Regular Expressions](#36-regular-expressions)
- [37. Dates and Internationalisation](#37-dates-and-internationalisation)
- [38. Clean Code, Performance, and Security](#38-clean-code-performance-and-security)
- [39. Common JavaScript Mistakes](#39-common-javascript-mistakes)
- [40. Practice Problems](#40-practice-problems)
- [41. Mini Project Roadmap](#41-mini-project-roadmap)
- [42. Quick Revision Cheat Sheet](#42-quick-revision-cheat-sheet)
- [43. Frequently Asked Questions](#43-frequently-asked-questions)
- [44. Recommended Learning Resources](#44-recommended-learning-resources)

---

## 1. JavaScript at a Glance

### What is JavaScript?

JavaScript is a high-level, dynamically typed, multi-paradigm programming language. It is best known for adding behaviour and interactivity to websites, but it is also used outside browsers.

### What can JavaScript do?

- Make buttons, menus, tabs, and forms interactive.
- Update webpage content without reloading the page.
- Validate user input.
- Communicate with APIs and servers.
- Build frontend applications and backend services.
- Create command-line tools, automation, and desktop or mobile applications with suitable platforms.

### HTML vs CSS vs JavaScript

| Technology | Main responsibility | Simple example |
|---|---|---|
| HTML | Structure and content | A button exists on the page |
| CSS | Appearance and layout | The button is blue and rounded |
| JavaScript | Behaviour and logic | Clicking the button changes a message |

### JavaScript vs Java

JavaScript and Java are different programming languages. Their names are similar, but their design, runtime, and ecosystems are different.

### ECMAScript

ECMAScript (often abbreviated ES) is the language specification that JavaScript implementations follow. You will see names such as ES6 / ES2015, ES2020, and ES2024 when reading about language features.

---

## 2. Set Up Your Environment

You can write JavaScript in a browser or run it with Node.js.

### Option A: Browser console

1. Open Chrome, Edge, or another modern browser.
2. Open Developer Tools (`F12` or `Ctrl + Shift + I`).
3. Select the **Console** tab.
4. Type JavaScript and press Enter.

```js
console.log("Hello, JavaScript!");
```

### Option B: VS Code and Node.js

1. Install [Visual Studio Code](https://code.visualstudio.com/).
2. Install the current supported [Node.js](https://nodejs.org/) release for your operating system.
3. Open a project folder in VS Code.
4. Create a file named `app.js`.
5. Open the VS Code terminal and run:

```bash
node app.js
```

Check your installed versions:

```bash
node --version
npm --version
```

### Browser JavaScript vs Node.js

| Browser | Node.js |
|---|---|
| Runs inside a web browser | Runs outside the browser |
| Can access the DOM (`document`) | Does not provide a webpage DOM by default |
| Uses browser APIs such as `localStorage` | Provides APIs such as `fs`, `path`, and `process` |
| Commonly used for frontend development | Commonly used for backend tools and servers |

The core JavaScript language is shared, but browser and Node.js environments provide different APIs.

---

## 3. Your First JavaScript Program

```js
// Display a message in the console.
console.log("Hello, world!");

// Store two numbers.
const firstNumber = 10;
const secondNumber = 20;

// Calculate and display their sum.
const total = firstNumber + secondNumber;
console.log(total); // 30
```

### Ways to display information

```js
console.log("Console message");
console.error("Something went wrong");
console.warn("This is a warning");
console.table([{ name: "Amina", score: 90 }, { name: "Rafi", score: 85 }]);
```

`console.log()` is a development tool. It does not display text directly on a webpage.

---

## 4. Syntax, Statements, and Comments

### Statements

A statement is an instruction JavaScript can execute.

```js
const name = "Raihan";
let age = 21;
age = age + 1;
console.log(name, age);
```

### Case sensitivity

JavaScript is case-sensitive. `userName`, `username`, and `UserName` are three different identifiers.

### Semicolons

JavaScript can automatically insert semicolons in many situations. Using semicolons consistently can make code easier to read and avoid some automatic-semicolon-insertion surprises.

### Comments

```js
// This is a single-line comment.

/*
  This is a multi-line comment.
  Use it to explain a larger idea.
*/
```

Comments should explain why something is done when the reason is not obvious. Avoid comments that simply repeat the code.

### Naming conventions

Use descriptive names and `camelCase` for variables and functions:

```js
const userEmail = "user@example.com";
function calculateTotalPrice() {
  // Calculate and return a total here.
}
```

Constants that represent fixed configuration values are sometimes written in `UPPER_SNAKE_CASE`, such as `MAX_RETRY_COUNT`.

---

## 5. Variables: `let`, `const`, and `var`

A variable is a named place to store a value.

### `let`

Use `let` when a variable needs to be reassigned.

```js
let score = 10;
score = 15;
console.log(score); // 15
```

### `const`

Use `const` when the variable binding should not be reassigned.

```js
const country = "Bangladesh";
// country = "Japan"; // TypeError: reassignment is not allowed.
```

A `const` object or array can still have its contents changed:

```js
const skills = ["HTML", "CSS"];
skills.push("JavaScript");
console.log(skills); // ["HTML", "CSS", "JavaScript"]

const user = { name: "Raihan" };
user.name = "Akash"; // Allowed: the object itself was not reassigned.
```

### `var`

`var` is the older way to declare variables. It is function-scoped and has different hoisting behaviour. Prefer `const` by default and `let` when reassignment is needed. Learn `var` so you can understand older code.

| Feature | `var` | `let` | `const` |
|---|---|---|---|
| Scope | Function | Block | Block |
| Reassignment | Yes | Yes | No |
| Redeclaration in same scope | Yes | No | No |
| Must be initialised at declaration | No | No | Yes |

**Rule of thumb:** Start with `const`. Change it to `let` only when reassignment is required. Avoid `var` in new code.

---

## 6. Data Types

A data type describes the kind of value a variable holds.

### Primitive types

JavaScript has seven primitive types:

| Type | Example | Description |
|---|---|---|
| String | `"Hello"` | Text |
| Number | `42`, `3.14` | Integers and floating-point numbers |
| BigInt | `12345678901234567890n` | Very large integers |
| Boolean | `true`, `false` | Logical values |
| Undefined | `undefined` | A value has not been assigned |
| Null | `null` | An intentional absence of a value |
| Symbol | `Symbol("id")` | A unique identifier |

```js
const name = "Raihan";       // String
const age = 21;               // Number
const bigNumber = 123n;       // BigInt
const isStudent = true;       // Boolean
let result;                   // Undefined
const selectedItem = null;    // Null
const uniqueId = Symbol("id"); // Symbol
```

### Non-primitive values

Objects, arrays, and functions are objects in the language's type system. Arrays are specialised objects used for ordered collections.

```js
const person = { name: "Raihan", age: 21 };
const numbers = [10, 20, 30];
const greet = function () {
  console.log("Hello!");
};
```

### The `typeof` operator

```js
console.log(typeof "Hello");      // "string"
console.log(typeof 42);            // "number"
console.log(typeof true);          // "boolean"
console.log(typeof undefined);     // "undefined"
console.log(typeof 10n);           // "bigint"
console.log(typeof Symbol("x"));  // "symbol"
console.log(typeof {});            // "object"
console.log(typeof function () {}); // "function"
console.log(typeof null);          // "object" (a historical JavaScript quirk)
```

Use `value === null` to check for `null`. Use `Array.isArray(value)` to check whether a value is an array.

---

## 7. Type Conversion and Type Coercion

**Type conversion** means deliberately changing a value from one type to another.

```js
const ageText = "25";
const ageNumber = Number(ageText);
console.log(ageNumber);        // 25
console.log(typeof ageNumber); // "number"

console.log(String(100));  // "100"
console.log(Boolean(1));    // true
console.log(Boolean(0));    // false
```

Useful conversion functions:

```js
Number("42");       // 42
Number("hello");    // NaN
String(42);          // "42"
Boolean("hello");   // true
parseInt("42px", 10); // 42
parseFloat("3.14kg"); // 3.14
```

**Type coercion** happens when JavaScript automatically converts a value during an operation.

```js
console.log("5" + 2); // "52" (string concatenation)
console.log("5" - 2); // 3 (numeric conversion)
console.log(5 == "5"); // true (loose equality converts types)
console.log(5 === "5"); // false (strict equality checks type and value)
```

Prefer explicit conversion and strict equality (`===` and `!==`) so the result is predictable.

### Truthy and falsy values

A value used in a condition is treated as truthy or falsy.

Falsy values include:

- `false`
- `0`, `-0`, and `0n`
- `""` (empty string)
- `null`
- `undefined`
- `NaN`

Most other values are truthy, including `"0"`, `"false"`, `[]`, and `{}`.

```js
const username = "";
if (username) {
  console.log("A username was provided");
} else {
  console.log("Username is empty");
}
```

---

## 8. Operators

Operators perform actions on values.

### Arithmetic operators

| Operator | Meaning | Example |
|---|---|---|
| `+` | Addition | `5 + 2 // 7` |
| `-` | Subtraction | `5 - 2 // 3` |
| `*` | Multiplication | `5 * 2 // 10` |
| `/` | Division | `5 / 2 // 2.5` |
| `%` | Remainder | `5 % 2 // 1` |
| `**` | Exponentiation | `2 ** 3 // 8` |
| `++` | Increment by one | `count++` |
| `--` | Decrement by one | `count--` |

### Assignment operators

```js
let points = 10;
points += 5; // points = points + 5
points -= 2;
points *= 2;
points /= 2;
points %= 3;
```

### Comparison operators

```js
10 > 5;    // true
10 < 5;    // false
10 >= 10;  // true
10 <= 9;   // false
10 === 10; // true
10 !== 5;  // true
```

### Logical operators

```js
true && true;  // true: AND
true || false; // true: OR
!true;         // false: NOT
```

Logical operators short-circuit: JavaScript may not evaluate the right-hand expression when the left side already determines the result.

### Nullish coalescing (`??`)

Use the right-hand value only when the left-hand value is `null` or `undefined`.

```js
const displayName = null;
console.log(displayName ?? "Guest"); // "Guest"

const quantity = 0;
console.log(quantity ?? 10); // 0
```

### Optional chaining (`?.`)

Safely access a property when an earlier value might be `null` or `undefined`.

```js
const user = { profile: { city: "Dhaka" } };
console.log(user.profile?.city); // "Dhaka"
console.log(user.address?.city); // undefined
```

### Ternary operator

A short conditional expression:

```js
const age = 20;
const message = age >= 18 ? "Adult" : "Minor";
console.log(message);
```

### Operator precedence

When an expression is difficult to read, use parentheses instead of relying on memory of operator precedence.

```js
const result = (2 + 3) * 4; // 20
```

---

## 9. Strings and Template Literals

A string represents text. Use single quotes, double quotes, or backticks.

```js
const firstName = "Raihan";
const language = 'JavaScript';
const message = `I am learning ${language}.`;
console.log(message);
```

Template literals support interpolation and multi-line strings:

```js
const name = "Raihan";
const score = 95;

const resultMessage = `Student: ${name}
Score: ${score}`;
console.log(resultMessage);
```

### Useful string properties and methods

```js
const text = "  Learn JavaScript  ";

text.length;                // Includes spaces
text.trim();                // Removes spaces at both ends
text.toUpperCase();         // Uppercase copy
text.toLowerCase();         // Lowercase copy
text.includes("Java");      // true
text.startsWith("  Learn"); // true
text.endsWith(" ");         // true
text.slice(2, 7);           // Extracts part of a string
text.replace("JavaScript", "JS");
"a,b,c".split(",");         // ["a", "b", "c"]
"hello".at(-1);             // "o"
```

Strings are immutable: string methods return new strings rather than changing the original string.

### Escape characters

```js
console.log("He said, \"Hello!\"");
console.log("First line\nSecond line");
console.log("Column 1\tColumn 2");
```

---

## 10. Numbers and Math

JavaScript uses the `Number` type for ordinary integers and decimal numbers. Floating-point calculations can have small precision differences.

```js
console.log(0.1 + 0.2); // May display 0.30000000000000004
console.log(Number.isInteger(10)); // true
console.log(Number.isNaN(Number("hello"))); // true
console.log(Number.isFinite(100)); // true
console.log((12.345).toFixed(2)); // "12.35" (returns a string)
```

### Useful `Math` methods

```js
Math.round(4.6); // 5
Math.floor(4.9); // 4
Math.ceil(4.1);  // 5
Math.trunc(4.9); // 4
Math.abs(-10);   // 10
Math.max(4, 8, 2); // 8
Math.min(4, 8, 2); // 2
Math.sqrt(25);   // 5
Math.pow(2, 3);  // 8
Math.random();   // A pseudo-random number from 0 (inclusive) to 1 (exclusive)
```

Random integer from `min` to `max`, including both ends:

```js
function randomInteger(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(randomInteger(1, 6)); // Example: a dice roll
```

Do not use `Math.random()` for passwords, security tokens, or other security-sensitive values. Use `crypto.getRandomValues()` in a browser or Node.js crypto APIs where appropriate.

---

## 11. Conditional Statements

Conditional statements let a program make decisions.

### `if`, `else if`, and `else`

```js
const marks = 82;

if (marks >= 80) {
  console.log("A+");
} else if (marks >= 70) {
  console.log("A");
} else if (marks >= 60) {
  console.log("A-");
} else {
  console.log("Keep practising");
}
```

### `switch`

Use `switch` when comparing one expression against several possible values.

```js
const day = "Monday";

switch (day) {
  case "Friday":
    console.log("Weekend is near");
    break;
  case "Monday":
    console.log("Start of the work week");
    break;
  default:
    console.log("Regular day");
}
```

`break` prevents execution from falling through to the next case. Fall-through can be intentional, but use it carefully.

### Ternary expression

```js
const isLoggedIn = true;
const page = isLoggedIn ? "Dashboard" : "Login";
```

Use `if...else` when the logic has multiple steps; use a ternary for a simple value choice.

---

## 12. Loops and Iteration

Loops repeat code while a condition is satisfied or while items remain.

### `for` loop

```js
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

### `while` loop

```js
let count = 1;

while (count <= 5) {
  console.log(count);
  count++;
}
```

### `do...while` loop

The body runs at least once because the condition is checked after the body.

```js
let number = 1;

do {
  console.log(number);
  number++;
} while (number <= 3);
```

### `for...of`

Use `for...of` to loop over values in an iterable, such as an array or string.

```js
const languages = ["HTML", "CSS", "JavaScript"];

for (const language of languages) {
  console.log(language);
}
```

### `for...in`

Use `for...in` to enumerate an object's enumerable property keys. It is usually not the best choice for looping over array values.

```js
const student = { name: "Raihan", age: 21 };

for (const key in student) {
  console.log(key, student[key]);
}
```

### `break` and `continue`

```js
for (let i = 1; i <= 10; i++) {
  if (i === 3) continue; // Skip this iteration.
  if (i === 8) break;    // Stop the loop.
  console.log(i);
}
```

Choose a loop that makes the intention clear. Always make sure a `while` loop can eventually reach its stopping condition.

---

## 13. Functions

A function is a reusable block of code that can receive input, perform a task, and optionally return a value.

### Function declaration

```js
function add(a, b) {
  return a + b;
}

console.log(add(5, 3)); // 8
```

### Function expression

```js
const subtract = function (a, b) {
  return a - b;
};

console.log(subtract(8, 3)); // 5
```

### Arrow function

```js
const multiply = (a, b) => {
  return a * b;
};

// Short form: an expression is returned automatically.
const double = number => number * 2;

console.log(multiply(4, 3)); // 12
console.log(double(5));       // 10
```

Arrow functions do not have their own `this` value. They are useful for callbacks, but they are not a direct replacement for every function declaration or method.

### Parameters and arguments

- **Parameters** are the names written in the function definition.
- **Arguments** are the actual values passed when the function is called.

```js
function greet(name) { // name is a parameter
  return `Hello, ${name}!`;
}

greet("Raihan"); // "Raihan" is an argument
```

### Default parameters

```js
function welcome(name = "Guest") {
  return `Welcome, ${name}!`;
}

console.log(welcome()); // "Welcome, Guest!"
```

### Rest parameters

Rest parameters collect remaining arguments into an array.

```js
function sum(...numbers) {
  return numbers.reduce((total, number) => total + number, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
```

### Return value

`return` sends a value back to the caller and ends that function's execution.

```js
function square(number) {
  return number * number;
}

const answer = square(6);
console.log(answer); // 36
```

A function without an explicit `return` returns `undefined`.

### Callback function

A callback is a function passed to another function so that it can be called later.

```js
function processUser(name, callback) {
  const message = `Hello, ${name}`;
  callback(message);
}

processUser("Raihan", function (message) {
  console.log(message);
});
```

### Higher-order function

A higher-order function accepts a function, returns a function, or both.

```js
function runOperation(a, b, operation) {
  return operation(a, b);
}

const answer = runOperation(5, 3, (x, y) => x + y);
console.log(answer); // 8
```

### Recursion

Recursion occurs when a function calls itself. A recursive function needs a base case to stop.

```js
function factorial(number) {
  if (number <= 1) return 1; // Base case
  return number * factorial(number - 1);
}

console.log(factorial(5)); // 120
```

---

## 14. Scope, Hoisting, and Closures

### Scope

Scope determines where a variable can be accessed.

- **Global scope:** available throughout its global environment.
- **Function scope:** available inside the function where it is declared.
- **Block scope:** available inside a block such as `{ ... }` when declared with `let` or `const`.

```js
const globalMessage = "I am outside the function";

function showMessage() {
  const localMessage = "I am inside the function";
  console.log(globalMessage); // Accessible
  console.log(localMessage);  // Accessible
}

showMessage();
// console.log(localMessage); // ReferenceError: not in this scope
```

### Hoisting

Hoisting describes how declarations are processed before code execution. It does **not** mean every variable can safely be used before its declaration.

```js
console.log(greet()); // Works: function declaration is available.

function greet() {
  return "Hello!";
}
```

`var` declarations are hoisted and initialised to `undefined`. `let` and `const` are also hoisted, but cannot be accessed before their declaration is evaluated; that period is called the **Temporal Dead Zone (TDZ)**.

```js
// console.log(score); // ReferenceError: TDZ
let score = 100;
```

### Closure

A closure is created when a function remembers and can access variables from its surrounding lexical scope, even after the outer function has finished running.

```js
function createCounter() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

const counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
console.log(counter()); // 3
```

Closures are useful for private state, callbacks, event handlers, and function factories.

---

## 15. Arrays

An array stores an ordered collection of values. Array indexes start at `0`.

```js
const fruits = ["Apple", "Banana", "Mango"];

console.log(fruits[0]);      // "Apple"
console.log(fruits.length);  // 3
console.log(fruits[2]);      // "Mango"
```

### Add and remove elements

```js
const items = ["Pen", "Book"];

items.push("Bag");      // Add to the end
items.pop();             // Remove from the end
items.unshift("Pencil"); // Add to the beginning
items.shift();           // Remove from the beginning
```

### Other useful methods

```js
const numbers = [10, 20, 30, 40];

numbers.includes(20);       // true
numbers.indexOf(30);        // 2
numbers.slice(1, 3);        // [20, 30], does not modify original
numbers.join(" - ");        // "10 - 20 - 30 - 40"
```

### `splice()` vs `slice()`

- `slice(start, end)` returns a shallow copy of part of an array and does not change the original.
- `splice(start, deleteCount, ...items)` changes the original array by removing, replacing, or inserting items.

```js
const values = [10, 20, 30, 40];
const copiedValues = values.slice(1, 3); // [20, 30]
values.splice(1, 1, 99);                 // values becomes [10, 99, 30, 40]
```

### Sorting numbers

By default, `sort()` compares string representations. Supply a comparator for numeric sorting.

```js
const scores = [40, 100, 5, 25];

scores.sort((a, b) => a - b); // Ascending: [5, 25, 40, 100]
scores.sort((a, b) => b - a); // Descending
```

`sort()` changes the array. To sort a copy, use `[...scores].sort(...)`.

### Copying arrays

```js
const original = [1, 2, 3];
const copy = [...original]; // Shallow copy
copy.push(4);
console.log(original); // [1, 2, 3]
```

A spread copy is shallow: nested objects are still shared references.

---

## 16. Array Methods: `map`, `filter`, and `reduce`

These methods are essential for transforming and analysing data.

### `forEach()` — perform an action for each item

```js
const numbers = [1, 2, 3];

numbers.forEach(number => {
  console.log(number);
});
```

`forEach()` is for side effects. It returns `undefined`; use `map()` when you need a new array.

### `map()` — transform every item

```js
const numbers = [1, 2, 3, 4];

const doubled = numbers.map(number => number * 2);
console.log(doubled); // [2, 4, 6, 8]
```

### `filter()` — keep items that pass a condition

```js
const numbers = [1, 2, 3, 4, 5, 6];

const evenNumbers = numbers.filter(number => number % 2 === 0);
console.log(evenNumbers); // [2, 4, 6]
```

### `reduce()` — combine items into one result

```js
const prices = [100, 200, 300];

const total = prices.reduce((sum, price) => {
  return sum + price;
}, 0); // 0 is the initial accumulator value

console.log(total); // 600
```

### `find()` and `findIndex()`

```js
const users = [
  { id: 1, name: "Amina" },
  { id: 2, name: "Rafi" }
];

const user = users.find(item => item.id === 2);
const index = users.findIndex(item => item.id === 2);
console.log(user);  // { id: 2, name: "Rafi" }
console.log(index); // 1
```

### `some()` and `every()`

```js
const scores = [70, 85, 90];

scores.some(score => score < 75);  // true: at least one matches
scores.every(score => score >= 50); // true: all match
```

### Method comparison

| Method | Main purpose | Returns |
|---|---|---|
| `forEach()` | Run a callback for each item | `undefined` |
| `map()` | Transform each item | New array |
| `filter()` | Keep matching items | New array |
| `reduce()` | Accumulate a result | One accumulated value |
| `find()` | Find the first matching item | Item or `undefined` |
| `findIndex()` | Find first matching position | Index or `-1` |
| `some()` | Check whether any item matches | Boolean |
| `every()` | Check whether all items match | Boolean |

**Remember:** `map()` changes the shape or value of each item; `filter()` changes which items remain; `reduce()` combines items into a result.

---

## 17. Objects

An object stores related data as key-value pairs. A value can be a primitive, array, function, or another object.

```js
const student = {
  name: "Raihan",
  age: 21,
  skills: ["HTML", "CSS", "JavaScript"],
  isLearning: true,
  introduce() {
    return `My name is ${this.name}.`;
  }
};

console.log(student.name);       // Dot notation
console.log(student["age"]);    // Bracket notation
console.log(student.introduce());
```

### Add, update, and delete properties

```js
student.country = "Bangladesh"; // Add
student.age = 22;                // Update
delete student.isLearning;       // Delete
```

### Check whether a property exists

```js
console.log("name" in student); // true
console.log(Object.hasOwn(student, "name")); // true
```

### Object methods

```js
const user = { name: "Amina", age: 20 };

Object.keys(user);   // ["name", "age"]
Object.values(user); // ["Amina", 20]
Object.entries(user); // [["name", "Amina"], ["age", 20]]
```

### Object copying

```js
const originalUser = { name: "Rafi", active: true };
const userCopy = { ...originalUser };

userCopy.name = "Amina";
console.log(originalUser.name); // "Rafi"
```

This is a shallow copy. For nested structures, understand the difference between shallow and deep copying before modifying the copy.

### Nested objects

```js
const profile = {
  name: "Raihan",
  address: {
    city: "Dhaka",
    country: "Bangladesh"
  }
};

console.log(profile.address.city); // "Dhaka"
```

---

## 18. Destructuring, Spread, and Rest

### Array destructuring

```js
const colors = ["Red", "Green", "Blue"];
const [firstColor, secondColor] = colors;

console.log(firstColor);  // "Red"
console.log(secondColor); // "Green"
```

### Object destructuring

```js
const user = { name: "Raihan", age: 21 };
const { name, age } = user;

console.log(name, age);
```

Rename a variable or provide a default:

```js
const { name: userName, country = "Unknown" } = user;
```

### Spread syntax (`...`)

Spread expands an iterable or an object's enumerable properties.

```js
const first = [1, 2];
const second = [3, 4];
const combined = [...first, ...second]; // [1, 2, 3, 4]

const baseUser = { name: "Raihan", role: "student" };
const updatedUser = { ...baseUser, role: "developer" };
```

### Rest syntax (`...`)

Rest collects remaining values. Its meaning depends on where it appears.

```js
const [mainColor, ...otherColors] = ["Red", "Green", "Blue"];
console.log(otherColors); // ["Green", "Blue"]

function showDetails(name, ...hobbies) {
  console.log(name, hobbies);
}

showDetails("Amina", "Reading", "Coding", "Music");
```

**Quick difference:** spread expands; rest collects.

---

## 19. `this`, `call`, `apply`, and `bind`

In a regular function, the value of `this` depends mainly on how the function is called. In an object method call, `this` normally refers to the object before the dot.

```js
const person = {
  name: "Raihan",
  sayName() {
    console.log(this.name);
  }
};

person.sayName(); // "Raihan"
```

Arrow functions do not create their own `this`; they use the surrounding `this` value.

### `call()`

Calls a function with a chosen `this` value and arguments listed separately.

```js
function introduce(city) {
  console.log(`${this.name} lives in ${city}`);
}

const user = { name: "Raihan" };
introduce.call(user, "Dhaka");
```

### `apply()`

Like `call()`, but passes arguments as an array (or array-like value).

```js
introduce.apply(user, ["Dhaka"]);
```

### `bind()`

Returns a new function with a chosen `this` value and optionally pre-filled arguments. It does not call the function immediately.

```js
const introduceUser = introduce.bind(user, "Dhaka");
introduceUser();
```

---

## 20. Useful Built-in Objects

JavaScript includes built-in objects that solve common problems.

### `Array`

Used for ordered collections. See [Arrays](#15-arrays) and [Array methods](#16-array-methods-map-filter-and-reduce).

### `Object`

Used for key-value data and object utilities such as `Object.keys()`, `Object.values()`, and `Object.entries()`.

### `String`

Provides text utilities such as `.includes()`, `.slice()`, `.trim()`, and `.replace()`.

### `Number` and `Math`

Provide numeric checks, conversions, and mathematical operations.

### `JSON`

Converts JavaScript data to and from JSON text.

```js
const user = { name: "Raihan", age: 21 };
const jsonText = JSON.stringify(user); // Object -> JSON string
const parsedUser = JSON.parse(jsonText); // JSON string -> object
```

JSON does not preserve every JavaScript value or type. For example, functions and `undefined` object properties are not represented as ordinary JSON values.

### `Map` and `Set`

See [Maps and Sets](#35-maps-sets-iterators-and-generators).

---

## 21. Error Handling and Debugging

An error is a problem that prevents code from completing normally or makes the result incorrect.

### Common error types

- `SyntaxError`: code cannot be parsed.
- `ReferenceError`: a variable or reference is not available.
- `TypeError`: an operation is not valid for that value.
- `RangeError`: a value is outside an allowed range.

### `try...catch...finally`

```js
try {
  const data = JSON.parse('{"name":"Raihan"}');
  console.log(data.name);
} catch (error) {
  console.error("Could not parse JSON:", error.message);
} finally {
  console.log("This block runs whether an error occurred or not.");
}
```

### Throw your own error

```js
function withdraw(balance, amount) {
  if (amount <= 0) {
    throw new Error("Amount must be greater than zero");
  }

  if (amount > balance) {
    throw new Error("Insufficient balance");
  }

  return balance - amount;
}
```

### Debugging tips

- Read the first error message and the file/line number carefully.
- Check spelling, capitalisation, brackets, quotes, and import paths.
- Use `console.log()` to inspect values and types.
- Use browser Developer Tools or the VS Code debugger.
- Add breakpoints and step through code one line at a time.
- Reproduce the smallest possible example before changing many lines.

---

## 22. The DOM: JavaScript and HTML

The **Document Object Model (DOM)** is the browser's object representation of an HTML document. JavaScript can use browser DOM APIs to read and update the page.

### Connect a JavaScript file to HTML

Use `defer` so the browser parses the HTML before running the external script.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript DOM Example</title>
  <script src="app.js" defer></script>
</head>
<body>
  <h1 id="heading">Hello</h1>
  <p class="description">Learning the DOM</p>
  <button id="change-button">Change heading</button>
</body>
</html>
```

### Select elements

```js
const heading = document.getElementById("heading");
const description = document.querySelector(".description");
const button = document.querySelector("#change-button");
const allParagraphs = document.querySelectorAll("p");
```

- `getElementById()` selects an element by its ID.
- `querySelector()` returns the first element matching a CSS selector.
- `querySelectorAll()` returns a static `NodeList` of matching elements.

### Read and update content

```js
heading.textContent = "JavaScript is working!";
description.textContent = "The paragraph was updated.";
```

Use `textContent` for plain text. Be careful with `innerHTML`: assigning untrusted text to it can create cross-site scripting (XSS) vulnerabilities.

### Change styles and classes

```js
heading.style.color = "blue";
heading.style.fontSize = "32px";

heading.classList.add("active");
heading.classList.remove("hidden");
heading.classList.toggle("highlight");
console.log(heading.classList.contains("active"));
```

Prefer CSS classes for groups of styles instead of adding many individual inline styles from JavaScript.

### Create and add an element

```js
const newParagraph = document.createElement("p");
newParagraph.textContent = "This paragraph was created with JavaScript.";
document.body.append(newParagraph);
```

### Remove an element

```js
newParagraph.remove();
```

### DOM traversal

```js
const parent = heading.parentElement;
const firstChild = document.body.firstElementChild;
const nextElement = heading.nextElementSibling;
```

---

## 23. Events and Event Handling

An event is an action or occurrence that browser code can respond to, such as a click, key press, form submission, or page load.

### Add an event listener

```html
<button id="counter-button">Click me</button>
<p id="counter-value">0</p>
```

```js
const counterButton = document.querySelector("#counter-button");
const counterValue = document.querySelector("#counter-value");
let count = 0;

counterButton.addEventListener("click", () => {
  count++;
  counterValue.textContent = count;
});
```

### The event object

```js
document.addEventListener("keydown", event => {
  console.log("Key pressed:", event.key);
});
```

The browser passes an event object to the listener. It contains useful information such as the event type and target.

### `event.target` vs `event.currentTarget`

- `target` is the element where the event originated.
- `currentTarget` is the element whose listener is currently running.

### Event bubbling

Many events bubble from the originating element through its ancestors. This allows **event delegation**: attach one listener to a parent and handle events from matching children.

```html
<ul id="task-list">
  <li>Learn HTML</li>
  <li>Learn CSS</li>
  <li>Learn JavaScript</li>
</ul>
```

```js
const taskList = document.querySelector("#task-list");

taskList.addEventListener("click", event => {
  if (event.target.matches("li")) {
    event.target.classList.toggle("completed");
  }
});
```

### Useful event methods

```js
form.addEventListener("submit", event => {
  event.preventDefault(); // Prevent the browser's default form submission.
});
```

`stopPropagation()` stops an event from continuing through the propagation path. Use it only when necessary because it can make event flow harder to understand.

---

## 24. Forms and User Input

Forms collect information from users. Read values from the form controls and validate them before using or sending them.

```html
<form id="signup-form">
  <label for="email">Email</label>
  <input id="email" name="email" type="email" required>
  <button type="submit">Sign up</button>
</form>
<p id="form-message" aria-live="polite"></p>
```

```js
const signupForm = document.querySelector("#signup-form");
const emailInput = document.querySelector("#email");
const formMessage = document.querySelector("#form-message");

signupForm.addEventListener("submit", event => {
  event.preventDefault();

  const email = emailInput.value.trim();

  if (!email) {
    formMessage.textContent = "Please enter your email.";
    return;
  }

  formMessage.textContent = `Submitted: ${email}`;
});
```

Browser validation attributes include `required`, `min`, `max`, `minlength`, `maxlength`, and suitable input types such as `email` and `number`.

Client-side validation improves the user experience, but a server must validate data again. Never trust data just because it came from your own form.

---

## 25. Browser Storage

Web Storage lets a browser store small amounts of string data for a website.

### `localStorage`

Data normally remains after the browser is closed and reopened, until it is cleared or removed by the site/user.

```js
localStorage.setItem("username", "Raihan");
const username = localStorage.getItem("username");
localStorage.removeItem("username");
localStorage.clear(); // Removes all keys for this origin.
```

### `sessionStorage`

Stores data for the page session. It is usually cleared when that tab's page session ends.

```js
sessionStorage.setItem("currentStep", "2");
const currentStep = sessionStorage.getItem("currentStep");
```

### Store objects with JSON

Web Storage stores strings, so convert objects to JSON first.

```js
const settings = { theme: "dark", language: "en" };
localStorage.setItem("settings", JSON.stringify(settings));

const savedText = localStorage.getItem("settings");
const savedSettings = savedText ? JSON.parse(savedText) : null;
console.log(savedSettings);
```

Do not store passwords, secret API keys, or sensitive authentication tokens in browser storage. It is accessible to JavaScript running on the same origin and can be exposed by an XSS vulnerability.

---

## 26. JSON and Working with APIs

### What is JSON?

JSON (JavaScript Object Notation) is a text format for exchanging structured data. It looks similar to JavaScript object syntax, but it is a text format with stricter rules.

```json
{
  "name": "Raihan",
  "age": 21,
  "isLearning": true,
  "skills": ["HTML", "CSS", "JavaScript"]
}
```

### Convert between JavaScript and JSON

```js
const user = { name: "Raihan", age: 21 };
const jsonString = JSON.stringify(user);
const userObject = JSON.parse(jsonString);
```

### What is an API?

An API (Application Programming Interface) is a way for software systems to communicate. A web API often accepts HTTP requests and returns data, commonly as JSON.

### Common HTTP methods

| Method | Common purpose |
|---|---|
| `GET` | Read data |
| `POST` | Create or submit data |
| `PUT` | Replace a resource |
| `PATCH` | Partially update a resource |
| `DELETE` | Delete a resource |

### Common HTTP status codes

| Code | Meaning |
|---|---|
| `200` | OK |
| `201` | Created |
| `204` | No Content |
| `400` | Bad Request |
| `401` | Unauthorized / authentication required |
| `403` | Forbidden |
| `404` | Not Found |
| `500` | Internal Server Error |

The exact meaning of a response depends on the API and HTTP semantics. A successful network connection does not necessarily mean the operation succeeded.

---

## 27. Asynchronous JavaScript

Some tasks take time, such as reading a file, waiting for a timer, or requesting information from a server. Asynchronous JavaScript lets a program start such work and continue handling other tasks instead of blocking until the work finishes.

### Synchronous example

```js
console.log("First");
console.log("Second");
console.log("Third");
```

Output:

```text
First
Second
Third
```

### Timer example

```js
console.log("First");

setTimeout(() => {
  console.log("This runs later");
}, 1000);

console.log("Second");
```

Typical output order:

```text
First
Second
This runs later
```

The `setTimeout()` delay is a minimum waiting time, not a guarantee that the callback runs at the exact millisecond.

### `setInterval()`

Runs a callback repeatedly after a specified delay until stopped.

```js
let seconds = 0;

const intervalId = setInterval(() => {
  seconds++;
  console.log(`Seconds: ${seconds}`);

  if (seconds === 5) {
    clearInterval(intervalId);
  }
}, 1000);
```

Use `clearTimeout(id)` to cancel a scheduled timeout and `clearInterval(id)` to stop an interval.

---

## 28. Promises

A Promise represents the eventual result of an asynchronous operation.

A promise has three states:

1. **Pending:** the operation has not completed.
2. **Fulfilled:** the operation completed successfully.
3. **Rejected:** the operation failed.

### Create a Promise

```js
const paymentPromise = new Promise((resolve, reject) => {
  const paymentSuccessful = true;

  if (paymentSuccessful) {
    resolve("Payment successful");
  } else {
    reject(new Error("Payment failed"));
  }
});
```

### Handle a Promise

```js
paymentPromise
  .then(result => {
    console.log(result);
  })
  .catch(error => {
    console.error(error.message);
  })
  .finally(() => {
    console.log("Payment process finished");
  });
```

- `.then()` handles fulfillment and returns a new promise.
- `.catch()` handles rejection (including errors thrown in earlier handlers).
- `.finally()` runs when the promise settles, whether fulfilled or rejected.

### Promise chaining

Return the next value or promise from a `.then()` handler so the next step waits for it.

```js
Promise.resolve(5)
  .then(number => number * 2)
  .then(number => number + 1)
  .then(result => console.log(result)); // 11
```

### Promise utility methods

```js
const first = Promise.resolve("A");
const second = Promise.resolve("B");

Promise.all([first, second]).then(values => console.log(values));
Promise.allSettled([first, second]).then(results => console.log(results));
Promise.race([first, second]).then(result => console.log(result));
Promise.any([first, second]).then(result => console.log(result));
```

- `Promise.all()` fulfils when all fulfil; it rejects if one rejects.
- `Promise.allSettled()` waits until every promise settles.
- `Promise.race()` settles with the first promise that settles.
- `Promise.any()` fulfils with the first fulfilled promise; it rejects with an `AggregateError` if all reject.

---

## 29. `async` and `await`

`async` and `await` provide a readable way to work with promises.

- An `async` function always returns a promise.
- `await` pauses that async function until the awaited promise settles; it does not block the entire JavaScript runtime.

```js
function getUser() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve({ id: 1, name: "Raihan" });
    }, 1000);
  });
}

async function showUser() {
  console.log("Loading user...");

  const user = await getUser();
  console.log(user);
}

showUser();
```

### Error handling with `try...catch`

```js
async function loadData() {
  try {
    const result = await getUser();
    console.log(result);
  } catch (error) {
    console.error("Could not load data:", error.message);
  }
}

loadData();
```

### Sequential vs parallel work

Sequential: the second operation starts after the first finishes.

```js
const firstResult = await firstTask();
const secondResult = await secondTask();
```

Parallel: start independent operations together and wait for both.

```js
const [firstResult, secondResult] = await Promise.all([
  firstTask(),
  secondTask()
]);
```

Use `Promise.all()` when tasks are independent and you need all successful results. Choose another promise utility when its failure behaviour better matches your requirement.

### Fetch data from an API

```js
async function loadPosts() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts");

    // fetch() does not reject just because the server returned 404 or 500.
    if (!response.ok) {
      throw new Error(`HTTP error: ${response.status}`);
    }

    const posts = await response.json();
    console.log(posts);
  } catch (error) {
    console.error("Request failed:", error.message);
  }
}

loadPosts();
```

The browser may restrict cross-origin requests through CORS. The server must allow the requesting origin; client-side JavaScript cannot bypass that server policy.

### Send JSON with `fetch()`

```js
async function createPost() {
  const newPost = {
    title: "Learning JavaScript",
    body: "Practise every day",
    userId: 1
  };

  const response = await fetch("https://jsonplaceholder.typicode.com/posts", {
    method: "POST",
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify(newPost)
  });

  if (!response.ok) {
    throw new Error(`Request failed: ${response.status}`);
  }

  return response.json();
}
```

---

## 30. The Event Loop

JavaScript execution in a typical browser or Node.js environment uses an event loop to coordinate synchronous code and queued callbacks. The host environment provides timers, I/O, and other APIs.

Important terms:

- **Call stack:** tracks the functions currently being executed.
- **Web APIs / host APIs:** browser or Node.js features that handle operations outside ordinary JavaScript execution.
- **Task (macrotask) queue:** holds tasks such as timer callbacks and certain event callbacks.
- **Microtask queue:** holds promise reactions and other microtasks.
- **Event loop:** coordinates when queued work can run after the current JavaScript stack is clear.

Example:

```js
console.log("A");

setTimeout(() => {
  console.log("B: timer callback");
}, 0);

Promise.resolve().then(() => {
  console.log("C: promise callback");
});

console.log("D");
```

Typical browser output:

```text
A
D
C: promise callback
B: timer callback
```

Why? Synchronous code runs first. Promise callbacks are microtasks, which are processed before the next timer task. A zero-millisecond timer still runs later, not immediately.

This is a simplified model. Browsers and Node.js have host-specific details and additional queues/phases.

---

## 31. JavaScript Modules

Modules let you split code into separate files and reuse functionality with `export` and `import`.

### Named export

`math.js`

```js
export const pi = 3.14159;

export function add(a, b) {
  return a + b;
}
```

`app.js`

```js
import { pi, add } from "./math.js";

console.log(pi);
console.log(add(5, 3));
```

### Default export

`greet.js`

```js
export default function greet(name) {
  return `Hello, ${name}!`;
}
```

`app.js`

```js
import greet from "./greet.js";
console.log(greet("Raihan"));
```

A module can have one default export and multiple named exports. Named imports must match exported names unless renamed with `as`.

### Browser setup

```html
<script type="module" src="app.js"></script>
```

Browsers treat scripts with `type="module"` as modules. When testing locally, use a local development server rather than relying on opening every module file directly with `file://`.

### ES Modules in Node.js

Node.js supports both ECMAScript Modules (ESM) and the older CommonJS module system.

A common ESM setup is:

`package.json`

```json
{
  "type": "module",
  "scripts": {
    "start": "node index.js"
  }
}
```

`index.js`

```js
import { add } from "./math.js";
console.log(add(2, 3));
```

Other explicit options:

- `.mjs` marks a file as an ES module.
- `.cjs` marks a file as CommonJS.
- A package's `"type"` field controls how `.js` files in that package scope are interpreted.

### CommonJS overview

```js
// CommonJS export
module.exports = function add(a, b) {
  return a + b;
};

// CommonJS import
const add = require("./math.cjs");
```

Do not mix ESM and CommonJS syntax without understanding the interoperability rules. In an ES module, `require` is not available by default; use `import`, or deliberately use a `.cjs` file for CommonJS code.

---

## 32. JavaScript with Node.js

Node.js is a JavaScript runtime that lets you execute JavaScript outside a web browser. It provides APIs for tasks such as file access, networking, operating-system information, and server creation.

### Run a file

```bash
node app.js
```

### Initialise a Node.js project

```bash
npm init -y
```

This creates a `package.json` file containing project metadata and configuration.

### Install a package

```bash
npm install package-name
```

Install a development-only dependency:

```bash
npm install --save-dev package-name
```

Run a script defined in `package.json`:

```json
{
  "scripts": {
    "start": "node index.js",
    "dev": "node --watch index.js"
  }
}
```

```bash
npm run start
npm run dev
```

The availability of a Node.js command or feature can depend on the Node.js version. Check the official documentation for your installed version.

### Import built-in modules

```js
import path from "node:path";
import { readFile, writeFile } from "node:fs/promises";
```

### Read and write a file (ESM)

```js
import { readFile, writeFile } from "node:fs/promises";

async function fileExample() {
  try {
    await writeFile("message.txt", "Hello from Node.js!", "utf8");

    const content = await readFile("message.txt", "utf8");
    console.log(content);
  } catch (error) {
    console.error("File operation failed:", error.message);
  }
}

fileExample();
```

### Basic HTTP server (ESM)

```js
import http from "node:http";

const server = http.createServer((request, response) => {
  response.writeHead(200, { "Content-Type": "text/plain; charset=utf-8" });
  response.end("Hello from a Node.js server!");
});

server.listen(3000, () => {
  console.log("Server running at http://localhost:3000");
});
```

### Important Node.js concepts

- `process`: information and controls for the current Node.js process.
- `process.env`: environment variables; do not commit secret values to GitHub.
- `process.argv`: command-line arguments.
- `path`: utilities for working with filesystem paths.
- `fs` / `node:fs`: file-system operations.
- `http` / `node:http`: HTTP server and client functionality.
- `Buffer`: work with binary data.
- `events`: event-driven programming utilities.

Node.js is an environment, not a separate programming language. Browser-only globals such as `document` and `localStorage` are not automatically available in Node.js.

---

## 33. Object-Oriented Programming

Object-oriented programming (OOP) organises code around objects that contain data and behaviour.

### Constructor function

```js
function User(name, role) {
  this.name = name;
  this.role = role;
}

const userOne = new User("Raihan", "Developer");
console.log(userOne.name);
```

### Classes

JavaScript classes provide syntax for working with the prototype-based object system.

```js
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  introduce() {
    return `I am ${this.name} and I am ${this.age}.`;
  }
}

const personOne = new Person("Raihan", 21);
console.log(personOne.introduce());
```

### Inheritance with `extends`

```js
class Developer extends Person {
  constructor(name, age, language) {
    super(name, age); // Call the parent constructor first.
    this.language = language;
  }

  code() {
    return `${this.name} writes ${this.language}.`;
  }
}

const developer = new Developer("Amina", 22, "JavaScript");
console.log(developer.introduce());
console.log(developer.code());
```

### Getters and setters

```js
class Product {
  constructor(price) {
    this._price = price;
  }

  get price() {
    return this._price;
  }

  set price(value) {
    if (value < 0) throw new Error("Price cannot be negative");
    this._price = value;
  }
}
```

### Static methods

A static method belongs to the class itself rather than an instance.

```js
class Calculator {
  static add(a, b) {
    return a + b;
  }
}

console.log(Calculator.add(2, 3)); // 5
```

### Private fields

A private field declared with `#` can be accessed only from within the class body.

```js
class BankAccount {
  #balance = 0;

  deposit(amount) {
    if (amount <= 0) throw new Error("Deposit must be positive");
    this.#balance += amount;
  }

  getBalance() {
    return this.#balance;
  }
}
```

### Four commonly taught OOP ideas

- **Encapsulation:** keep related data and behaviour together and control access to internal state.
- **Abstraction:** expose what a user needs while hiding unnecessary implementation detail.
- **Inheritance:** create a class based on another class.
- **Polymorphism:** use a shared interface while different objects provide different behaviour.

Use classes when they make the model clearer. JavaScript also supports composition and functional approaches; OOP is not required for every problem.

---

## 34. Functional Programming Concepts

Functional programming emphasises composing functions and transforming data.

### Pure function

A pure function returns the same output for the same inputs and does not cause observable side effects.

```js
function add(a, b) {
  return a + b;
}
```

### Side effect

A side effect changes something outside the function or interacts with the outside world, such as updating the DOM, writing a file, or making a network request.

### Immutability

Instead of changing an existing array or object, create a new one when that is clearer or safer.

```js
const originalNumbers = [1, 2, 3];
const updatedNumbers = [...originalNumbers, 4];

console.log(originalNumbers); // [1, 2, 3]
console.log(updatedNumbers);  // [1, 2, 3, 4]
```

### Function composition

Combine small functions to create a larger operation.

```js
const double = number => number * 2;
const addFive = number => number + 5;

const result = addFive(double(10));
console.log(result); // 25
```

---

## 35. Maps, Sets, Iterators, and Generators

### `Map`

A `Map` stores key-value pairs. Keys can be values of any type, and entries preserve insertion order.

```js
const userRoles = new Map();

userRoles.set("Raihan", "Developer");
userRoles.set("Amina", "Designer");

console.log(userRoles.get("Raihan")); // "Developer"
console.log(userRoles.has("Amina"));  // true
console.log(userRoles.size);           // 2

userRoles.delete("Amina");
```

### `Set`

A `Set` stores unique values.

```js
const numbers = [1, 2, 2, 3, 3, 4];
const uniqueNumbers = [...new Set(numbers)];

console.log(uniqueNumbers); // [1, 2, 3, 4]
```

Useful methods include `.add()`, `.has()`, `.delete()`, and `.clear()`.

### WeakMap and WeakSet

`WeakMap` and `WeakSet` are specialised collections that hold object references weakly. They are useful for certain memory-sensitive patterns, but they are not enumerable like `Map` and `Set`.

### Iterables and iterators

An iterable provides an iterator, allowing values to be visited one at a time. Arrays and strings are common iterables. `for...of` uses the iterable protocol.

### Generators

A generator function uses `function*` and `yield` to produce values over time.

```js
function* createId() {
  let id = 1;
  while (true) {
    yield id++;
  }
}

const idGenerator = createId();
console.log(idGenerator.next().value); // 1
console.log(idGenerator.next().value); // 2
```

---

## 36. Regular Expressions

A regular expression (RegExp) describes a pattern used to search, match, or replace text.

```js
const message = "JavaScript is powerful";
const pattern = /javascript/i; // i = case-insensitive

console.log(pattern.test(message)); // true
```

### Common pattern symbols

| Symbol | Meaning |
|---|---|
| `\d` | Digit |
| `\w` | Word character (letters, digits, underscore) |
| `\s` | Whitespace |
| `.` | Any character except line terminators by default |
| `+` | One or more |
| `*` | Zero or more |
| `?` | Zero or one (also changes quantifier behaviour) |
| `^` | Start of input/line, depending on flags |
| `$` | End of input/line, depending on flags |
| `[abc]` | One character from the set |
| `{2,5}` | Between two and five repetitions |

### Common RegExp methods

```js
const text = "Order number: 12345";
const orderNumber = text.match(/\d+/);
console.log(orderNumber?.[0]); // "12345"

const cleaned = "a   b".replace(/\s+/g, " ");
console.log(cleaned); // "a b"
```

Regular expressions are useful, but complex patterns can be difficult to maintain. Validate important data on the server too.

---

## 37. Dates and Internationalisation

### Create a date

```js
const now = new Date();
const specificDate = new Date("2026-01-15T10:30:00Z");

console.log(now);
console.log(specificDate.toISOString());
console.log(now.getFullYear());
console.log(now.getMonth()); // Month index starts at 0
console.log(now.getDate()); // Day of the month
```

Be careful with date parsing and time zones. A date-only string and a date-time string can have different time-zone interpretations. Use explicit offsets or UTC when the application needs unambiguous timestamps.

### Format numbers and dates for a locale

```js
const price = new Intl.NumberFormat("en-US", {
  style: "currency",
  currency: "USD"
}).format(1234.5);

const dateText = new Intl.DateTimeFormat("en-GB", {
  dateStyle: "long"
}).format(new Date());

console.log(price);
console.log(dateText);
```

`Intl` helps format dates, numbers, lists, and other information according to locale preferences.

---

## 38. Clean Code, Performance, and Security

### Write readable code

- Use meaningful variable and function names.
- Keep functions focused on one responsibility where practical.
- Prefer `const`; use `let` when reassignment is needed.
- Use strict equality (`===`) in most comparisons.
- Avoid deeply nested conditions when a clear early return is possible.
- Remove unused variables and dead code.
- Format code consistently with a formatter such as Prettier.
- Add comments to explain decisions, assumptions, and non-obvious logic.

### Performance basics

- Choose an appropriate data structure and algorithm.
- Avoid unnecessary DOM updates and repeated expensive work.
- Do not create timers or event listeners you never clean up.
- Measure performance before attempting complex optimisation.
- For large lists, consider pagination or rendering only visible items.

### Security basics

- Never expose private API keys, passwords, or database credentials in frontend JavaScript or a public Git repository.
- Keep secrets in server-side environment variables and use a safe secret-management process.
- Do not place untrusted content into `innerHTML`; prefer `textContent` or safe DOM construction.
- Validate and authorise data on the server; client-side checks can be bypassed.
- Use HTTPS for network communication.
- Be careful when building URLs or SQL queries from untrusted input; use safe APIs and parameterised database queries.
- Do not use `eval()` on untrusted input.
- Keep packages updated and review the dependencies your project installs.

---

## 39. Common JavaScript Mistakes

### 1. Using `=` instead of a comparison

```js
let age = 18;

if (age === 18) {
  console.log("Age is 18");
}
```

`=` assigns a value. `===` compares values and types.

### 2. Forgetting that indexes start at zero

```js
const names = ["Amina", "Rafi", "Raihan"];
console.log(names[0]); // "Amina"
```

### 3. Confusing `const` with a deeply immutable value

`const` prevents reassignment of the binding, not edits to an object's properties or an array's items.

### 4. Forgetting to return from a function

```js
const double = number => number * 2;
```

A function using braces needs an explicit `return` if it should return a value.

### 5. Using `map()` when you only need a side effect

Use `forEach()` or a loop when you do not need a transformed array. Use `map()` when you need the returned array.

### 6. Forgetting the initial value in `reduce()`

Provide an initial accumulator value when possible, especially for sums and other reductions where an empty array is possible.

### 7. Comparing objects by value

Two separately created objects are not equal just because their properties look the same.

```js
console.log({ name: "A" } === { name: "A" }); // false
```

Object equality checks identity/reference, not deep structural equality.

### 8. Expecting `fetch()` to reject for HTTP 404 or 500

Check `response.ok` or `response.status` after `fetch()` resolves.

### 9. Forgetting `await`

Without `await`, an async operation often gives you a Promise instead of the final result.

### 10. Using browser globals in Node.js

`document`, `window`, and `localStorage` are browser APIs. They are not normally available in a Node.js process.

### 11. Mixing CommonJS and ES Modules

In an ES module, use `import` and `export`. Check the file extension and the `"type"` field in `package.json`.

### 12. Assuming `sort()` sorts numbers numerically

Use `.sort((a, b) => a - b)` for ascending numeric order.

### 13. Using `==` without understanding coercion

Prefer `===` to avoid unexpected type conversions.

### 14. Modifying an array while iterating over it

This can cause elements to be skipped or indexes to shift. Consider creating a filtered copy or iterating backwards when removal is required.

### 15. Forgetting that `setTimeout()` is not an exact clock

The callback can run later than the specified delay if the environment is busy or the page is throttled.

---

## 40. Practice Problems

Try to solve these without looking at the examples above. Use `console.log()` to test your answers.

### Beginner

1. Print `Hello, JavaScript!` in the console.
2. Create two variables and print their sum, difference, product, and quotient.
3. Convert the string `"250"` into a number.
4. Check whether a number is even or odd.
5. Find the largest of three numbers.
6. Print the numbers from 1 to 100.
7. Print the multiplication table of a given number.
8. Calculate the sum of all integers from 1 to `n`.
9. Reverse a string.
10. Count the number of vowels in a string.

### Intermediate

11. Find the largest and smallest number in an array.
12. Remove duplicate values from an array.
13. Create a new array containing the square of every number using `map()`.
14. Keep only positive numbers using `filter()`.
15. Calculate an array's total using `reduce()`.
16. Find the first user whose `isActive` property is `true`.
17. Count how many times each word appears in a sentence.
18. Create a function that accepts any number of values and returns their average.
19. Check whether a word is a palindrome.
20. Sort an array of numbers in ascending and descending order.

### Advanced beginner / practical

21. Build a counter with increment, decrement, and reset buttons.
22. Build a to-do list that can add, complete, and delete tasks.
23. Save a theme preference in `localStorage`.
24. Fetch a list of posts from a public API and display the titles.
25. Handle loading, success, empty, and error states in an API-driven page.
26. Create a Promise that resolves after two seconds.
27. Use `async`/`await` and `Promise.all()` to load two independent resources.
28. Create a `BankAccount` class with deposit and withdrawal methods.
29. Create a `Map` to count the frequency of characters in a string.
30. Create a small Node.js HTTP server that returns a JSON response.

### A few sample solutions

**Even or odd**

```js
function checkEvenOrOdd(number) {
  return number % 2 === 0 ? "Even" : "Odd";
}

console.log(checkEvenOrOdd(7)); // "Odd"
```

**Reverse a string**

```js
function reverseString(value) {
  return [...value].reverse().join("");
}

console.log(reverseString("hello")); // "olleh"
```

**Remove duplicates**

```js
function removeDuplicates(values) {
  return [...new Set(values)];
}

console.log(removeDuplicates([1, 2, 2, 3, 3])); // [1, 2, 3]
```

**Find the largest number**

```js
function findLargest(numbers) {
  if (numbers.length === 0) return undefined;
  return Math.max(...numbers);
}

console.log(findLargest([4, 9, 2, 15])); // 15
```

---

## 41. Mini Project Roadmap

Build projects in this order. Each project combines several topics from this guide.

| Level | Project | Concepts to practise |
|---|---|---|
| 1 | Calculator | Variables, functions, operators, conditions |
| 2 | Number guessing game | Loops, conditions, random numbers |
| 3 | Counter app | DOM selection, events, state |
| 4 | Digital clock | `Date`, timers, DOM updates |
| 5 | To-do list | Arrays, objects, DOM, events, storage |
| 6 | Expense tracker | Array methods, forms, objects, local storage |
| 7 | Weather app | `fetch()`, promises, `async`/`await`, error handling |
| 8 | GitHub profile finder | APIs, DOM rendering, loading and error states |
| 9 | Quiz application | Arrays of objects, functions, events, score logic |
| 10 | REST API with Node.js | Modules, HTTP, JSON, validation, file/database work |

For every project:

1. Write down the problem before coding.
2. Break the problem into small steps.
3. Build one feature at a time.
4. Test normal cases and edge cases.
5. Refactor unclear code.
6. Write a README explaining the project, features, setup, and what you learned.

---

## 42. Quick Revision Cheat Sheet

| Need to... | Use |
|---|---|
| Declare a value that should not be reassigned | `const` |
| Declare a value that will be reassigned | `let` |
| Check type | `typeof value` |
| Check an array | `Array.isArray(value)` |
| Compare strictly | `===` |
| Provide a fallback for null/undefined | `value ?? fallback` |
| Safely access a nested property | `user.profile?.name` |
| Repeat a task | `for`, `while`, `for...of` |
| Create a reusable operation | `function` or arrow function |
| Transform array items | `map()` |
| Select array items | `filter()` |
| Combine array items | `reduce()` |
| Find one matching item | `find()` |
| Copy/merge arrays | `[...array]` |
| Copy/merge objects | `{ ...object }` |
| Extract object properties | `const { name } = user` |
| Handle an error | `try...catch` |
| Select a DOM element | `document.querySelector()` |
| Listen for an event | `addEventListener()` |
| Save browser string data | `localStorage.setItem()` |
| Convert object to JSON text | `JSON.stringify()` |
| Convert JSON text to object | `JSON.parse()` |
| Request web data | `fetch()` |
| Wait for a Promise | `await` inside an async function (or supported top-level context) |
| Export/import code | `export` / `import` |
| Read a file in Node.js | `node:fs` or `node:fs/promises` |

### Important method reminders

```js
// Array
array.push(value);
array.pop();
array.includes(value);
array.map(callback);
array.filter(callback);
array.reduce(callback, initialValue);
array.find(callback);
array.slice(start, end);
array.splice(start, deleteCount);

// String
text.trim();
text.toLowerCase();
text.toUpperCase();
text.includes("word");
text.replace("old", "new");
text.split(",");

// Object
Object.keys(object);
Object.values(object);
Object.entries(object);
Object.hasOwn(object, "key");

// Promise
Promise.all(promises);
Promise.allSettled(promises);
Promise.race(promises);
Promise.any(promises);
```

---

## 43. Frequently Asked Questions

### Is JavaScript the same as Java?

No. They are different languages with different ecosystems and use cases.

### Do I need HTML and CSS before JavaScript?

For frontend web development, basic HTML and CSS make DOM and browser examples much easier to understand. You can still learn core JavaScript without them.

### Is JavaScript compiled or interpreted?

The practical answer is that modern JavaScript engines commonly use a combination of interpretation and just-in-time compilation techniques. The exact implementation differs by engine.

### Is JavaScript single-threaded?

A typical JavaScript execution context runs JavaScript on one main thread, while the host environment can perform asynchronous work and provide worker threads or other concurrency facilities. The details depend on the environment.

### What is the difference between `null` and `undefined`?

`undefined` commonly indicates that a value has not been assigned or is absent. `null` is usually assigned intentionally to represent no value.

### What is the difference between `map()` and `forEach()`?

`map()` returns a new array containing transformed values. `forEach()` runs a callback for each item and returns `undefined`.

### What is the difference between `filter()` and `find()`?

`filter()` returns an array of all matching items. `find()` returns the first matching item, or `undefined` if none matches.

### What is the difference between `async/await` and Promises?

`async/await` is syntax built around Promises. It lets asynchronous code be written in a style that is often easier to read.

### What should I learn after JavaScript?

Practise building projects first. Then explore Git/GitHub, HTTP and APIs, Node.js, databases, testing, TypeScript, and a frontend framework such as React when you understand the fundamentals.

---

## 44. Recommended Learning Resources

Use this README as a practical companion, not as a replacement for official documentation. Documentation explains edge cases and newly supported features in more depth.

1. [MDN — JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide) — structured guide to the language.
2. [MDN — JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) — detailed reference for syntax, built-ins, and language behaviour.
3. [MDN — Learn JavaScript](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting) — beginner-focused learning modules.
4. [JavaScript.info](https://javascript.info/) — detailed tutorials with examples.
5. [Node.js Documentation](https://nodejs.org/en/learn) — learn Node.js and server-side JavaScript.
6. [Node.js ECMAScript Modules](https://nodejs.org/api/esm.html) — understand `import`, `export`, and Node.js module configuration.

---

## Final Advice

JavaScript becomes easier when you write code regularly instead of only reading about it. Understand the problem, create a small solution, test it, and improve it. When you forget a concept, return to the relevant section, run the example, and modify it until the behaviour makes sense.

**Learn → Practise → Build → Debug → Revise → Repeat.**

---

*This guide is intended as a living document. As JavaScript and its surrounding platforms evolve, check the official documentation linked above for current browser and Node.js support.*
