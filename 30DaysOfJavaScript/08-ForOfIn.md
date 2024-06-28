## For-of and For-in Loop Statements
In this chapter, we will learn about two more loop statements which are very important in JavaScript when we are dealing with Objects.

## For-in Loop
For-in statement loops through the properties of an object.

Syntax:
```javascript
for (variable in array){
    //---code---
}
```

**Example 1:**
```javascript
let programmer = {
    name: 'Shubham',
    tech: 'JS',
    laptop: {
        cpu: 'i5',
        ram: 8,
        brand: 'hp'
    }
}

for (let key in programmer){
    console.log(key);
}
```

Output:
```bash
name
tech
laptop
```

**Example 2:**
```javascript
let programmer = {
    name: 'Shivam',
    tech: 'Java',
    laptop: {
        cpu: 'ryzen 5',
        ram: 8,
        brand: 'hp'
    }
}

for (let x in programmer){
    console.log(x, programmer[x]);
}
```

Output:
```bash
name Shivam
tech Java
laptop {cpu: 'ryzen 5', ram: 8, brand: 'hp'}
```

## For-of Loop
For-of loop statement allows to iterate through various data structures like Arrays, Strings, Maps, NodeLists, etc.

Syntax:
```javascript
for (variable of iterable_data_structure){
    //---code---
}
```
Example:

```javascript
let user = "Hii";
for (let x of user){
    console.log(x + "--");
}
```

Output:
```bash
H--
i--
i--
```

This chapter ends here. I know this was a shorter one. 🙄<br/>
Don't woory, we'll be back with For-of in **ARRAYS IN JAVASCRIPT** along with For-Each. Before that, let us deep drive into **[FUNCTIONS - ❤️Heart of JavaScript](./30DaysOfJavaScript/09-Functions.md)**. 😄😄