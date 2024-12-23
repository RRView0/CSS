# JavaScript Topics with Examples

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

## 5. Control Flow

### Subtopics:
- If-Else
- Switch
- Loops (for, while, do-while)

### Example:
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

## 6. Functions

### Subtopics:
- Function Declaration
- Function Expressions
- Arrow Functions
- Default Parameters

### Example:
```javascript
function greet(name) {
  return `Hello, ${name}`;
}
console.log(greet('Alice'));

const add = (a, b) => a + b;
console.log(add(5, 10));
```

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

## 15. Testing and Debugging

### Subtopics:
- Using `console.log`
- Debugging in Browser

### Example:
```javascript
console.log('Debugging message');
