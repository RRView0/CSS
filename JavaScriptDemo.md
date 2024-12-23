# JavaScript
## 1. Introduction to JavaScript

### Subtopics:
- What is JavaScript?
- Features of JavaScript
- Setting up JavaScript in HTML

### Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Example</title>
</head>
<body>
  <h1>Welcome to JavaScript</h1>
  <script>
    console.log('Hello, World!');
  </script>
</body>
</html>
```

**Answer:**
JavaScript is a programming language commonly used to create interactive effects within web browsers. It enables dynamic content, such as user interactions and animations.

---

## 2. Variables and Constants

### Subtopics:
- Declaring variables (`var`, `let`, `const`)
- Scope of variables

### Example:
```javascript
let name = 'John';
const age = 25;
var city = 'New York';
console.log(`Name: ${name}, Age: ${age}, City: ${city}`);
```

**Answer:**
- `let` and `const` have block scope; `var` has function scope.
- Use `const` for values that do not change, and `let` for those that do.

---

## 3. Data Types

### Subtopics:
- Primitive Types: String, Number, Boolean, Null, Undefined, Symbol
- Non-Primitive Types: Object, Array, Function

### Example:
```javascript
let str = 'Hello';
let num = 123;
let isAvailable = true;
let person = { name: 'John', age: 30 };
let colors = ['red', 'green', 'blue'];

console.log(typeof str, typeof num, typeof isAvailable);
console.log(person, colors);
```

**Answer:**
JavaScript data types are broadly categorized into:
- Primitive (immutable) types like `string`, `number`, etc.
- Non-Primitive (mutable) types like `object` and `array`.

---

## 4. Operators

### Subtopics:
- Arithmetic Operators
- Comparison Operators
- Logical Operators
- Assignment Operators
- Ternary Operator

### Example:
```javascript
let a = 10;
let b = 20;
console.log(a + b); // Arithmetic
console.log(a > b); // Comparison
console.log(a > 5 && b > 15); // Logical
```

**Answer:**
- Arithmetic: `+`, `-`, `*`, `/`, `%`.
- Logical: `&&`, `||`, `!`.
- Ternary: `condition ? value1 : value2`.

---

## 5. Control Flow

### Subtopics:
- If-Else
- Switch
- Loops (for, while, do-while)

### Example:
#### If-Else Example:
```javascript
let number = 10;
if (number > 0) {
  console.log('Positive number');
} else if (number < 0) {
  console.log('Negative number');
} else {
  console.log('Zero');
}
```

#### Switch Example:
```javascript
let grade = 'A';
switch (grade) {
  case 'A':
    console.log('Excellent');
    break;
  case 'B':
    console.log('Good');
    break;
  default:
    console.log('Need Improvement');
}
```

**Answer:**
- Use `if-else` for conditional logic.
- Use `switch` for multiple conditions with fixed cases.
- Loops are used to iterate over data structures.

---

## 6. Functions

### Subtopics:
- Function Declaration
- Function Expressions
- Arrow Functions
- Default Parameters

### Example:
#### Function Declaration:
```javascript
function greet(name) {
  return `Hello, ${name}`;
}
console.log(greet('Alice'));
```

#### Function Expressions:
```javascript
const multiply = function(a, b) {
  return a * b;
};
console.log(multiply(4, 5));
```

#### Arrow Functions:
```javascript
const add = (a, b) => a + b;
console.log(add(5, 10));
```

#### Default Parameters:
```javascript
function greetWithDefault(name = 'Guest') {
  return `Hello, ${name}`;
}
console.log(greetWithDefault()); // Hello, Guest
console.log(greetWithDefault('Alice')); // Hello, Alice
```

**Answer:**
- Functions encapsulate reusable logic.
- Arrow functions (`=>`) are concise and ideal for callbacks.
- Default parameters allow specifying fallback values.

---

## 7. Objects and Classes

### Subtopics:
- Creating Objects
- Object Methods
- Classes and Inheritance

### Example:
```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hi, I'm ${this.name}`);
  }
}
const john = new Person('John', 30);
john.greet();
```

**Answer:**
- Objects store key-value pairs.
- Classes provide a blueprint for objects, supporting inheritance and encapsulation.

---

## 8. Arrays

### Subtopics:
- Array Methods (`map`, `filter`, `reduce`, etc.)
- Multidimensional Arrays

### Example:
```javascript
let numbers = [1, 2, 3, 4];
let doubled = numbers.map(n => n * 2);
console.log(doubled);
```

**Answer:**
Arrays are ordered collections with powerful methods for transformation and filtering.

---

## 9. Events

### Subtopics:
- Adding Event Listeners
- Handling Events

### Example:
```javascript
<button id="myButton">Click Me</button>
<script>
document.getElementById('myButton').addEventListener('click', () => {
  alert('Button clicked!');
});
</script>
```

**Answer:**
Events are user interactions like clicks or key presses, handled using listeners.

---

## 10. DOM Manipulation

### Subtopics:
- Selecting Elements
- Modifying Content
- Adding and Removing Elements

### Example:
```javascript
let heading = document.createElement('h1');
heading.textContent = 'Hello, DOM!';
document.body.appendChild(heading);
```

**Answer:**
DOM allows interaction with HTML elements via JavaScript for dynamic content.

---

## 11. Promises and Async/Await

### Subtopics:
- Using Promises
- Fetch API
- Async/Await Syntax

### Example:
```javascript
async function fetchData() {
  const response = await fetch('https://jsonplaceholder.typicode.com/posts');
  const data = await response.json();
  console.log(data);
}
fetchData();
```

**Answer:**
Promises and `async/await` handle asynchronous operations like API calls.

---

## 12. Error Handling

### Subtopics:
- Try-Catch-Finally
- Throwing Errors

### Example:
```javascript
try {
  let result = riskyFunction();
} catch (error) {
  console.error('Error occurred:', error.message);
} finally {
  console.log('Execution complete');
}
```

**Answer:**
Error handling ensures robust code execution with fallback mechanisms.

---

## 13. Modules

### Subtopics:
- Export and Import

### Example:
```javascript
// math.js
export const add = (a, b) => a + b;

// main.js
import { add } from './math.js';
console.log(add(2, 3));
```

**Answer:**
Modules split code into reusable files, enhancing maintainability.

---

## 14. Advanced Topics

### Subtopics:
- Closures
- Callbacks
- Higher-Order Functions

### Example:
```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
const counter = outer();
counter();
counter();
```

**Answer:**
Advanced concepts like closures enable encapsulation, callbacks manage async flow, and higher-order functions operate on other functions.

---




## 15. Testing and Debugging

### Subtopics:
- Using `console.log`
- Debugging in Browser

### Example:
```javascript
console.log('Debugging message');
```

**Answer:**
Use `console.log` and browser debugging tools to troubleshoot and inspect code behavior.
