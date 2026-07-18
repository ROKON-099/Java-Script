# JavaScript Objects (Part 3)

This section covers:

- Nested Objects
- Nested Array inside Object
- Object inside Array
- Optional Chaining (`?.`)

---

# Nested Objects

## Definition

A **Nested Object** is an object that contains another object as one of its properties.

It allows you to organize related data in a structured way.

---

## Syntax

```javascript
const object = {
    property1: value,
    property2: {
        key1: value,
        key2: value
    }
};
```

---

## Example

```javascript
const student = {

    name: "Rokon",

    age: 23,

    address: {

        city: "Dhaka",

        country: "Bangladesh"

    }

};

console.log(student);
```

### Output

```javascript
{
    name: "Rokon",
    age: 23,
    address: {
        city: "Dhaka",
        country: "Bangladesh"
    }
}
```

---

# Access Nested Properties

Use multiple dots (`.`) to access nested properties.

```javascript
const student = {

    name: "Rokon",

    address: {

        city: "Dhaka",

        country: "Bangladesh"

    }

};

console.log(student.address.city);

console.log(student.address.country);
```

### Output

```
Dhaka

Bangladesh
```

---

# Update Nested Property

```javascript
const student = {

    name: "Rokon",

    address: {

        city: "Dhaka"

    }

};

student.address.city = "Chittagong";

console.log(student.address.city);
```

### Output

```
Chittagong
```

---

# Add Nested Property

```javascript
const student = {

    name: "Rokon",

    address: {}

};

student.address.zipCode = 1207;

console.log(student);
```

### Output

```javascript
{
    name: "Rokon",
    address: {
        zipCode: 1207
    }
}
```

---

# Nested Object Example

```javascript
const company = {

    name: "OpenAI",

    location: {

        country: "USA",

        city: "San Francisco"

    },

    founder: {

        firstName: "Sam",

        lastName: "Altman"

    }

};

console.log(company.location.city);

console.log(company.founder.firstName);
```

### Output

```
San Francisco

Sam
```

---

# Nested Array inside Object

## Definition

An object property can store an array.

This is one of the most common data structures in JavaScript.

---

## Syntax

```javascript
const object = {

    arrayName: []

};
```

---

## Example

```javascript
const student = {

    name: "Rokon",

    skills: [

        "HTML",

        "CSS",

        "JavaScript"

    ]

};

console.log(student.skills);
```

### Output

```javascript
["HTML","CSS","JavaScript"]
```

---

# Access Array Elements

```javascript
console.log(student.skills[0]);

console.log(student.skills[2]);
```

### Output

```
HTML

JavaScript
```

---

# Loop Through Array

```javascript
const student = {

    name: "Rokon",

    skills: [

        "HTML",

        "CSS",

        "JavaScript"

    ]

};

for(const skill of student.skills){

    console.log(skill);

}
```

### Output

```
HTML

CSS

JavaScript
```

---

# Add New Skill

```javascript
student.skills.push("React");

console.log(student.skills);
```

### Output

```javascript
["HTML","CSS","JavaScript","React"]
```

---

# Real Project Example

```javascript
const user = {

    name: "John",

    roles: [

        "Admin",

        "Editor",

        "Manager"

    ]

};

console.log(user.roles[1]);
```

### Output

```
Editor
```

---

# Object inside Array

## Definition

An array can contain multiple objects.

This is the most common structure returned from APIs and databases.

---

## Syntax

```javascript
const array = [

    {},

    {},

    {}

];
```

---

