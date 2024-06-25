## Our First Program
Let us write our first JavaScript program:
```js
console.log("Hello World");
```
To run this program first save the file in the format `<fileName>.js` and then open terminal.

Now type `node <fileName>.js` in the terminal and press `Enter`.

Alternatively, you can install an Extension named 'Code Runner' in your VS Code to directly run you programs using the Code Runner button located at top-right section of code editor or you can also use shortcut `Ctrl + Alt + N`.

The above program will print `Hello World` in the console.
<br><br>

## Basic Terminology
### Variables
Variables acts as a container for holding data values. We can declare a JavaScript variable by using `var`or `let` (let and const were introduced in ES6). Some rules for naming a variable are as follows:
- Variables can have alphabets.
- Variables can have number except first the letter.
- Special characters doller sign ($) and underscore (_) are allowed.
- Since we cannot use space while naming variables, we can seperate two or more words in a variable name using snake casing (eg: user_name) or camel casing (eg: userName).

### Constant
Constant is also a type of variable whose value cannot be changed. Also, declaration and assigning value to a `const` should be done in the same line otherwise it will result error.

```js
var radius = 3;
const pi = 3.14;
var area = pi*radius*radius;
console.log(area);
```

Here, we don't want to change the value of pi anywhere later in the program so we have used `const` but the value of radius can be changed later in the program.

### Data Types
Data types defines the type of data that we are going to use in our program. In JavaScript, we don't usually need to define the data type but there are two categories of data type in JavaScript. These are: Primitive and Objective.

- **Primitive**: This includes Number, String, Boolean, null, undefined, Symbol.
- **Objective**: Array, function, object, date.

We can find the data type of a variable using `typeof`.
```js
let num = 7.8;
console.log(typeof num);
```
This will print `number`.

To use hexadecimal number, we use 0x before the number to denote that it's a hexadecimal number.
```js
let num = 0xff;
```

### Something more about number...
```js
let num1 = 1.5e12;                  // equals to 1.5*10^12
let num2 = 100_000_000_000_000      // equals to 100000000000000 
/*We can use  underscore in numbers for better understanding*/
let num3 = 18000000000000002n 
```
We should use 'BigInt' if number is very big otherwise some of the last digits will be ignored and will be rounded off. To do this, we have to add `n` at the end of that number (like in num3). Remember that we cannot add normal number to BigInt. We have first convert them also to BigInt.

## Escape Sequences
```js
var a = "This is a single inverted comma '";
var b = 'This is a double inverted comma "';
var c = 'This is a single inverted comma ' and this is a double inverted comma "';
```
It is possible that sometime we would need to use `'` and `"` in same line but here, in `c`, it will create error. So, we need escape sequence to remove special meaning of some special characters at certain points.

We could rewrite the `var c` as below:
```js
var c = 'This is a single inverted comma \' and This is a double inverted comma "';
```
Here, `\'` removes the special meaning of `'` at that point.

List of escape sequence in JavaScript.

- `\'` => for single quote<br> 
- `\"` => for double quote<br> 
- `\\` => for backslash<br> 
- `\b` => for backspace<br> 
- `\f` => form feed<br> 
- `\n` => for next line<br> 
- `\r` => for carriage return<br> 
- `\t` => for horizontal tab<br> 
- `\v` => for vertical tab<br> 

## Coercion and Conversion
JavaScript variables can be converted to a new variable or another data type either by the use of JavaScript function or automatically by javascript itself. 

* By using function
```js
let num1 = String(10);          //number is converted to string
let num2 = Number("55");        //string is converted to number (works if string value contains number only)
```
* Automatically by JS
```js
let x = 10;
x = x + " ";                    //x is now a string
x = x-2;                        //x is now a number
x = !x;                         //x is now a boolean
```

### Convert String to Number
```js
let x = "123Ss";
x = parseInt(x);                //converted to string
console.log(x);
```
There's a condition with parseInt that numbers should be present at starting point. 

### Adding two Strings
```js
let firstName = "John";
let lastName = "Doe";
let fullName = firstName + lastName;
console.log(fullName);
```
This will print `JohnDoe`. To print with space we can add `" "`.
```js
fullname = firstName + " " + lastName;
```

## Template Literals and Interpolation
Nprmal attempt of printing output on console (i.e, using only `''` and `""`) is not considered very efficient if we have large number of variables in the same line. To overcome this, we use **Template Literal** and **Interpolation**.

Template literals use back-ticks (\`) rather than quotes to define strings. backticks are located directly below the `Esc` key. This key has a tidle symbol (~) also.

Template literals provide an easy way to interpolate variables and expressions into strings.

```js
console.log(`${firstName} ${lastName}`);
```
`${}` is used to print the value of the variable. Other things are printed as wriiten inside the backticks.

### List of all falsy values
A boolean expression is that which returns `true` or `false`. Here is a list of all values which return `false`.

* The keyword `false`.
* The number zero (0) or negative zero (-0).
* The BigInt zero (0n, 0x0n, etc.).
* "", '' Empty String values.
* The absence of any value (null).
* The primitive value (undefined).
* NaN - Not a Number

## Semicolon in JavaScript
JavaScript uses ASI (Automatic Semicolon Insertion) so it is not mandatory to use semicolons. However, it is advised to do so because sometimes ASI inserts `;` in a place where it is not required. So, it is safe to use Semicolon (;) and stick with the flow that other programming languages follow.
<br><br>
