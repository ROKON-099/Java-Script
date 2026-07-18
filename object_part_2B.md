
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

