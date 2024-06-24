## Objects in JavaScript
In JavaScript, an object is an unordered collection of key-value pairs. Each key-value pair is called a property. The key of a property can be a `string`. The value of a property can be any value, e.g., a `string,` a `number,` an `array,` and even a `function`.

**Note:** JavaScript provides you with many ways to create an object. The most commonly used one is to use the object literal notation.

The following example creates an empty object using the object literal notation:
```javascript

let empty = {}
```
Below example creates an person object using the object literal notation with key-value pairs.The person object has two properties firstName and lastName with the corresponding values 'John' and 'Doe'.

```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe'
};
```

## Accessing properties