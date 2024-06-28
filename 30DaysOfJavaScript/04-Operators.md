## Operators
Operators in JavaScript are the special symbols that perform some process or calculation over the operand(s). There are various types of operators in JavaScript which are:
- Arithmetic operator
- Assignment operator
- Comparison/Relational operator
- String operator
- Logical operator
- Bitwise operator
- Ternary operator
- Typeof operators

## Arithmetic Operators
- ( + ) used to perform addition.
- ( - ) is used to perform subtraction.
- ( * ) is used to perform multiplication.
- ( / ) is used to perform divison.
- ( % ) is used to obtain remainder after division.

We can use `++` and `--` to perform increment and decrement operations.

## Assignment Operator
`=` is the assignment operator and is used to assign values to a variable.

## Relational Operators
Relational operators return true or false based on comparison.
- `>` checks if left hand side is greater than right hand side.
- `<` checks if left hand side is smaller than right hand side.
- `>=` checks if left hand side is greater than or equal to right hand side.
- `<=` checks if left hand side is smaller than or equal to right hand side.
- `==` checks if left hand side is equals to right hand side.
- `===` checks if left hand side is equals to right hand side. It also compares the type of data.

You might get a clear picture of how `==` and `===` works differently from the below example:
```javascript
console.log(1=="1");
```
This will print `true` as it does not compare the datatype.
```javascript
console.log(1==="1");
```
This will print `false` as one of them is a string and other is a number.

For Strings, ASCII value of subsequent characters are compared.
```javascript
console.log("Ball" > "Apple");
```
This will print `true` because ASCII value of B (which is 66) is greater than ASCII value of A (which is 65).

In JavaScript, `===` is preferred more as it compares the values keeping their data types, (i.e., no automatic data type coercion) which is helpful in avoiding bugs.

## Logical Operators
Logical operators return `true` or `false` depending upon the conditions. There are three logical operators in JavaScript. These are as follows:
- AND ( && )
- OR ( || )
- NOT ( ! )
<br/>
<br/>

**AND ( && )** returns `true` if two conditions are true. If any of the two is false, result will be false.

```javascript
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

```javascript
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

```javascript
let result = 5>10;
console.log(!result);
```
Output:
```bash
true
```

## Bitwise Operator
These operators works directly on bits (binary digits) equivalent of a number. In JavaScript, all the numbers are stored as 64 bits floating point numbers, but all bitwise operations are performed on 32 bits. <br/>
So, a number is converted to 32 bits signed integers before bitwise operation is performed on it. <br/>
After the bitwise operation is performed, the result is converted back to 64 bits JavaScript numbers.

### JavaScript Bitwise Operators
- & (AND) - Sets each bit to 1 if both bits are 1.
- | (OR) - Sets each bit to 1 if any one or both bits are 1.
- ^ (XOR) - Sets each bit to 1 if only one of two bits is 1.
- ~ (NOT) - Inverts all the bits.
- << (Zero fill left shift) - Shifts left by pushing zeros in from the right and let the leftmost bits fall off.
- \>> (Signed right shift) - Shifts right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off.
- \>>> (Zero fill right shift) - Shifts right by pushing zeros in from the left, and let the rightmost bits fall off.

## Ternary Operator
Ternary Operator ( ? : ) acts similarly to the 'if-else' statement. If condition is `true`, it returns left side of colon ( : ) and if the condition is `false`, it returns right side of the colon ( : ).

```javascript
let result = 5%2===0 ? "Even" : "Odd";
console.log(result);
```
Output:
```bash
Odd
```

## Typeof Operator
The typeof operator returns the data type of a JavaScript variable.

```javascript
console.log(typeof "Hello");    //string
console.log(typeof 5);          //number
console.log(typeof 5.5);        //number
console.log(typeof true);       //boolean
console.log(typeof 1234n);      //bigint
console.log(typeof a);          //undefined
console.log(typeof NaN);        //number
console.log(typeof null);       //object
```