# JavaScript Objects (Part 1)

## What is an Object?

### Definition

An **Object** is a collection of related data stored as **key-value pairs**.

Objects allow you to store multiple related values in a single variable.

---

## Why Do We Use Objects?

Objects are useful when you want to store information about one thing.

For example:

- User Information
- Product Details
- Student Data
- Employee Information
- Car Details

Instead of creating many variables:

```javascript
let name = "Rokon";
let age = 23;
let country = "Bangladesh";
```

We can use one object.

```javascript
const user = {
    name: "Rokon",
    age: 23,
    country: "Bangladesh"
};
```

---

# Object Structure

```javascript
const user = {
    name: "Rokon",
    age: 23,
    country: "Bangladesh"
};
```

```
Object

user

↓

{

name : "Rokon"

age : 23

country : "Bangladesh"

}
```

Here,

```
name
```

is called the **Key (Property)**

```
"Rokon"
```

is called the **Value**

---

# Creating Objects

There are several ways to create objects.

---

## Method 1 (Most Common)

```javascript
const student = {

    name: "Rokon",

    age: 23,

    cgpa: 3.85

};

console.log(student);
```

### Output

```javascript
{
  name: "Rokon",
  age: 23,
  cgpa: 3.85
}
```

---

## Method 2

Create an empty object.

```javascript
const person = {};

person.name = "Rokon";
person.age = 23;

console.log(person);
```

### Output

```javascript
{
  name: "Rokon",
  age: 23
}
```

---

# Properties

## Definition

A **Property** is a key-value pair inside an object.

---

## Example

```javascript
const laptop = {

    brand: "HP",

    model: "EliteBook",

    ram: "16GB"

};
```

---

### Properties

| Property | Value |
|------------|---------|
| brand | HP |
| model | EliteBook |
| ram | 16GB |

---

Another Example

```javascript
const car = {

    brand: "Toyota",

    color: "Black",

    price: 25000

};
```

---

# Accessing Properties

There are two ways.

---

## 1. Dot Notation (Recommended)

```javascript
const student = {

    name: "Rokon",

    age: 23

};

console.log(student.name);

console.log(student.age);
```

### Output

```
Rokon
23
```

---

## 2. Bracket Notation

```javascript
console.log(student["name"]);

console.log(student["age"]);
```

### Output

```
Rokon
23
```

---

