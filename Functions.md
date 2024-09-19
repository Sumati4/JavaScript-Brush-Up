# Functions in JavaScript

A **function** in JavaScript is a block of code designed to perform a particular task. You can think of it as a reusable piece of code that runs when "called" or "invoked."

## How to Define a Function

There are several ways to define functions in JavaScript:

### 1. Function Declaration

This is the most common way to declare a function.

```
function functionName() {
  // code to be executed
}
```
Example:
```
function sayHello() {
  console.log("Hello, World!");
}
```
You can then call the function like this:
```
sayHello(); // Output: Hello, World!
```
### 2. Function Expression
In this method, a function is assigned to a variable.
```
const functionName = function() {
  // code to be executed
};
```
Example:
```
const greet = function() {
  console.log("Hi there!");
};

greet(); // Output: Hi there!
```
# Types of Functions in JavaScript

## 1. Named Functions
Functions with a name.

```js
function myFunction() {
  // code
}
```
## 2. Anonymous Functions
Functions without a name, often used in function expressions.
```
const myFunction = function() {
  // code
};
```
## 3. Arrow Functions
Arrow functions provide a shorter syntax for writing functions, introduced in ES6.
```
const myFunction = () => {
  // code
};
```
## 4. IIFE (Immediately Invoked Function Expression)
These functions run immediately after being defined.
```
(function() {
  // code
})();
```
## 5. Callback Functions
Functions passed as arguments to other functions. They are executed inside the outer function.
```
function doSomething(callback) {
  callback();
}
```
