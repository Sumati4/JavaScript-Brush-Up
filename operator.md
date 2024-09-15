 Operator Precedence in JavaScript

### What is Operator Precedence?

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
