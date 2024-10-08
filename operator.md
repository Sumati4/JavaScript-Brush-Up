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

# Conditional Statement Types in JavaScript

Conditional statements are used to make decisions in JavaScript code. They allow you to execute different code blocks based on certain conditions. Here are the main types of conditional statements:

### 1. `if` Statement

The `if` statement allows you to execute a block of code if a specified condition is true.

**Syntax:**
```
if (condition) {
    // Code to execute if the condition is true
}
```
Example:
```
let age = 20;
if (age >= 18) {
    console.log('You are an adult.');
}
```
### 2. if-else Statement
The if-else statement provides an alternative block of code to execute if the condition is false.

Syntax:
```
if (condition) {
    // Code to execute if the condition is true
} else {
    // Code to execute if the condition is false
}
```
Example:
```
let age = 16;
if (age >= 18) {
    console.log('You are an adult.');
} else {
    console.log('You are a minor.');
}
```
### 3. if-else if-else Statement
The if-else if-else statement allows you to check multiple conditions.

Syntax:
```
if (condition1) {
    // Code to execute if condition1 is true
} else if (condition2) {
    // Code to execute if condition2 is true
} else {
    // Code to execute if none of the above conditions are true
}
```
Example:
```
let score = 85;
if (score >= 90) {
    console.log('Grade: A');
} else if (score >= 80) {
    console.log('Grade: B');
} else {
    console.log('Grade: C');
}
```
### 4. switch Statement
The switch statement is used to select one of many code blocks to be executed based on the value of an expression.

Syntax:
```
switch (expression) {
    case value1:
        // Code to execute if expression === value1
        break;
    case value2:
        // Code to execute if expression === value2
        break;
    default:
        // Code to execute if no case matches
}
```
Example:

```
let day = 3;
switch (day) {
    case 1:
        console.log('Monday');
        break;
    case 2:
        console.log('Tuesday');
        break;
    case 3:
        console.log('Wednesday');
        break;
    default:
        console.log('Weekend');
}
```
### Summary

- **`if` Statement**: Executes code if a condition is true.
- **`if-else` Statement**: Executes one block of code if a condition is true, and another block if it's false.
- **`if-else if-else` Statement**: Checks multiple conditions and executes the corresponding code block.
- **`switch` Statement**: Selects and executes one block of code from multiple options based on the value of an expression.
# Double Equals (`==`) vs Triple Equals (`===`) in JavaScript

In JavaScript, there are two types of equality operators that you can use to compare values: `==` (double equals) and `===` (triple equals). They work differently when checking for equality.

### Double Equals (`==`)

The **double equals (`==`)** operator checks for **equality** of values, but it **does not** consider the **data type**. It performs type coercion, which means it converts the values to the same type before comparing them.

**Example:**
```js
let num = 5;
let str = '5';

console.log(num == str); // Output: true
```
Here, num is a number and str is a string, but == converts the string '5' to the number 5 before comparing, so the result is true.
### Triple Equals (`===`)

The **triple equals (`===`)** operator checks for both **value** and **data type**. It does not perform type coercion, so both the value and the type must be the same for the comparison to return `true`.

**Example:**
```js
let num = 5;
let str = '5';

console.log(num === str); // Output: false
```
Here, num is a number and str is a string. Since === checks both the value and the type, and they are different types, the result is false.
### Summary

- **Double Equals (`==`)**: Compares values for equality **after** converting them to the same type. (Type coercion)
- **Triple Equals (`===`)**: Compares values for equality **without** converting them. Both value and type must be the same.

Use `===` when you want to ensure that both the value and the type are exactly the same, and `==` if you want to allow for type coercion.

