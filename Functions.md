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
## Common Events:
- **click:** When the user clicks an element.
- **keydown:** When a key is pressed.
- **mouseover:** When the mouse hovers over an element.
## Why Use Event Handling?
- It makes web pages interactive.
- You can respond to user inputs, control animations, validate forms, etc.

 # First-Class Functions in JavaScript

- **First-Class Functions** mean that functions in JavaScript are treated like any other variable.
- They can be stored in variables, passed as arguments to other functions, and returned from functions.

### Example:

```js
// Assign a function to a variable
const greet = function() {
  console.log("Hello!");
};

// Pass a function as an argument
function callFunction(func) {
  func(); // Calling the passed function
}

callFunction(greet); // Output: Hello!
```
**In this example:**

- The greet function is assigned to a variable.
- It is passed as an argument to the callFunction function, showing how functions are treated like values.
**Key Features:**
- Assign functions to variables.
- Pass functions as arguments to other functions.
- Return functions from other functions.
## Why First-Class Functions are Useful:
They make JavaScript flexible and powerful, allowing techniques like callbacks, higher-order functions, and functional programming. 

# Pure vs Impure Functions in JavaScript

| **Aspect**             | **Pure Functions**                                                                 | **Impure Functions**                                                                |
|------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Definition**          | A function that always returns the same output for the same input and has no side effects. | A function whose output can change for the same input or has side effects (e.g., modifying external data). |
| **Characteristics**     | - No side effects (does not modify external state) <br> - Returns the same result for the same input | - May have side effects (modifies external state) <br> - Output may vary even for the same input |
| **Example**             | ```js  function add(a, b) { return a + b; } ```                                   | ```js let count = 0; function increment() { count++; return count; } ```           |
| **Output**              | - Always predictable output (e.g., `add(2, 3)` will always return `5`)             | - Output depends on external state (e.g., `increment()` will return a different result each time it is called) |
| **Use Case**            | - Easier to test and debug <br> - Makes the code more predictable and reliable     | - Can be useful when you need to update external states like UI or server requests  |

### Explanation:

- **Pure Function Example:**
  ```js
  function add(a, b) {
    return a + b;
  }
  ```
Always returns the same output for the same input (add(2, 3) always returns 5).

**Impure Function Example:**
```
let count = 0;
function increment() {
  count++;
  return count;
}
```
The output changes with every call because it modifies the external variable count.
### Conclusion:
- Pure functions are predictable and have no side effects.
- Impure functions may modify external state and produce different results for the same input.

# Function Currying in JavaScript

- **Currying** is a technique in JavaScript where a function is transformed into a series of functions, each taking a single argument.
- Instead of taking all arguments at once, a curried function takes them one at a time.

### Example:

```js
function add(a) {
  return function(b) {
    return a + b;
  };
}

const addTwo = add(2); // The first argument is '2'
console.log(addTwo(3)); // Output: 5
```
**In this example:**
-The add function is curried.
-First, add(2) is called, returning a new function.
-Then, addTwo(3) is called, which completes the addition (2 + 3 = 5).
## Why Use Currying?
- It allows you to break down a function into smaller, more manageable parts.
- It’s useful when you want to reuse a function with some preset values (partial application).

**Currying is like splitting a function that takes multiple arguments into a chain of functions, each handling one argument at a time**

# `call()`, `apply()`, and `bind()` Methods in JavaScript

These methods are used to control the context (`this`) of functions in JavaScript.

## 1. `call()`

- **Purpose**: Invokes a function with a given `this` value and individual arguments.
- **Syntax**: `functionName.call(thisValue, arg1, arg2, ...)`

### Example:

```js
function greet(greeting, name) {
  console.log(`${greeting}, ${name}!`);
}

greet.call(null, "Hello", "Sumati"); // Output: Hello, Sumati!
```
**In this example:**
- call() invokes the greet function.
- null sets the this value (not used in this example).
- "Hello" and "Sumati" are the arguments passed to greet.
## 2. apply()
- **Purpose:** Invokes a function with a given this value and arguments provided as an array.
- **Syntax:** functionName.apply(thisValue, [arg1, arg2, ...])
### Example:
```
function greet(greeting, name) {
  console.log(`${greeting}, ${name}!`);
}

greet.apply(null, ["Hello", "Sumati"]); // Output: Hello, Sumati!
```
**In this example:**
- apply() invokes the greet function.
- null sets the this value (not used in this example).
- ["Hello", "Sumati"] is an array of arguments passed to greet.
## 3. bind()
**Purpose:** Creates a new function with a given this value and initial arguments, which can be called later.
**Syntax:** const newFunction = functionName.bind(thisValue, arg1, arg2, ...)
### Example:
```
function greet(greeting, name) {
  console.log(`${greeting}, ${name}!`);
}

const greetHello = greet.bind(null, "Hello");
greetHello("Sumati"); // Output: Hello, Sumati!
```
**In this example:**
- bind() creates a new function greetHello with this value null and "Hello" as the preset argument.
- greetHello("Sumati") calls the new function with "Sumati" as the second argument.
### Summary
- **call():** Calls a function immediately with specified this and arguments.
- **apply():** Calls a function immediately with specified this and an array of arguments.
- **bind():** Creates a new function with a specified this and initial arguments, to be called later.
