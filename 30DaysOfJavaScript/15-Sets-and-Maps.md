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