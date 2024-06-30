## Destructuring and Spread
Destructuring is a way to unpack arrays, and objects and assigning to a distinct variable.

```javascript
  const numbers = [1, 2, 3]
  let [numOne, numTwo, numThree] = numbers

  console.log(numOne, numTwo, numThree)
```
Output:
```bash
1 2 3
```

```javascript
const fullStack = [
  ['HTML', 'CSS', 'JS', 'React'],
  ['Node', 'Express', 'MongoDB']
]
const [frontEnd, backEnd] = fullStack

console.log(frontEnd)
console.log(backEnd)
```

Output:
```bash
["HTML", "CSS", "JS", "React"]
["Node", "Express", "MongoDB"]
```
If you want to skip one of numbers then use `,` that help you to omit the specific index value.

```javascript
  const numbers = [1, 2, 3]
  let [numOne, , numThree] = numbers

  console.log(numOne, numThree)
```
Output:
```bash
1 3
```

We can not assign variable to all the elements in the array. We can destructure few of the first and we can get the remaining as array using spread operator(...).

```javascript
const nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
let [num1, num2, num3, ...rest] = nums

console.log(num1, num2, num3)
console.log(rest)
```
Output:
```bash
1 2 3
[4, 5, 6, 7, 8, 9, 10]
```
