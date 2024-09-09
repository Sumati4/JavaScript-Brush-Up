# JavaScript Overview

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

This document serves as a simple explanation of JavaScript .

