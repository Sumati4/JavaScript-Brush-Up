## What are Variables?

**Variables** are like storage boxes for data in your code. They let you keep values like numbers or text, and you can give these values names so you can easily use them later. For example, you might have a variable named `age` to store a person’s age.

### Difference Between `var`, `let`, and `const`

In JavaScript, there are three ways to create variables: `var`, `let`, and `const`. Here’s how they are different:

- **`var`**:
  - **Scope**: The variable is available throughout the function in which it is declared. If it’s declared outside of any function, it is available globally.
  - **Hoisting**: The declaration is moved to the top of its scope, so you can use it before it is declared in the code.
  - **Reassignment**: You can change the value of a `var` variable anytime.

  ```js
  var name = "Alice";
  name = "Bob"; // This is allowed
   ```

- **`let`**

   - **Scope**: The variable is available only within the block (like inside `{ }`) where it is declared.
   - **Hoisting**: The declaration is moved to the top, but the variable is not accessible before its declaration in the code.
   - **Reassignment**: You can change the value of a `let` variable anytime.

```javascript
let age = 30;
age = 31; // This is allowed
```
- **`const`**

    - **Scope**: The variable is available only within the block where it is declared.
    - **Hoisting**: The declaration is moved to the top, but the variable is not accessible before its declaration.
    - **Reassignment**: You cannot change the value of a `const` variable once it is set.

```javascript
const pi = 3.14;
// pi = 3.1415; // This will cause an error
```
### Summary
- Use var for older code or function-scoped variables.
- Use let for variables that you will change, and that are limited to a block scope.
- Use const for variables that should not change once set.
This document serves as a simple explanation of JavaScript .

# Data Types in JavaScript

In JavaScript, **data types** refer to the different types of values that variables can hold. There are two main categories: **Primitive** and **Non-Primitive** data types.

## Primitive Data Types:
These are basic data types that represent single values. There are 7 primitive data types in JavaScript:

1. **Number**: Represents numbers, including integers and floating-point values (decimals).
   ```
   let age = 25;
   let pi = 3.14;
   ```
2. **String:** Represents a sequence of characters (text), enclosed in quotes (single ', double ", or backticks `).
```
let name = "Sumati";
```
3.**Boolean:**  Represents logical values, either true or false.
```
let isStudent = true;
```
4.**Null:** Represents an empty or non-existent value. It is manually assigned.
```
let result = null;
```
5.**Undefined:** A variable that is declared but not assigned any value is undefined by default.
```
let car;
```
6.**Symbol:** Represents a unique identifier, useful for object properties.
```
let sym = Symbol("unique");
```
7.**BigInt:** Used for working with very large integers, beyond the safe range for Number.
```
let bigNum = 123456789012345678901234567890n;
```
## Non-Primitive Data Types:
Non-primitive data types are more complex and can store multiple values. The main non-primitive type in JavaScript is Object.

1.**Object:** Can hold multiple values as key-value pairs. It can also represent arrays and functions.
```
let person = { name: "Sumati", age: 25 };
```
2.**Array:** A type of object that holds a list of values.

```
let numbers = [1, 2, 3, 4];
```
