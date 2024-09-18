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
