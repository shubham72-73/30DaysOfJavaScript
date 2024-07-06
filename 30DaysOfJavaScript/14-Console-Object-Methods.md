## Console Object Methods
We will cover about console and console object methods. Absolute beginners usually do not know which to use: `console.log()`.

We use console object methods to show output on the browser console to show output on the browser document(view port). Both methods used only for testing and debugging purposes. The console method is the most popular testing and debugging tool on the browser.

### console.log()
We use console.log() to show output on the browser console. We can substitute values and also we can style the logging out put using %c.

Showing output on browser console or if you have [node.js](https://nodejs.org/en) then it will show output in Terminal. You can check [01 days](./02-Installation.md) to know more about node.js.

```javascript
console.log("30 Days of JavaScript");
```

```bash
30 Days of JavaScript
```
* Subtitution

```javascript
console.log("%d %s Days of JavaScript", 30, "Days");
```

Output:
```bash
30 Days of JavaScript
```

* CSS
We can style logging message using css. Copy the following code.

```javascript
console.log('%c30 Days Of JavaScript', 'color:green') // log output is green
console.log(
  '%c30 Days%c %cOf%c %cJavaScript%c',
  'color:green',
  '',
  'color:red',
  '',
  'color:yellow'
) // log output green red and yellow text
```

### console.warn()
We use console.warn() to give warning on browser. For instance to inform or warn deprecation of version of a package or bad practices.

```javascript
console.warn('This is a warning')
console.warn(
  'You are using React. Do not touch the DOM. Virtual DOM will take care of handling the DOM!'
)
console.warn('Warning is different from error')
```

### console.error()
The console.error() method shows an error messages.

```javascript
console.error('This is an error message')
console.error('We all make mistakes')
```

### console.count()
It prints the number of times the console.count() is called. It takes a string label parameter. It is very helpful to count the number of times a function is called. In the following example,

```javascript
const hello = () => {
    console.count("hello Shivam! called")
}

hello()
hello()
hello()
```
Output:
```bash
hello Shivam! called: 1
hello Shivam! called: 2
hello Shivam! called: 3
```
### console.clear()
The console.clear() cleans the browser console.