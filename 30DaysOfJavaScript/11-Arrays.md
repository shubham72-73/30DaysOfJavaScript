## Arrays in JavaScript
In contrast to variables, an array can store multiple values. Each value in an array has an index, and each index has a reference in a memory address. Each value can be accessed by using their indexes. The index of an array starts from zero, and the index of the last element is less by one from the length of the array.

An array is a collection of different data types which are ordered and changeable(modifiable). An array allows storing duplicate elements and different data types. An array can be empty, or it may have different data type values.

## How to create an empty array
In JavaScript, we can create an array in different ways. Let us see different ways to create an array. It is very common to use const instead of let to declare an array variable. If you ar using const it means you do not use that variable name again.

* Using Array constructor
```javascript
const arr = Array()
// or
// let arr = new Array()
console.log(arr) 
```

Output:
```bash
  []
```

* Using square brackets([])
```javascript
// syntax
// This the most recommended way to create an empty list
const arr = []
console.log(arr)
```
Output:
```bash
  []
```

## How to create an array with values

```javascript
const numbers = [0, 3.14, 9.81, 37, 98.6, 100] // array of numbers
const fruits = ['banana', 'orange', 'mango', 'lemon'] // array of string
console.log(numbers)
console.log(fruits)
```
Output:
```bash
[0, 3.14, 9.81, 37, 98.6, 100]
['banana', 'orange', 'mango', 'lemon']
```

## Accessing array items using index
We access each element in an array using their index. An array index starts from `0`.

```javascript
const fruits = ['banana', 'orange', 'mango', 'lemon']
let firstFruit = fruits[0] // we are accessing the first item using its index

console.log(firstFruit) 

secondFruit = fruits[1]
console.log(secondFruit) 

let lastFruit = fruits[3]
console.log(lastFruit) 
// Last index can be calculated as follows
```

Output:
```bash
banana
orange
lemon
```

## Adding item to an array using push
adding item in the end. To add item to the end of an existing array we use the push method.

```javascript
const arr  = ['item1', 'item2','item3']
arr.push('new item')
console.log(arr)
```

Output:
```bash
['item1', 'item2','item3','new item']
```

