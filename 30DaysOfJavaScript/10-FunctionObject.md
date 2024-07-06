## Function inside Object
We can use function inside an Object.
```javascript
let laptop = {
    cpu: 'i9',
    ram: '16',
    brand: 'hp',
    greet: function(){
        console.log("Hello");
    }
}
laptop.greet();
```

Output:
```bash
Hello
```

## 'This' Keyword
"This" keyword refers to an object that is executing the current piece of code.

```javascript
let hero1 = {
    name: 'Captain America',
    weapon: 'shield',
    lines: 'Avengers Assemble!',
    getDialog: function(){
        console.log(this.lines);
    }
}

let hero2 = {
    name: 'Iron Man',
    weapon: 'suit',
    lines: 'I am Iron Man!',
    getDialog: function(){
        console.log(this.lines);
    }
}

laptop1.getDialog();
```

We can use 'this' keyword for comparing also.

## Constructor function in JavaScript
A constructor is a special function that creates and initializes an object instance of a class. In Javascript, a constructor gets called when an object is created using the `new` keyword. The purpose of a constructor is to create an object and set values for any existing object properties.

```javascript
function Superhero(hero, name){
    this.hero = hero;
    this.name = name;
}

let Superhero1 = new Superhero('Spider Man', 'Peter Parker');
let Superhero2 = new Superhero('Hulk', 'Bruce Banner');

console.log(Superhero1);
console.log(Superhero2);
```

Output:
```bash
Superhero {hero: 'Spider Man', name: 'Peter Parker'}
Superhero {hero: 'Hulk', name: 'Bruce Banner'}
```

We can also add a method to a constuctor.
```javascript
function Superhero(hero, name){
    this.hero = hero;
    this.name = name;
    this.comic = function(){
        console.log("Marvel");
    }
}

let Superhero3 = new Superhero('Thor', 'Thor');
Superhero3.name = 'Thor Odinson';

console.log(Superhero3);
console.comic();
```

Output:
```bash
Superhero{
    hero: 'Thor',
    name: 'Thor Odinson',
    comic: [function(anonymous)]
}
Marvel
```

If `return` does not returns any Object then it will be skipped.