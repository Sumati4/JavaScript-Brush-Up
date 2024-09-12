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
# Difference Between `null` and `undefined` in JavaScript

In JavaScript, `null` and `undefined` are two different values, but they both represent the absence of a value.

## 1. `null`:
- **Meaning**: `null` represents an empty or non-existent value. It is like saying, "There is nothing here."
- **Who assigns it?**: It is **explicitly assigned by the programmer** when they want to indicate that something is intentionally empty or has no value.

### Real-Life Example:
Think of `null` like a parking spot that has a sign saying "No car." The parking spot exists, but it's intentionally left empty.

```
let car = null; // No car is present here.
```
Another Example:
If you have an empty glass and you decide to say, "This glass has nothing in it," you are assigning null to the glass.

## 2. undefined:
**Meaning:** undefined means that a variable has been declared, but no value has been assigned to it yet. It's like saying, "I don't know what goes here."
**Who assigns it?:** It is automatically assigned by JavaScript when you declare a variable but do not give it a value.
### Real-Life Example:
Think of undefined like a new parking spot with no car, but there's no sign either. You just don't know yet if a car will park there or not.
```
let house; // No value is assigned, so it's undefined.
```
Another Example:
If you have an empty glass and you never said whether it should have water or juice, the glass is undefined.

**Key Difference:**
**null:** You, the programmer, assign it when you want to say, "There is nothing here."
**undefined:** JavaScript assigns it when a variable has been declared, but no value has been given yet.
### In summary:
**null** is like saying, "This has no value, and I know it."
**undefined** is like saying, "I don't know the value yet."
