## Objects in JavaScript
In JavaScript, an object is an unordered collection of key-value pairs. Each key-value pair is called a property. The key of a property can be a `string`. The value of a property can be any value, e.g., a `string,` a `number,` an `array,` and even a `function`.

**Note:** JavaScript provides you with many ways to create an object. The most commonly used one is to use the object literal notation.

The following example creates an empty object using the object literal notation:
```javascript
let empty = {}
```
Below example creates an person object using the object literal notation with key-value pairs. The `person` object has two properties `firstName` and `lastName` with the corresponding values 'John' and 'Doe'.

```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe'
};
```

## Accessing properties
To can print the objects like any other variable.

```javascript
console.log(person);
```
Output:
```bash
{firstName:'John',lastName:'Doe'}
```

To fetch a particular value we can use dot ( . ) operator or square bracket ( [ ] ).

```javascript
console.log(person.firstName);
console.log(person["firstName"]);
```
Output:
```bash
John
John
```

### Dot vs Square Bracket
Both Dot operator and Square Bracket are used to access the properties of Object. Both works fine and nearly in the same way. The difference is Square Brackets works even if the value that is serving as the `key`, is coming from some expression. <br>Let us see an example to be more clear.

```javascript
let mobile = {
    brand: "Nokia",
    type: "Smartphone"
};
let name = "brand";

console.log(mobile.name);       //undefined

console.log(mobile[name]);      //Nokia

console.log(mobile["name"]);    //undefined

console.log(mobile["brand"]);   //Nokia
```

If you have noticed, you will find that the expression we passed to the square brackets, is a variable. Passing string value will give `undefined` if none of the `key` matches to that string.

We can also modify or add new property to the objects. This also can be done by both ( . ) and ( [ ] ).

### Modifying value inside an Object
```javascript
let mobile = {
    brand: "Nokia",
    type: "Smartphone"
};

mobile.brand = "Samsung";

mobile["type"] = "Feature Phone";

console.log(mobile);
```

Output:

```bash
{
    brand:'Samsung',
    type:'Feature Phone'
}
```

Here, we modified the value of `brand` using dot operator and the value of `type` using square brackets. You can use any of the two.

### Adding new Property
You can also add new property to the Objects. Let us see an example.
```javascript
let mobile = {
    brand: "Motorola",
    type: "Smartphone"
};

mobile.camera = "50MP";

mobile["processor"] = "Snapdragon";

console.log(mobile);
```

Output:
```bash
{
    brand:'Motorola',
    type:'Smartphone',
    camera:'50MP',
    processor:'Snapdragon'
}
```

<br/>

## Complex Objects
Complex objects are the objects that are built from a smaller or a collection of objects.

```javascript
let mcu = {
    totalPhases: '6',
    movies: '34',
    phaseOne: {
        name: 'Avengers Assembled',
        totalMovies: '6'
    }
};

console.log(mcu);
```

```bash
{
    totalPhases:'6',
    movies:'34',
    phaseOne:{
        name:'Avengers Assembled',
        totalMovies:'6'
    }
}
```

We can access the values in Complex Objects similarly how we have done in Simple Objects.

```javascript
console.log(mcu.phaseOne.name);     //Avengers Assembled
```
We will get `undefined` if we try to access a value that does not exist.

```javascript
console.log(mcu.phaseTwo);          //undefined
```
<br/>

## Nullish Coalescing Operator (??)
A logical operator that returns its right-hand-side operand when its left-hand-side opened is null or defined. Otherwise, returns its left-hand-side operand.

```javascript
let mcu = {
    totalPhases: '6',
    movies: '34',
    phaseOne: {
        name: 'Avengers Assembled',
        totalMovies: '6'
    }
};

console.log(mcu.phaseOne??name);    //Avengers Assembled

console.log(mcu.phaseTwo??name);    //undefined
```

We can also delete something from Object using delete.
```javascript
let mcu = {
    totalPhases: '6',
    movies: '34',
    phaseOne: {
        name: 'Avengers Assembled',
        totalMovies: '6'
    }
};

delete mcu.phaseOne;

console.log(mcu);
```
Output:
```bash
{
    totalPhases: '6',
    movies: '34'
}
```

Since we have learned about Objects, we are now ready to take a look into For-of and For-in Loop statements.

So our next Chapter will focus on these two Loop Statements which are **[For-Of and For-In](./08-For-of-in.md)**.