

### What is JavaScript?

JavaScript (JS) is a popular programming language that convert static web pages to interactive and dynamic web pages. It is often used for things like:

- **Changing web page content**: Updating text, images, and styles without refreshing the page.
- **Handling user actions**: Responding to clicks, form inputs, or keyboard actions.
- **Running tasks in the background**: Fetching data from servers without reloading the page (using technologies like `fetch` or `AJAX`).
- **Object-oriented features**: JS supports objects and inheritance for more complex programming.

JavaScript runs directly in the browser (client-side), but it can also be used on the server-side using tools like **Node.js**. It's commonly used for building web applications, validating forms, and managing the behavior of the browser.


---

### What is a JavaScript Engine and Its Role?

A **JavaScript engine** is a program that executes JavaScript code. Every browser has its own JS engine. Some popular ones are:

- **V8** (used by Chrome and Node.js)
- **SpiderMonkey** (used by Firefox)
- **JavaScriptCore** (used by Safari)
- **Chakra** (used by Microsoft Edge)

#### How Does a JS Engine Work?

1. **Parsing**: The engine reads the JavaScript code and turns it into a structure called an Abstract Syntax Tree (AST). This helps the engine understand the code.
2. **Compilation**: Modern JS engines use a technique called **Just-In-Time (JIT) Compilation**. This means they compile the code into machine code while the program is running to make it faster.
3. **Execution**: After compilation, the engine runs the machine code and manages things like variables, function calls, and events.
4. **Memory Management**: The engine also handles memory. It cleans up unused data to free up space, preventing memory leaks.

In summary, the **JS Engine** is responsible for reading, optimizing, and executing JavaScript code efficiently.

---
# Client-Side vs. Server-Side

### What is Client-Side?

**Client-side** refers to everything that happens on the user's device (like their browser) when they visit a website. This includes:

- **HTML, CSS, and JavaScript**: These are the core technologies that the browser uses to display web pages and make them interactive.
- **User Interactions**: Anything you do on a website, like clicking buttons, filling out forms, or scrolling through content, happens on the client-side.


**Client-side** is all about how the website looks and behaves for the user. It happens on the user's machine, and changes made on the client-side do not need to communicate with the server.

### What is Server-Side?

**Server-side** refers to everything that happens on a web server behind the scenes. When you visit a website, your browser sends a request to the server, and the server sends back the necessary files (like HTML, images, or data). The server-side is responsible for:

- **Handling Requests**: When you submit a form or make a purchase, the data is sent to the server for processing.
- **Database Operations**: Storing and retrieving information like user accounts, products, or blog posts.
- **Security**: Authenticating users, encrypting sensitive data, and managing secure transactions.
- **Generating Web Pages**: The server can dynamically create web pages based on the data it has, such as user profiles or search results.

The **server-side** works behind the scenes, away from the user. It handles data processing, business logic, and interactions with databases or APIs.

---

### Key Differences:

- **Client-side** happens on the user's browser (the "front end").
- **Server-side** happens on the server (the "back end").

In simple terms:
- **Client-side** = What you see and interact with on a website.
- **Server-side** = What makes the website work behind the scenes.
![](https://github.com/Sumati4/JavaScript-Brush-Up/blob/main/client%20side%20and%20server%20side.png)

## What is REPL?

**REPL** stands for **Read-Eval-Print Loop**. It’s an interactive environment where you can quickly test small pieces of code. Here's what happens in REPL:
REPL is commonly used in programming languages like JavaScript, Python, Ruby, etc. For example, when you open a JavaScript console in a browser or a Python interpreter, you're working inside a REPL.

- **Read**: It reads the user’s input (a line of code).
- **Eval**: It evaluates the input and processes the result..
- **Print**: It prints the result of the evaluation to the user.
- **Loop**: The process repeats, allowing for more inputs.

REPL is great for trying out code snippets and learning. You don’t need to write a full program—just type and see what happens!

### Example in JavaScript REPL:

```js
> let num = 10;
> num * 2;
20
```
## What is the Console Window?

The **console window** is a part of the REPL (Read-Eval-Print Loop) environment. It's a tool where you can write and test code, and see the results immediately. You can usually find the console window in web browsers or development tools.

### How to Open the Console Window

In most web browsers, you can open the console by pressing `F12` or `Ctrl + Shift + I`, then selecting the "Console" tab.

### Example of Using the Console

```js
> console.log("Hello, World!");
Hello, World!
```

### Why Use the Console Window?
- **Quick Testing:** Test your code instantly.
- **Debugging:** Find and fix errors in your code.
- **Logging**: Print messages to understand what’s happening.

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
# Understanding the DOM and its Difference from HTML

## What is the DOM?

**DOM** stands for **Document Object Model**. It is a structured representation of an HTML document that JavaScript can interact with. When a webpage is loaded, the browser creates a live, interactive model of the page known as the DOM, allowing developers to manipulate the content, structure, and style of the web page dynamically.

In simple terms:
- Think of the DOM as a **bridge** between HTML and JavaScript.
- It represents the web page as a tree of objects, where each HTML element is a node.

### Example:

If you have this HTML:
```
<!DOCTYPE html>
<html>
  <body>
    <h1>Hello, World!</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```
The DOM representation would look like a tree:
```
Document
 └── html
      └── body
           ├── h1 ("Hello, World!")
           └── p ("This is a paragraph.")
```



## HTML:
- **What it is**: A language used to define the structure of a webpage.
- **Static**: Once written, HTML is just static text and cannot change by itself.
- **Defines**: The layout, elements, and structure of a webpage (like paragraphs, headings, images).

## DOM:
- **What it is**: A live, interactive representation of the webpage created by the browser.
- **Dynamic**: It can be manipulated by JavaScript to change the content, structure, or styles of the webpage after it has loaded.
- **Controls**: Allows scripts (JavaScript) to read, modify, or interact with HTML elements.

---

# JavaScript Selectors

## What are Selectors in JavaScript?

Selectors in JavaScript are used to **select** and **manipulate** HTML elements on a webpage. They help you target specific elements in the Document Object Model (DOM) so that you can read or change their content, style, or attributes using JavaScript.

In simple terms:
- Think of selectors as **tools** that let you point at specific elements on a web page.
- Once selected, you can do things like change the text, update the style, or handle events (e.g., clicking a button).

## Common JavaScript Selectors:

### 1. `getElementById()`
This selector targets an element by its **ID**. IDs are unique, so this method will only return one element.

```javascript
let element = document.getElementById('myElement');
console.log(element);  // Outputs the element with ID 'myElement'
```
### 2. getElementsByClassName()
This selector targets all elements that have a specific class. It returns a collection (array-like) of elements.

```
let elements = document.getElementsByClassName('myClass');
console.log(elements);  // Outputs a collection of all elements with the class 'myClass'
```
### 3. getElementsByTagName()
This selector targets all elements by their tag name (e.g., div, p, h1). It returns a collection of elements.
```
let elements = document.getElementsByTagName('p');
console.log(elements);  // Outputs all  (paragraph) elements
```
### 4. querySelector()
This selector targets the first element that matches a specific CSS selector. It can be an ID, class, tag, or any valid CSS selector.
```
let element = document.querySelector('.myClass');
console.log(element);  // Outputs the first element with class 'myClass'
```
### 5. querySelectorAll()
This selector targets all elements that match a specific CSS selector and returns a collection.
```
let elements = document.querySelectorAll('p');
console.log(elements);  // Outputs a collection of all <p> elements
```
Examples:
Selecting by ID:
```
<h1 id="title">Hello World</h1>

<script>
  let title = document.getElementById('title');
  title.textContent = 'Hello, JavaScript!';
</script>
```
Selecting by Class:
```
<p class="description">This is paragraph 1.</p>
<p class="description">This is paragraph 2.</p>

<script>
  let paragraphs = document.getElementsByClassName('description');
  console.log(paragraphs);  // Outputs all paragraphs with class 'description'
</script>
```
Selecting by Tag:
```
<div>Div 1</div>
<div>Div 2</div>

<script>
  let divs = document.getElementsByTagName('div');
  console.log(divs);  // Outputs all <div> elements
</script>
```
Using querySelector():
```
<p class="info">Info 1</p>
<p class="info">Info 2</p>

<script>
  let firstInfo = document.querySelector('.info');
  console.log(firstInfo);  // Outputs the first element with class 'info'
</script>
```
Using querySelectorAll():
```
<p class="info">Info 1</p>
<p class="info">Info 2</p>

<script>
  let allInfo = document.querySelectorAll('.info');
  console.log(allInfo);  // Outputs all elements with class 'info'
</script>
```
Key Takeaway:
Selectors allow you to target HTML elements for manipulation.
There are different types of selectors to target elements by ID, class, tag, or using CSS selectors.

# Scope in JavaScript
Scope in JavaScript refers to the accessibility of variables, functions, and objects in different parts of the code. It determines where variables and functions can be used in your code.

There are two main types of scope:

### 1. Global Scope
When a variable is declared outside of any function or block, it is in the global scope.
Variables in the global scope can be accessed from anywhere in the code.
Example:
```
let name = "Alice";  // Global variable

function greet() {
  console.log(name);  // Can access global variable 'name'
}

greet();  // Output: Alice
console.log(name);  // Output: Alice
```
### 2. Local Scope
Variables declared inside a function or block ({}) are in the local scope.
They can only be accessed within that function or block and are not available outside of it.
Example:
```
function sayHello() {
  let message = "Hello, world!";  // Local variable
  console.log(message);  // Can access 'message' inside the function
}
sayHello();  // Output: Hello, world!
// console.log(message);  // Error: message is not defined (cannot access outside)
```
### 3. Block Scope (with let and const)
Variables declared with let and const inside a block {} are limited to that block.
This is different from var, which is function-scoped.
Example:
```
if (true) {
  let age = 25;  // Block-scoped variable
  console.log(age);  // Output: 25
}

// console.log(age);  // Error: age is not defined (block scope)
```
### 4. Function Scope (with var)
Variables declared with var inside a function are function-scoped, meaning they are only accessible within the function, even if they are declared inside blocks within the function.
Example:
```
function showNumber() {
  if (true) {
    var number = 10;  // Function-scoped variable
  }
  console.log(number);  // Output: 10
}
showNumber();
// console.log(number);  // Error: number is not defined (outside function)
```
### Summary
**Global Scope:** Variables are accessible everywhere in the code.
**Local Scope:** Variables are only accessible within the function or block where they are defined.
**Block Scope:** Variables declared with let and const are confined to the block.
**Function Scope:** Variables declared with var are confined to the function.

# Hoisting in JavaScript
Hoisting is a JavaScript behavior where variables and function declarations are moved to the top of their scope before the code is executed.

For variables, only the declaration is hoisted, not the value.
```
console.log(x);  // Output: undefined
var x = 5;  // Declaration is hoisted, but value is not
```
It's like the above code is understood as:

```
var x;  // Hoisted declaration
console.log(x);  // undefined
x = 5;  // Assigned value
```
//For functions, both the declaration and body are hoisted.
```
greet();  // Output: Hello!
function greet() {
  console.log("Hello!");
}
```
The entire function is hoisted, so you can call it before defining it.
