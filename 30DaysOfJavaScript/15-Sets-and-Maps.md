## What is Set? 
Set is a collection of elements. Set can only contains unique elements. Let us see how to create a set in the section below.

### Creating an empty set

```javascript
const companies = new Set()
console.log(companies)
```

Output:
```bash
Set(0) {}
```

### Creating set from array
```javascript
const languages = [
  'English',
  'Finnish',
  'English',
  'French',
  'Spanish',
  'English',
  'French',
]

const setOfLanguages = new Set(languages)
console.log(setOfLanguages)
```
Output:
```bash
Set(4) {"English", "Finnish", "French", "Spanish"}
```
**Note:** Set is an iterable object and we can iterate through each elements.

```javascript
const languages = [
  'English',
  'Finnish',
  'English',
  'French',
  'Spanish',
  'English',
  'French',
]

const setOfLanguages = new Set(languages)

for (const language of setOfLanguages) {
  console.log(language)
}
```
Output:
```bash
English
Finnish
French
Spanish
```
### Adding an element to a set
```javascript
const companies = new Set() // creating an empty set
console.log(companies.size) // 0

companies.add('Google') // add element to the set
companies.add('Facebook')
companies.add('Amazon')
companies.add('Oracle')
companies.add('Microsoft')
console.log(companies.size) // 5 elements in the set
console.log(companies)
```
Output:
```bash
Set(5) {"Google", "Facebook", "Amazon", "Oracle", "Microsoft"}
```

**Note:** We can also use loop to add element to a set.

```javascript
const companies = ['Google', 'Facebook', 'Amazon', 'Oracle', 'Microsoft']
setOfCompanies = new Set()
for (const company of companies) {
  setOfCompanies.add(company)
}

```
Output:
```bash
Set(5) {"Google", "Facebook", "Amazon", "Oracle", "Microsoft"}
```

### Deleting an element a set
We can delete an element from a set using a `delete()` method. We gonna delete above set element

```javascript
console.log(companies.delete('Google'))
console.log(companies.size) // 4 elements left in the set
```

### Checking an element in the set
The `has()` method can help to know if a certain element exists in a set.

```javascript
console.log(companies.has('Apple')) // false
console.log(companies.has('Facebook')) // true
```

## What is Map?
Map is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type.

Map has the following properties and methods-

- `new Map()` – creates the map.
- `map.set(key, value)` – stores the value by the key.
- `map.get(key)` – returns the value by the key, undefined if key doesn’t exist in map.
- `map.has(key)` – returns true if the key exists, false otherwise.
- `map.delete(key)` – removes the element (the key/value pair) by the key.
- `map.clear()` – removes everything from the map.
- `map.size` – returns the current element count.

```javascript
let map = new Map();

map.set('1', 'str1');   // a string key
map.set(1, 'num1');     // a numeric key
map.set(true, 'bool1'); // a boolean key

// remember the regular Object? it would convert keys to string
// Map keeps the type, so these two are different:
console.log( map.get(1) ); // 'num1'
console.log( map.get('1') ); // 'str1'

console.log(map.size); // 3
```

**Note:** Map can also use objects as keys.

```javascript
let john = { name: "John" };

// for every user, let's store their visits count
let visitsCountMap = new Map();

// john is the key for the map
visitsCountMap.set(john, 123);

console.log( visitsCountMap.get(john) ); // 123

```

### Iteration over Map
For looping over a map, there are 3 methods:

- `map.keys()` – returns an iterable for keys,
- `map.values()` – returns an iterable for values,
- `map.entries()` – returns an iterable for entries [key, value], it’s used by default in for..of.

```javascript
let recipeMap = new Map([
  ['cucumber', 500],
  ['tomatoes', 350],
  ['onion',    50]
]);

// iterate over keys (vegetables)
for (let vegetable of recipeMap.keys()) {
  console.log(vegetable); // cucumber, tomatoes, onion
}

// iterate over values (amounts)
for (let amount of recipeMap.values()) {
  console.log(amount); // 500, 350, 50
}

// iterate over [key, value] entries
for (let entry of recipeMap) { // the same as of recipeMap.entries()
  console.log(entry); // cucumber,500 (and so on)
}
```
