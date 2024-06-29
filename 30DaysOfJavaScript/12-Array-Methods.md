## Advance Array Methods
Instead of writing regular loop, latest version of JavaScript introduced lots of built in methods which can help us to solve complicated problems. All builtin methods take callback function. In this section, we will see forEach, map, filter, find, and sort.

### forEach
Used to iterate an array elements. We use forEach only with arrays. It takes a callback function with elements, index parameter and array itself. The index and the array optional.

```javascript
let sum = 0;
const numbers = [1, 2, 3, 4, 5];
const add = numbers.forEach((num) => sum+= num)
console.log(add)
```
Output:
```bash
15
```

### map
Used to iterate an array elements and modify the array elements. It takes a callback function with elements, index , array parameter and return a new array.

```javascript
const elements = [2, 3, 4, 1];
const multiply = elements.map((element) => element * 2)
console.log(multiply)
```
Output:
```bash
2
6
8
2
```

### filter
Used to filter out items which full fill filtering conditions and return a new array.

```javascript
const elements = [2, 3, 4, 7];
const even = elements.map((element) => element % 2 == 0)
console.log(even)
```
Output:
```bash
2
4
```
### find
find: Return the first element which satisfies the condition

```javascript
const young = [23, 55, 48, 72];
const age = elements.find((age) => age < 30)
console.log(age)
```
Output:
```bash
23
```

### sort
The sort methods arranges the array elements either ascending or descending order. By default, the sort() method sorts values as strings.This works well for string array items but not for numbers. If number values are sorted as strings and it give us wrong result. Sort method modify the original array. It is recommended to copy the original data before you start using sort method.

```javascript
const products = ['Milk', 'Coffee', 'Sugar', 'Honey', 'Apple', 'Carrot']
console.log(products.sort()) //  
```
Output:
```bash
['Apple', 'Carrot', 'Coffee', 'Honey', 'Milk', 'Sugar']
```
