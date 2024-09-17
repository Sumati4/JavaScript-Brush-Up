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
How to Access Elements?
You can access an element by its index:

```
console.log(fruits[0]); // Output: Apple
```
How to Insert Elements into an Array?
At the end of an array using push():
```
fruits.push('Orange');
console.log(fruits); // Output: ['Apple', 'Banana', 'Mango', 'Orange']
```
At the beginning of an array using unshift():
```
fruits.unshift('Grapes');
console.log(fruits); // Output: ['Grapes', 'Apple', 'Banana', 'Mango', 'Orange']
```
How to Remove Elements from an Array?
From the end of an array using pop():
```
fruits.pop();
console.log(fruits); // Output: ['Grapes', 'Apple', 'Banana', 'Mango']
```
From the beginning of an array using shift():


fruits.shift();
console.log(fruits); // Output: ['Apple', 'Banana', 'Mango']
How to Modify (Replace) an Element?
You can replace an element by directly accessing its index:

javascript
Copy code
fruits[1] = 'Strawberry';
console.log(fruits); // Output: ['Apple', 'Strawberry', 'Mango']
How to Sort an Array?
Use the sort() method to sort an array alphabetically or numerically.

Sort alphabetically:

javascript
Copy code
fruits.sort();
console.log(fruits); // Output: ['Apple', 'Mango', 'Strawberry']
Sort numerically (ascending order):

javascript
Copy code
let numbers = [3, 1, 4, 1, 5, 9];
numbers.sort((a, b) => a - b);
console.log(numbers); // Output: [1, 1, 3, 4, 5, 9]
How to Reverse an Array?
Use the reverse() method to reverse the order of elements in the array:

javascript
Copy code
fruits.reverse();
console.log(fruits); // Output: ['Strawberry', 'Mango', 'Apple']
Other Useful Array Methods:
splice() - Add or remove elements at any position:

javascript
Copy code
// Remove 1 element at index 1
fruits.splice(1, 1);
console.log(fruits); // Output: ['Strawberry', 'Apple']

// Add 'Banana' at index 1
fruits.splice(1, 0, 'Banana');
console.log(fruits); // Output: ['Strawberry', 'Banana', 'Apple']
slice() - Create a new array by slicing out a portion:

```
let someFruits = fruits.slice(0, 2);
console.log(someFruits); // Output: ['Strawberry', 'Banana']
## concat() - Join two or more arrays together:

```
let moreFruits = ['Pineapple', 'Grapes'];
let allFruits = fruits.concat(moreFruits);
console.log(allFruits); // Output: ['Strawberry', 'Banana', 'Apple', 'Pineapple', 'Grapes']
```
How to Loop Through an Array?
## Using for loop:
```

for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
```
## Using forEach():
```
fruits.forEach(fruit => console.log(fruit));
```
### Summary of Common Methods:
**Insert:** push(), unshift()
**Remove:** pop(), shift(), splice()
**Access:** [] (index)
**Modify:** [] (index)
**Sort:** sort()
**Reverse:** reverse()
**Slice:** slice()
**Join arrays:** concat()
