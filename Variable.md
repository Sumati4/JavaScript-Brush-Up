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
