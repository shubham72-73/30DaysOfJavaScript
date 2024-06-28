## Functions
A function is a block of code which is designed to perfrom some specific task. A function is executed when something "invokes" it.

Syntax:
```javascript
function function_name( parameter1, parameter2, ... ){
    //---code--
}
```

Example:
```javascript
function greet(){
    console.log("Namaste World!");
}           //function definition/ declaration/ statement

greet();    //function call (invokation)
```
Output:
```bash
Namaste World!
```

## Return and Passing
When a `return` statement is used in a function body, the execution of function stops at that point.

```javascript
function greet(){
    return "Hello";
}
greet();                  //Hello
```
We can also pass a value (argument) to the function.

Example:
```javascript
function greet(user){
    return `Hello ${user}`;
}
let user = 'Shubham';
let str = greet(user);
console.log(str);        //Hello Shubham
```

## Function Expression
We can assign a function to a variable just like any other value. Below is an example;
```javascript
let add = function(num1, num2){
    return num1 + num2;
}
let result = add(5,6);
console.log(result);    //11
```
Note that we are not naming the function in case of function expression. We are accessing it using the variable to which it was assigned. But this does not mean we can't name our function in function expression. This is called **Named Function Expression**.

Example:
```javascript
let a = function b(){
    console.log("Hello");
}
a();                    //Hello
```

We can use named function in function expression. However, we can't call b( ) function directly as it will throw error (referenceError). So to call above function, we have used variable 'a'.

## Function default params
```javascript
function add(num1, num2, num3){
    console.log(num1, num2, num3);
    return num1 + num2 + num3;
}
let result = add (5,6);
```

Output:
```bash
5 6 undefined
NaN
```

**Reason:** We have not declared the value of `num3`. <br/>
So to overcome this, we can define a default value like:<br/>
```javascript
function add(num1, num2, num3=1){
    //---code---
}
```
If we do not provide the value of "num3" then the default value '1' will be used. However, if we declare value for "num3" like: `add(5,6,5)` then it will use '5' as the value of num3.

## Arrow Function
Arrow function allows us to write shorter function syntax.
```javascript
let myFunction = (a,b) => a*b;
let hello = () => {
    return "Hello World!";
}
myFunction(5,3);           //15
hello();                   //Hello World!
```

- If the function has only one statement and the statement returns a value, you can remove the brackets and 'return' keyword.<br/>
Example: `let hello = () => "Hello";`

- In fact, if you have only one parameter you can skip parenthesis as well. <br/>
Example: `let hello = val => "Hello" + val;`