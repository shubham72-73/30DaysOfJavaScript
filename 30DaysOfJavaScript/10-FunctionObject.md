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