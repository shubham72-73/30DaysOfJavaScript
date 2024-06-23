## Loops in JavaScript
Let's understand a problem first before start to understand loops. Imagine that you have to print your name 5 time in JavaScript then how will you do that? 🤔
Your answer would be something like the following code.
```javascript
console.log("Shivam");
console.log("Shivam");
console.log("Shivam");
console.log("Shivam");
console.log("Shivam");
```
**Note:** JavaScript loops are essential for efficiently handling repetitive tasks. They execute a block of code repeatedly as long as a specified condition remains true.
Yes! to solve problem like above loop exist. You can achieve same thing in the following few line of code.

```javascript
for(let i = 1; i<=5; i++) {
 console.log("Shivam");
}
```

Output
```javascript
Shivam
Shivam
Shivam
Shivam
Shivam
```

So in simple words, Loop is a sequence of instruction(s) that is executed each time the given condition is `true`.
There are 5 type of loops in JavaScript. These are as follows:

- for loop
- for in loop
- for of loop
- while loop
- do while loop

### For Loop
The above example shows the application of for loop.

Syntax:
```js
for (initialization; condition; increment/decrement){
    statements;
}
```

### While Loop
Statements inside while loop will be executed only when the condition is `true`.

Syntax:
```js
while(condition){
    statements;
    /*incement/decrement operation 
    can also be applied here*/
}
```

Example:
```js
let i = 0;
while (i<5){
    console.log("Shubham");
    i++;
}
```

Output:
```bash
Shubham
Shubham
Shubham
Shubham
Shubham
```

### do-while loop
A do-while loop is somewhat similar to while loop. The difference is that, statement is executed before checking the condition. This means that execution will happen at least once even if the condition is false.

Syntax:
```js
while(condition){
    statements;
    /*incement/decrement operation 
    can also be applied here*/
}
```

Example:
```js
let i = 5;
do{
    console.log("Shubham");
    i++;
}while(i<5)
```

Output:
```bash
Shubham
```

Note that we got output even though the condition was false.

### For of and For in loop
We will cover these loops after we will cover OBJECTS IN JAVASCRIPT which is our next chapter.