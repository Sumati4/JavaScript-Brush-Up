 Operator Precedence in JavaScript

# What is Operator Precedence?

Operator precedence determines the order in which operations are performed in an expression with multiple operators. JavaScript follows specific rules to decide which operations to execute first.

For example:
```
let result = 3 + 4 * 2;
console.log(result); // Output: 11, not 14
```
Here, multiplication (*) happens before addition (+) because * has higher precedence than +.
### Simple Rule

Think of operator precedence like math rules (BODMAS):
- **Multiplication** and **Division** come before **Addition** and **Subtraction**.
- Some operators (like `()` for parentheses) are evaluated first.

### Example of Operator Precedence

```
let a = 5;
let b = 10;
let result = a + b * 2 - 3; 
console.log(result); // Output: 17
```
### Explanation:

- First, `b * 2` is calculated (since `*` has higher precedence).
- Then, `a + result` from the first calculation is evaluated.
- Finally, `- 3` is done.

### Precedence Table (Common Operators)

| Operator   | Description              | Precedence |
|------------|--------------------------|------------|
| `()`       | Parentheses               | Highest    |
| `*`, `/`   | Multiplication, Division  | High       |
| `+`, `-`   | Addition, Subtraction     | Medium     |
| `=`        | Assignment                | Lowest     |

Remember, operators with **higher precedence** are evaluated before those with **lower precedence**. If two operators have the **same precedence**, they are evaluated from **left to right**.

### Grouping with Parentheses

You can use parentheses `()` to change the order of evaluation:

```js
let result = (3 + 4) * 2;
console.log(result); // Output: 14
```
# Unary vs Binary vs Ternary Operators in JavaScript

### 1. Unary Operators

A **unary operator** works with **a single operand** (one value).

- **Example**: `++`, `--`, `typeof`, etc.
  
  ```
  let x = 5;
  x++; // Unary operator '++' increments the value of x by 1
  console.log(x); // Output: 6

  console.log(typeof x); // Output: 'number' (typeof is a unary operator that checks the type of the variable)

```

### 2. Binary Operators

A binary operator works with **two operands** (two values).

- **Example**: `+`, `-`, `*`, `/`, `>`, `<`, `&&`, `||`, etc.

```
let a = 10;
let b = 5;
let sum = a + b; // '+' is a binary operator that adds two values
console.log(sum); // Output: 15
```
Here, a and b are the two operands, and + is the binary operator.

### 3. Ternary Operator

A ternary operator works with **three operands** and is often used as a shortcut for an `if-else` statement. It's also called a **conditional operator**.

- **Syntax**: `condition ? expression1 : expression2`

```js
let age = 18;
let canVote = (age >= 18) ? 'Yes' : 'No'; // Ternary operator checks the condition
console.log(canVote); // Output: 'Yes'
```

Here, the condition `(age >= 18)` is checked:

- If **true**, the result is `'Yes'`.
- If **false**, the result is `'No'`.

### Summary

- **Unary Operator**: Works with **one operand** (e.g., `++`, `--`, `typeof`).
- **Binary Operator**: Works with **two operands** (e.g., `+`, `-`, `*`, `&&`, `||`).
- **Ternary Operator**: Works with **three operands** and is used for conditional expressions (e.g., `condition ? true : false`).
# Short-Circuit Evaluation in JavaScript

# What is Short-Circuit Evaluation?

**Short-circuit evaluation** is a concept in JavaScript where logical operators (`&&` and `||`) stop evaluating as soon as the result is known.

- **`&&` (AND operator)**: If the first value is **false**, it will **not** check the second value because the entire expression will be false.
- **`||` (OR operator)**: If the first value is **true**, it will **not** check the second value because the entire expression will be true.

### How it Works

### AND (`&&`) Operator

In an `&&` operation, if the first value is **false**, the expression stops and returns **false** immediately.

```
let result = false && true; 
console.log(result); // Output: false
```
Here, the first value is false, so JavaScript does not check the second value.

#### OR (||) Operator
In an || operation, if the first value is true, the expression stops and returns true immediately.

```
let result = true || false; 
console.log(result); // Output: true
```
Here, the first value is true, so JavaScript does not check the second value.

Example
```
let x = 0;
let y = 5;

let result = x || y; 
console.log(result); // Output: 5
```
In this case, x is 0 (which is falsy), so the || operator checks y, which is 5, and returns it.

### Summary
**&& (AND):** Stops at the first false value.
**|| (OR):** Stops at the first true value.
