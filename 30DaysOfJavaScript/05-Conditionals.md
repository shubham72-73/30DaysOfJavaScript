## Conditional in JavaScript
Conditional statements control behavior in JavaScript and determine whether or not pieces of code can run. There are multiple different types of conditionals in JavaScript including:

- “If” statements: where if a condition is true it is used to specify execution for a block of code.
- “Else” statements: where if the same condition is false it specifies the execution for a block of code.
- “Else if” statements: this specifies a new test if the first condition is false.
- "Switch" statements: It executes a particular block of code based on the given conditions.

### If Statement Example
As the most common type of conditional, the if statement only runs if the condition enclosed in parentheses () is truthy.

```javascript
let age = 18
if (age > 5) {
 console.log("You're eligible to take license")
}
​
```
Output
```bash
You're eligible to take license
```

### Else Statement Example
You can extend an if statement with an else statement, which adds another block to run when the if conditional doesn’t pass.

```javascript
let age = 18
if (age < 5) {
 console.log("You're eligible to take license")
} else {
 console.log("You're not eligible to take license")
}
​
```
Output
```bash
You're not eligible to take license
```

### Else if Statement Example
You can also extend an if statement with an else if statement, which adds another conditional with its own block.

```javascript
let age = 17
if (age <= 5) {
 console.log("You're eligible to take license")
} else if ( age === 17) {
 console.log("You will be eligible next year to take license")
} else {
 console.log("You're not eligible to take license")
}
​
```
Output
```bash
You will be eligible next year to take license
```

### Switch Statement Example
Switch statement is a control flow structure that allows you to execute different blocks of code depending on the value of an expression or variable.

```js
switch (expression) {
  case value1:
    // code to execute if expression === value1
    break;
  case value2:
    // code to execute if expression === value2
    break;
  ...
  default:
    // code to execute if no case matches
}
```
If we do not use 'break' statement, all the cases will be executed which are written after the matched case. <br/>
Other thing to be noted is that we can use a 'default' statement which will be executed when none of the case is matched.

```js
let num = 1;
switch (num){
    case 5:
        console.log("Number is 5");
        break;
    case 10:
        console.log("Number is 10");
        break;
    default:
        console.log("Neither 5 nor 10");
}
```