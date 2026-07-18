# JavaScript Objects (Part 4)

This section covers:

- Looping Objects (`for...in`)
- Object Destructuring
- Spread Operator with Objects
- Real Project Examples
- Common Mistakes
- Interview Questions
- Summary Table

---

# Looping Objects (for...in)

## Definition

The **for...in** loop is used to iterate over the **keys (properties)** of an object.

It executes once for each enumerable property.

---

## Syntax

```javascript
for (const key in object) {

    // code

}
```

---

## Example

```javascript
const student = {

    name: "Rokon",

    age: 23,

    cgpa: 3.90

};

for(const key in student){

    console.log(key);

}
```

### Output

```
name

age

cgpa
```

---

# Access Values

```javascript
const student = {

    name: "Rokon",

    age: 23,

    cgpa: 3.90

};

for(const key in student){

    console.log(student[key]);

}
```

### Output

```
Rokon

23

3.9
```

---

# Access Keys and Values

```javascript
const student = {

    name: "Rokon",

    age: 23,

    cgpa: 3.90

};

for(const key in student){

    console.log(key, student[key]);

}
```

### Output

```
name Rokon

age 23

cgpa 3.9
```

---

# Why Use Bracket Notation?

Inside a `for...in` loop, `key` is a variable.

```javascript
student[key]
```

Correct

```javascript
student.key
```

Wrong

---

# Object Destructuring

## Definition

Object destructuring extracts properties from an object and stores them in variables.

It makes code shorter and easier to read.

---

## Without Destructuring

```javascript
const user = {

    name: "Rokon",

    age: 23

};

const name = user.name;

const age = user.age;

console.log(name);

console.log(age);
```

Output

```
Rokon

23
```

---

## With Destructuring

```javascript
const user = {

    name: "Rokon",

    age: 23

};

const {name, age} = user;

console.log(name);

console.log(age);
```

### Output

```
Rokon

23
```

---

# Rename Variables

```javascript
const user = {

    name: "Rokon",

    age: 23

};

const {

    name: fullName,

    age: userAge

} = user;

console.log(fullName);

console.log(userAge);
```

### Output

```
Rokon

23
```

---

# Default Values

```javascript
const user = {

    name: "Rokon"

};

const {

    name,

    country = "Bangladesh"

} = user;

console.log(country);
```

### Output

```
Bangladesh
```

---

# Nested Object Destructuring

```javascript
const student = {

    name: "Rokon",

    address: {

        city: "Dhaka"

    }

};

const {

    address: {city}

} = student;

console.log(city);
```

### Output

```
Dhaka
```

---

