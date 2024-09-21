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
