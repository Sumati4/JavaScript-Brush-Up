# Arrays in JavaScript
What is an Array?
An array is a special type of object in JavaScript that allows you to store multiple values in a single variable. You can think of an array like a list, where each value has a position (or index).

Example:
```
let fruits = ['Apple', 'Banana', 'Mango'];
```
In this example:

'Apple' is at index 0
'Banana' is at index 1
'Mango' is at index 2
## How to Access Elements?
You can access an element by its index:

```
console.log(fruits[0]); // Output: Apple
```
## How to Insert Elements into an Array?
At the end of an array using push():
```
fruits.push('Orange');
console.log(fruits); // Output: ['Apple', 'Banana', 'Mango', 'Orange']
```
## At the beginning of an array using unshift():
```
fruits.unshift('Grapes');
console.log(fruits); // Output: ['Grapes', 'Apple', 'Banana', 'Mango', 'Orange']
```
## How to Remove Elements from an Array?
### From the end of an array using pop():
```
fruits.pop();
console.log(fruits); // Output: ['Grapes', 'Apple', 'Banana', 'Mango']
```
### From the beginning of an array using shift():
```
fruits.shift();
console.log(fruits); // Output: ['Apple', 'Banana', 'Mango']
```
## How to Modify (Replace) an Element?
You can replace an element by directly accessing its index:
```
fruits[1] = 'Strawberry';
console.log(fruits); // Output: ['Apple', 'Strawberry', 'Mango']
```
## How to Sort an Array?
Use the sort() method to sort an array alphabetically or numerically.

### Sort alphabetically:
```
fruits.sort();
console.log(fruits); // Output: ['Apple', 'Mango', 'Strawberry']
```
#### Sort numerically (ascending order):
```
let numbers = [3, 1, 4, 1, 5, 9];
numbers.sort((a, b) => a - b);
console.log(numbers); // Output: [1, 1, 3, 4, 5, 9]
```
## How to Reverse an Array?
Use the reverse() method to reverse the order of elements in the array:
```
fruits.reverse();
console.log(fruits); // Output: ['Strawberry', 'Mango', 'Apple']
```
## Other Useful Array Methods:
**splice()** - Add or remove elements at any position:

```
// Remove 1 element at index 1
fruits.splice(1, 1);
console.log(fruits); // Output: ['Strawberry', 'Apple']

// Add 'Banana' at index 1
fruits.splice(1, 0, 'Banana');
console.log(fruits); // Output: ['Strawberry', 'Banana', 'Apple']
slice() - Create a new array by slicing out a portion:


let someFruits = fruits.slice(0, 2);
console.log(someFruits); // Output: ['Strawberry', 'Banana']
```
## concat() - Join two or more arrays together:

```
let moreFruits = ['Pineapple', 'Grapes'];
let allFruits = fruits.concat(moreFruits);
console.log(allFruits); // Output: ['Strawberry', 'Banana', 'Apple', 'Pineapple', 'Grapes']
```
## How to Loop Through an Array?
### Using for loop:
```

for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
```
## Using forEach():
```
fruits.forEach(fruit => console.log(fruit));
```
## Summary of Common Methods:

- **Insert**: `push()`, `unshift()`
- **Remove**: `pop()`, `shift()`, `splice()`
- **Access**: `[]` (index)
- **Modify**: `[]` (index)
- **Sort**: `sort()`
- **Reverse**: `reverse()`
- **Slice**: `slice()`
- **Join arrays**: `concat()`

# Array Destructuring in JavaScript
## What is Array Destructuring?
Array Destructuring is a convenient way to unpack values from arrays and assign them to variables. Instead of accessing each value manually using indices, you can extract multiple values in a single line of code.

**example**
```
let fruits = ['Apple', 'Banana', 'Mango'];

// Old way (without destructuring):
let firstFruit = fruits[0];
let secondFruit = fruits[1];

// New way (with destructuring):
let [firstFruit, secondFruit] = fruits;

console.log(firstFruit);  // Output: Apple
console.log(secondFruit); // Output: Banana
```
How Does It Work?
When you destructure an array, the values at each index are assigned to variables in the order they appear.

```
let [a, b, c] = [1, 2, 3];
console.log(a); // 1
console.log(b); // 2
console.log(c); // 3
```
Skipping Values
You can also skip values when destructuring by leaving empty spaces:
```
let [first, , third] = ['Red', 'Green', 'Blue'];
console.log(first);  // Output: Red
console.log(third);  // Output: Blue
```
Default Values
If the array has fewer values than the variables you're destructuring, you can set default values.

```
let [a = 1, b = 2, c = 3] = [10];
console.log(a); // 10 (from the array)
console.log(b); // 2  (default value)
console.log(c); // 3  (default value)
```
## Destructuring with Rest Operator (...)
You can also use the rest operator (...) to collect the remaining values into an array.

```
let [first, ...rest] = [10, 20, 30, 40];
console.log(first); // Output: 10
console.log(rest);  // Output: [20, 30, 40]
```
**Practical Example**: Swapping Variables
Array destructuring makes it easy to swap two variables without a temporary variable.

```
let a = 5, b = 10;

// Swap values
[a, b] = [b, a];

console.log(a); // Output: 10
console.log(b); // Output: 5
```
## Summary:
- **Array Destructuring** allows you to unpack array values into variables.
- You can **skip values**, assign **default values**, and use the **rest operator** to collect the rest of the array.
- It’s a clean and simple way to handle arrays in JavaScript!

