## Conditional in JavaScript
Conditional statements control behavior in JavaScript and determine whether or not pieces of code can run. There are multiple different types of conditionals in JavaScript including:

- “If” statements: where if a condition is true it is used to specify execution for a block of code.
- “Else” statements: where if the same condition is false it specifies the execution for a block of code.
- “Else if” statements: this specifies a new test if the first condition is false.

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


