
# JavaScript Objects (Part 2B)

This section covers:

- Object.keys()
- Object.values()
- Object.entries()
- Real Project Examples
- Common Mistakes
- Interview Questions
- Summary Table

---

# Object.keys()

## Definition

The `Object.keys()` method returns an **array containing all the property names (keys)** of an object.

It does **not** return the values.

---

## Syntax

```javascript
Object.keys(object)
```

---

## Example

```javascript
const student = {

    name: "Rokon",

    age: 23,

    cgpa: 3.90

};

console.log(Object.keys(student));
```

### Output

```javascript
["name", "age", "cgpa"]
```

---

## Explanation

```
Object

↓

{

name

age

cgpa

}

↓

Object.keys()

↓

["name","age","cgpa"]
```

---

## Store Keys in a Variable

```javascript
const user = {

    name: "John",

    email: "john@gmail.com",

    role: "Admin"

};

const keys = Object.keys(user);

console.log(keys);
```

Output

```javascript
["name","email","role"]
```

---

## Access Individual Keys

```javascript
const person = {

    name: "Rokon",

    country: "Bangladesh"

};

const keys = Object.keys(person);

console.log(keys[0]);

console.log(keys[1]);
```

Output

```
name

country
```

---

# Object.values()

## Definition

The `Object.values()` method returns an **array containing all the values** of an object.

---

## Syntax

```javascript
Object.values(object)
```

---

## Example

```javascript
const student = {

    name: "Rokon",

    age: 23,

    cgpa: 3.90

};

console.log(Object.values(student));
```

### Output

```javascript
["Rokon",23,3.9]
```

---

## Explanation

```
Object

↓

{

name : Rokon

age : 23

cgpa : 3.9

}

↓

Object.values()

↓

["Rokon",23,3.9]
```

---

## Another Example

```javascript
const laptop = {

    brand: "HP",

    ram: "16GB",

    price: 80000

};

console.log(Object.values(laptop));
```

Output

```javascript
["HP","16GB",80000]
```

---

# Object.entries()

## Definition

The `Object.entries()` method returns an array of **key-value pairs**.

Each element is itself an array with two items:

```
[key, value]
```

---

## Syntax

```javascript
Object.entries(object)
```

---

## Example

```javascript
const student = {

    name: "Rokon",

    age: 23

};

console.log(Object.entries(student));
```

### Output

```javascript
[
    ["name","Rokon"],
    ["age",23]
]
```

---

## Explanation

```
Object

↓

{

name : Rokon

age : 23

}

↓

Object.entries()

↓

[

["name","Rokon"],

["age",23]

]
```

---

## Access Individual Entries

```javascript
const user = {

    name: "John",

    age: 30

};

const entries = Object.entries(user);

console.log(entries[0]);

console.log(entries[1]);
```

Output

```javascript
["name","John"]

["age",30]
```

---

# Looping Through Entries

```javascript
const user = {

    name: "Rokon",

    age: 23,

    country: "Bangladesh"

};

for(const [key,value] of Object.entries(user)){

    console.log(key, value);

}
```

Output

```
name Rokon

age 23

country Bangladesh
```

---
# Difference Between keys(), values() and entries()

| Method | Returns |
|---------|----------|
| Object.keys() | Array of Keys |
| Object.values() | Array of Values |
| Object.entries() | Array of Key-Value Pairs |

---

# Real Project Example 1

## Display User Information

```javascript
const user = {

    name: "Rokon",

    email: "rokon@gmail.com",

    role: "Admin"

};

Object.keys(user).forEach(key => {

    console.log(key);

});
```

Output

```
name

email

role
```

---

# Real Project Example 2

## Show Product Values

```javascript
const product = {

    name: "Laptop",

    brand: "HP",

    price: 70000

};

Object.values(product).forEach(value => {

    console.log(value);

});
```

Output

```
Laptop

HP

70000
```

---

# Real Project Example 3

## Create Profile Card

```javascript
const user = {

    Name: "Rokon",

    Age: 23,

    Country: "Bangladesh"

};

for(const [key,value] of Object.entries(user)){

    console.log(`${key}: ${value}`);

}
```

Output

```
Name: Rokon

Age: 23

Country: Bangladesh
```

---

# Real Project Example 4

## Count Object Properties

```javascript
const employee = {

    id: 101,

    name: "John",

    department: "IT",

    salary: 50000

};

console.log(Object.keys(employee).length);
```

Output

```
4
```

---

# Real Project Example 5

## Check if Object is Empty

```javascript
const obj = {};

if(Object.keys(obj).length === 0){

    console.log("Object is Empty");

}
```

Output

```
Object is Empty
```

---

# Best Practices

✅ Use `Object.keys()` when only property names are needed.

---

✅ Use `Object.values()` when only values are required.

---

✅ Use `Object.entries()` when both keys and values are needed.

---

✅ Prefer `for...of` with `Object.entries()` for clean iteration.

```javascript
for(const [key,value] of Object.entries(user)){

    console.log(key,value);

}
```

---

# Common Mistakes

## Forgetting Object.

Wrong

```javascript
keys(user)
```

Correct

```javascript
Object.keys(user)
```

---

## Expecting Object.keys() to Return Values

Wrong expectation

```javascript
Object.keys(user)
```

Output

```javascript
["name","age"]
```

Not

```javascript
["Rokon",23]
```

---

## Confusing entries() with values()

Wrong

```javascript
Object.entries(user)
```

Output

```javascript
[
["name","Rokon"]
]
```

Not

```javascript
["Rokon"]
```

---

## Using for...of Directly on Objects

Wrong

```javascript
for(const item of user){

}
```

Objects are **not iterable**.

Correct

```javascript
for(const item of Object.entries(user)){

}
```

---

# Interview Questions

## What does Object.keys() return?

An array containing all property names.

---

## What does Object.values() return?

An array containing all property values.

---

## What does Object.entries() return?

An array of key-value pairs.

---

## Which method is best for looping through both keys and values?

```javascript
Object.entries()
```

---

## How do you count the number of properties in an object?

```javascript
Object.keys(object).length
```

---

## How do you check whether an object is empty?

```javascript
Object.keys(object).length === 0
```

---

## Which method is most useful for generating dynamic tables or profile cards?

```javascript
Object.entries()
```

---

# Summary Table

| Method | Returns | Common Use |
|---------|----------|------------|
| Object.keys() | Array of Keys | Property names |
| Object.values() | Array of Values | Property values |
| Object.entries() | Array of Key-Value Pairs | Looping, Tables, APIs |

---

# Most Frequently Used

⭐⭐⭐⭐⭐

- Object.keys()

- Object.entries()

⭐⭐⭐⭐

- Object.values()

---

# Final Notes

These methods are widely used in modern JavaScript, React, and Node.js applications:

- ✅ Iterate over API response objects
- ✅ Render dynamic tables and lists
- ✅ Build profile cards
- ✅ Validate object data
- ✅ Count object properties
- ✅ Check if an object is empty

Mastering `Object.keys()`, `Object.values()`, and `Object.entries()` will make working with JSON data, React props/state, and backend API responses much easier.

