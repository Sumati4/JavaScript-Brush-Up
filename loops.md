# Loops in JavaScript

## What are Loops?

A **loop** is a way to repeat a block of code multiple times. Instead of writing the same code over and over, loops allow you to run the same code with different values or until a condition is met.

### Example:

If you want to print numbers 1 to 5, instead of writing:
```javascript
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
```
You can use a loop to do it in a shorter way:

```
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```
### Types of Loops in JavaScript
## 1. for Loop
A for loop repeats a block of code a specific number of times.

Syntax:
```
for (initialization; condition; increment/decrement) {
  // code to be executed
}
```
Example:
```
for (let i = 0; i < 5; i++) {
  console.log(i);  // Prints numbers 0 to 4
}
```
## 2. while Loop
A while loop repeats a block of code as long as the condition is true.

Syntax:

```
while (condition) {
  // code to be executed
}
```
Example:
```
let i = 0;
while (i < 5) {
  console.log(i);  // Prints numbers 0 to 4
  i++;
}
```
## 3. do...while Loop
A do...while loop is similar to the while loop, but it ensures the code is run at least once before checking the condition.

Syntax:
```
do {
  // code to be executed
} while (condition);
```
Example:
```
let i = 0;
do {
  console.log(i);  // Prints numbers 0 to 4
  i++;
} while (i < 5);
```
## 4. for...of Loop
A for...of loop is used to loop over the values of an iterable (like arrays or strings).

Syntax:
```
for (variable of iterable) {
  // code to be executed
}
```
Example:
```
let fruits = ['apple', 'banana', 'mango'];
for (let fruit of fruits) {
  console.log(fruit);  // Prints each fruit in the array
}
```
## 5. for...in Loop
A for...in loop is used to loop over the properties of an object.

Syntax:
```
for (key in object) {
  // code to be executed
}
```
Example:
```
let car = { brand: 'Toyota', model: 'Corolla', year: 2021 };
for (let key in car) {
  console.log(key + ": " + car[key]);  // Prints each key-value pair in the object
}
```
# Difference Between `for` and `for...of` Loops in JavaScript

## `for` Loop:

- The `for` loop is used to repeat a block of code a specific number of times.
- It works with any kind of data (numbers, arrays, objects), but you need to manually manage the loop counter (index).
  
### Example:
```javascript
let fruits = ['apple', 'banana', 'mango'];

for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);  // Prints each fruit in the array
}

```
## `for...of` Loop:

The `for...of` loop is specifically used to iterate over the **values** of iterable objects like arrays, strings, or sets. 

It is simpler because you don't have to manage an index or counter; it directly gives you the values.

### Example:

```javascript
let fruits = ['apple', 'banana', 'mango'];

for (let fruit of fruits) {
  console.log(fruit);  // Prints each fruit in the array
}
```
## Comparison Table

| **Feature**         | **for Loop**                                                | **for...of Loop**                                |
|---------------------|---------------------------------------------------          |--------------------------------------------------|
| **Purpose**         | Used for general iteration over any data.                   | Specifically used to loop over values of iterables. |
| **Usage**           | Requires manually managing the loop counter.                | Automatically gives you the values of the iterable. |
| **Best For**        | When you need control over the index (e.g., accessing index)| When you want to loop over items in an array or iterable. |
| **Iterates Over**   | Can iterate over anything by index (e.g., arrays, numbers). | Iterates over the values of iterable objects (arrays, strings, sets). |
| **Example Output**  | Outputs array elements using `fruits[i]`.                   | Outputs array elements directly using `fruit`.    |
## Summary:
- Use a `for` loop when you need more control (like accessing the index of each element).
- Use a `for...of` loop for simplicity when you just need the values from an array or iterable.

# Difference Between `for...of` and `for...in` Loops in JavaScript

## `for...of` Loop:

- The `for...of` loop is used to iterate over the **values** of iterable objects like arrays, strings, or sets.
- It is simpler and directly gives you the **values** of the iterable.

### Example:

```javascript
let fruits = ['apple', 'banana', 'mango'];

for (let fruit of fruits) {
  console.log(fruit);  // Prints each fruit in the array
}
```
## `for...in` Loop:

The `for...in` loop is used to iterate over the **keys/properties** of an object (or the indexes of an array).

It gives you the **keys** or **property names** instead of the values.

### Example:

```javascript
let car = { brand: 'Toyota', model: 'Corolla', year: 2021 };

for (let key in car) {
  console.log(key + ": " + car[key]);  // Prints each key-value pair in the object
}
```
## Comparison Table

| **Feature**         | **for...of Loop**                                  | **for...in Loop**                                  |
|---------------------|---------------------------------------------------|----------------------------------------------------|
| **Purpose**         | Loops over values of iterable objects (arrays, strings, sets). | Loops over keys/properties of an object (or indexes of arrays). |
| **Iterates Over**   | Values of arrays, strings, or any iterable.       | Keys or property names of objects or indexes of arrays. |
| **Best For**        | When you need the actual values from the iterable. | When you need to access the keys or properties of an object. |
| **Example Output**  | Prints each value in an array or string.           | Prints each key and value of an object or index and value of an array. |
## Summary:

- Use a `for...of` loop to get the **values** from an array, string, or iterable.
- Use a `for...in` loop to get the **keys** or **indexes** from objects or arrays.
  # `forEach` Loop in JavaScript

## What is the `forEach` Loop?

The `forEach` loop is an array method that executes a provided function once for each element in an array. It is used to perform operations on each element of the array, such as logging values or modifying them.

### Example:

```javascript
let fruits = ['apple', 'banana', 'mango'];

fruits.forEach(function(fruit) {
  console.log(fruit);  // Prints each fruit in the array
});
```

# Comparison of Loop Methods in JavaScript

## Comparison Table:

| **Feature**         | **for Loop**                                      | **for...of Loop**                                  | **for...in Loop**                                  | **forEach Loop**                                 |
|---------------------|---------------------------------------------------|---------------------------------------------------|----------------------------------------------------|--------------------------------------------------|
| **Purpose**         | Used for general iteration over any data.         | Specifically used to loop over values of iterables. | Used to loop over keys/properties of an object (or indexes of arrays). | Used to execute a function for each element in an array. |
| **Usage**           | Requires manually managing the loop counter.      | Automatically gives you the values of the iterable. | Requires manually managing the keys or indexes.    | Directly applies a function to each element in the array. |
| **Best For**        | When you need control over the index (e.g., accessing index). | When you want to loop over items in an array or iterable. | When you need to access the keys or properties of an object. | When you need to perform an operation on each element of an array. |
| **Iterates Over**   | Can iterate over anything by index (e.g., arrays, numbers). | Values of arrays, strings, or any iterable.        | Keys or property names of objects or indexes of arrays. | Values of an array. |
| **Example Output**  | Outputs array elements using `fruits[i]`.         | Outputs array elements directly using `fruit`.     | Prints each key and value of an object or index and value of an array. | Executes a function on each element, such as logging it. |

## Summary:

- Use a `for` loop when you need more control (like accessing the index of each element).
- Use a `for...of` loop for simplicity when you just need the values from an array or iterable.
- Use a `for...in` loop to get the keys or indexes from objects or arrays.
- Use `forEach` when you need to perform an operation on each element of an array, especially when you want to use a function.

  
