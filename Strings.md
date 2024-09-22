# What is a String in JavaScript?

In JavaScript, a **string** is a sequence of characters used to represent text. Strings can include letters, numbers, symbols, spaces, or a combination of these.

## How to Write a String?
You can create a string by enclosing characters in quotes. There are three types of quotes you can use:
1. **Single quotes**: `'Hello'`
2. **Double quotes**: `"Hello"`
3. **Backticks (Template literals)**: `` `Hello` ``

### Example:
```js
let myString1 = 'This is a string';
let myString2 = "This is also a string";
let myString3 = `This is a string using backticks`;
```
## String Properties:
Strings are immutable, meaning once created, they cannot be changed.
You can find the length of a string using .length property.
Example:
```
let message = "Hello, World!";
console.log(message.length); // Output: 13
```
## Common String Methods:
**toUpperCase()** - Converts the string to uppercase.
```
let str = "hello";
console.log(str.toUpperCase()); // Output: "HELLO"
```
**toLowerCase()**- Converts the string to lowercase.
```
let str = "HELLO";
console.log(str.toLowerCase()); // Output: "hello"
```
**charAt(index)** - Returns the character at the specified index.

```
let str = "JavaScript";
console.log(str.charAt(0)); // Output: "J"
```
**substring(start, end)**- Extracts a part of the string.
```
let str = "Hello, World!";
console.log(str.substring(0, 5)); // Output: "Hello"
```
## Conclusion:
Strings in JavaScript are used to work with text. You can perform various operations on strings using different methods like changing case, extracting characters, and more!

# Template Literals vs String Interpolation in JavaScript

In JavaScript, **template literals** and **string interpolation** are closely related. Template literals allow us to embed expressions directly inside a string, which is what string interpolation is used for.

Here's a simple comparison:

| **Feature**                | **Template Literals**                                         | **String Interpolation** |
|----------------------------|---------------------------------------------------------------|--------------------------|
| **Definition**              | A way to create strings using backticks `` ` ` ``             | Inserting variables or expressions into strings |
| **Syntax**                  | Uses backticks `` ` ` `` instead of quotes `" "` or `' '`     | Use `${expression}` inside template literals |
| **Multi-line Support**      | Allows writing multi-line strings easily                     | Part of template literals, lets you insert dynamic content inside strings |
| **Variable Insertion**      | Supports inserting variables directly inside the string       | Achieved by wrapping expressions inside `${}` |
| **Expression Support**      | Can include JavaScript expressions directly inside a string   | Part of template literals, can evaluate expressions in `${}` |
| **Use Case**                | To create complex, multi-line, or dynamic strings easily      | To dynamically insert variables/expressions in a string |

### Example

1. **Without Template Literals or String Interpolation:**

```javascript
let name = "Sumati";
let greeting = "Hello, " + name + "! Welcome to JavaScript.";
console.log(greeting);
```
Here, you have to concatenate (join) strings with +, which can be messy.

2.**With Template Literals and String Interpolation:**
```
let name = "Sumati";
let greeting = `Hello, ${name}! Welcome to JavaScript.`;
console.log(greeting);
```
In this version, using template literals (backticks `) makes it much cleaner and easier to interpolate the variable name.

**Multi-line String Example:**
Without Template Literals:
```
let message = "This is line 1.\n" + 
              "This is line 2.";
console.log(message);
```
**With Template Literals (Multi-line Support):**
```
let message = `This is line 1.
This is line 2.`;
console.log(message);
```
The template literal automatically handles the new line without needing .

### Summary
Template Literals: Make string writing simpler and support multi-line strings.
String Interpolation: Makes it easy to insert variables and expressions inside strings using ${} inside template literals.
