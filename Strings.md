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
- **Template Literals:** Make string writing simpler and support multi-line strings.
- **String Interpolation:** Makes it easy to insert variables and expressions inside strings using ${} inside template literals.

# Single Quotes vs Double Quotes vs Backticks in JavaScript

In JavaScript, strings can be created using **single quotes (`'`)**, **double quotes (`"`)**, or **backticks (` `` `)**. Each has its use case and features. Here's a comparison:

| **Feature**              | **Single Quotes `' '`**                                   | **Double Quotes `" "`**                                    | **Backticks `` ` ` ``**                                    |
|--------------------------|-----------------------------------------------------------|------------------------------------------------------------|-------------------------------------------------------------|
| **Basic Usage**           | Used for creating simple strings                          | Similar to single quotes for simple strings                 | Used for template literals and multi-line strings            |
| **Variable Interpolation**| Not supported, must concatenate variables using `+`       | Not supported, must concatenate variables using `+`          | Supports string interpolation with `${}`                    |
| **Multi-line Strings**    | Not supported, need to use `\n` for new lines             | Not supported, need to use `\n` for new lines               | Supports multi-line strings without special characters       |
| **Escape Characters**     | Use `\'` to escape single quotes inside the string        | Use `\"` to escape double quotes inside the string          | Backticks rarely need escaping, but `\`` can escape a backtick |
| **Preferred Use Case**    | When consistency is needed, e.g., JSON                    | When consistency is needed, e.g., JSON                      | When you need interpolation or multi-line strings            |

---

### Examples

1. **Single Quotes**:

```javascript
let singleQuoteStr = 'This is a string';
let name = 'Sumati';
let message = 'Hello, ' + name + '!';  // Concatenation required
console.log(message);
```
2.**Double Quotes:**
```
let doubleQuoteStr = "This is also a string";
let name = "Sumati";
let message = "Hello, " + name + "!";  // Concatenation required
console.log(message);
```
3.**Backticks (Template Literals):**
```
let backtickStr = `This is a string with backticks`;
let name = "Sumati";
let message = `Hello, ${name}! Welcome to JavaScript.`;  // String interpolation
console.log(message);
```
### Summary

- **Single Quotes (`' '`) and Double Quotes (`" "`):** 
  Both are similar, and the choice between them often comes down to **preference** or **consistency**. Neither supports string interpolation or multi-line strings without escape characters.

- **Backticks (Template Literals `` ` ` ``):** 
  Offer more flexibility with **string interpolation** and **multi-line strings**, making them ideal for **dynamic content** or when working with complex strings.

  # Important String Operations in JavaScript

This document highlights some of the most commonly used string operations in JavaScript, with examples to demonstrate their usage.

## 1. `length`
The `length` property returns the length of a string.

```
let str = "Hello, World!";
console.log(str.length);  // Output: 13
```



## 2. charAt()
The charAt() method returns the character at a specified index (position) in a string.

```
let str = "Hello";
console.log(str.charAt(1));  // Output: e
```
## 3. indexOf()
The indexOf() method returns the index of the first occurrence of a specified value in a string. If the value is not found, it returns -1.
```
let str = "Hello, World!";
console.log(str.indexOf("World"));  // Output: 7
console.log(str.indexOf("JavaScript"));  // Output: -1
```
## 4. includes()
The includes() method checks whether a string contains a specified substring. It returns true or false.
```
let str = "Hello, World!";
console.log(str.includes("World"));  // Output: true
console.log(str.includes("JavaScript"));  // Output: false
```
## 5. substring()
The substring() method extracts a part of a string and returns it as a new string. You can specify the start and end indices.
```
let str = "Hello, World!";
console.log(str.substring(0, 5));  // Output: Hello
```
## 6. slice()
The slice() method extracts a section of a string and returns it as a new string, similar to substring(), but it can also accept negative indices.
```
let str = "Hello, World!";
console.log(str.slice(7));  // Output: World!
console.log(str.slice(-6));  // Output: World!
```
## 7. toUpperCase() and toLowerCase()
These methods convert the string to uppercase or lowercase, respectively.
```
let str = "Hello, World!";
console.log(str.toUpperCase());  // Output: HELLO, WORLD!
console.log(str.toLowerCase());  // Output: hello, world!
```
## 8. replace()
The replace() method replaces the first occurrence of a specified value with another value. To replace all occurrences, use a regular expression with the global flag (/g).
```
let str = "Hello, World!";
console.log(str.replace("World", "JavaScript"));  // Output: Hello, JavaScript!
console.log(str.replace(/o/g, "0"));  // Output: Hell0, W0rld!
```
## 9. split()
The split() method splits a string into an array of substrings based on a specified delimiter.
```
let str = "Hello, World!";
let arr = str.split(", ");
console.log(arr);  // Output: ['Hello', 'World!']
```

## 10. trim()
The trim() method removes whitespace from both ends of a string.
```
let str = "   Hello, World!   ";
console.log(str.trim());  // Output: "Hello, World!"
```
## 11. concat()
The concat() method concatenates (joins) two or more strings.
```
let str1 = "Hello";
let str2 = "World";
console.log(str1.concat(", ", str2, "!"));  // Output: Hello, World!
```
## 12. startsWith() and endsWith()
The startsWith() method checks if a string starts with a specified substring, and endsWith() checks if it ends with a specified substring.
```
let str = "Hello, World!";
console.log(str.startsWith("Hello"));  // Output: true
console.log(str.endsWith("!"));  // Output: true
```
## 13. repeat()
The repeat() method repeats a string a specified number of times.

```
let str = "Hello ";
console.log(str.repeat(3));  // Output: Hello Hello Hello
```
## 14. `substr()`
The `substr()` method extracts a part of a string, starting at a specified index and extending for a given number of characters. Unlike `substring()`, you specify the start index and the length of the substring.

```javascript
let str = "Hello, World!";
console.log(str.substr(7, 5));  // Output: World
```
Note: substr() is considered a legacy function, and it is recommended to use slice() or substring() instead for modern code.
## 15. search()
The search() method searches a string for a specified value or regular expression and returns the position of the match. If no match is found, it returns -1.
```
let str = "Hello, World!";
console.log(str.search("World"));  // Output: 7
console.log(str.search("JavaScript"));  // Output: -1
```
## 16. `lastIndexOf()`
The `lastIndexOf()` method returns the index of the last occurrence of a specified value in a string. It searches from the end of the string towards the beginning. If the value is not found, it returns `-1`.

```javascript
let str = "Hello, World, Hello!";
console.log(str.lastIndexOf("Hello"));  // Output: 13
console.log(str.lastIndexOf("World"));  // Output: 7
```
## 17. charCodeAt()
The charCodeAt() method returns the Unicode of the character at a specified index in a string. The returned value is an integer representing the UTF-16 code unit.
```
let str = "Hello";
console.log(str.charCodeAt(0));  // Output: 72 (Unicode for 'H')
```
## 18. valueOf()
The valueOf() method returns the primitive value of a String object. In most cases, this method is called automatically when string operations are applied, so it's rarely used explicitly.

```
let str = new String("Hello");
console.log(str.valueOf());  // Output: Hello
```
## 19. toString()
The toString() method returns a string representing the specified object. It's similar to valueOf(), but can be explicitly called on various data types (e.g., numbers, arrays) to return their string representation.

```
let num = 123;
console.log(num.toString());  // Output: "123"
```
## 20. match()
The match() method retrieves the result of matching a string against a regular expression. It returns an array of matches, or null if no match is found.

```
let str = "The rain in Spain stays mainly in the plain";
let result = str.match(/ain/g);
console.log(result);  // Output: ['ain', 'ain', 'ain']
```
You can also use it with capturing groups:

```
let str = "2024-09-10";
let datePattern = /(\d{4})-(\d{2})-(\d{2})/;
let result = str.match(datePattern);
console.log(result);  
// Output: ['2024-09-10', '2024', '09', '10']
```

