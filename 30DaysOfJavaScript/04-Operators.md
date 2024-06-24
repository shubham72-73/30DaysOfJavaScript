## Operators
Operators in JavaScript are the special symbols that perform some process or calculation over the operand(s). There are various types of operators in JavaScript which are:
- Arithmetic operator
- Assignment operator
- Comparison/Relational operator
- String operator
- Logical operator
- Bitwise operator
- Ternary operator
- Type operators

### Arithmetic Operators
- ( + ) used to perform addition.
- ( - ) is used to perform subtraction.
- ( * ) is used to perform multiplication.
- ( / ) is used to perform divison.
- ( % ) is used to obtain remainder after division.

We can use `++` and `--` to perform increment and decrement operations.

### Assignment Operator
`=` is the assignment operator and is used to assign values to a variable.

### Relational Operators
Relational operators return true or false based on comparison.
- `>` checks if left hand side is greater than right hand side.
- `<` checks if left hand side is smaller than right hand side.
- `>=` checks if left hand side is greater than or equal to right hand side.
- `<=` checks if left hand side is smaller than or equal to right hand side.
- `==` checks if left hand side is equals to right hand side.
- `===` checks if left hand side is equals to right hand side. It also compares the type of data.

You might get a clear picture of how `==` and `===` works differently from the below example:
```js
console.log(1=="1");
```
This will print `true` as it does not compare the datatype.
```js
console.log(1==="1");
```
This will print `false` as one of them is a string and other is a number.

For Strings, ASCII value of subsequent characters are compared.
```js
console.log("Ball" > "Apple");
```
This will print `true` because ASCII value of B (which is 66) is greater than ASCII value of A (which is 65).

In JavaScript, `===` is preferred more as it compares the values keeping their data types, (i.e., no automatic data type coercion) which is helpful in avoiding bugs.

### Logical Operators
Logical operators return `true` or `false` depending upon the conditions. There are three logical operators in JavaScript. These are as follows:
- AND ( && )
- OR ( || )
- NOT ( ! )
<br/>
<br/>

**AND ( && )** returns `true` if two conditions are true. If any of the two is false, result will be false.

```js
let result1 = 2<5 && 7<10;
let result2 = 2<5 && 7>10;
console.log(result1);
console.log(result2);
```
Output:
```bash
true
false
```

<br/>

**OR ( || )** returns `true` if any one or both of the conditions are true. It returns `false` only if both the conditions are false.

```js
let result1 = 2<5 || 7<10;
let result2 = 2<5 || 7>10;
let result3 = 2>5 || 7>10;
console.log(result1);
console.log(result2);
console.log(result3);
```
Output:
```bash
true
true
false
```
<br/>

**NOT ( ! )** just reverse the output i.e., it returns `true` for false conditions and `false` for true conditions.

```js
let result = 5>10;
console.log(!result);
```
Output:
```bash
true
```