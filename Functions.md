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
# Difference Between Arguments and Parameters in JavaScript

## Parameters
- **Parameters** are variables listed as part of the function definition.
- They act as placeholders for the values that the function will receive when it is called.

Example:

```
function add(a, b) {
  // a and b are parameters
  return a + b;
}
```
## Arguments

- **Arguments** are the actual values passed to the function when it is called.
- These values are assigned to the parameters of the function.

### Example:

```
add(5, 3);
```
| **Aspect**     | **Parameters**                                      | **Arguments**                                  |
|----------------|-----------------------------------------------------|------------------------------------------------|
| **Definition** | Variables in the function definition                | Actual values passed to the function           |
| **Purpose**    | Act as placeholders for the values the function will receive | Provide the actual data the function will use  |
| **Declared**   | In the function definition                          | When the function is called                    |
| **Example**    | `function add(a, b) {}` (`a` and `b` are parameters) | `add(5, 3)` (`5` and `3` are arguments)        |

# Default Parameters in JavaScript

- **Default Parameters** allow you to set default values for function parameters. 
- If no argument is passed when the function is called, the default value is used instead.

### Example:

```js
function greet(name = "Guest") {
  console.log(`Hello, ${name}!`);
}

greet(); // Output: Hello, Guest!
greet("Sumati"); // Output: Hello, Sumati!
```
In the example above:

- If no value is passed for name, it defaults to "Guest".
- If a value is provided, like "Sumati", that value is used instead of the default.

  # Event Handling in JavaScript

- **Event Handling** in JavaScript allows you to respond to user actions like clicks, key presses, or mouse movements.
- It helps make web pages interactive by triggering specific actions when an event occurs.

### Example:

```js
document.getElementById("myButton").addEventListener("click", function() {
  alert("Button was clicked!");
});
```
**In this example:**
- An event listener is added to the button.
- When the button is clicked, the function is triggered, showing an alert.
Common Events:
- **click:** When the user clicks an element.
- **keydown:** When a key is pressed.
- **mouseover:** When the mouse hovers over an element.
## Why Use Event Handling?
- It makes web pages interactive.
- You can respond to user inputs, control animations, validate forms, etc.
