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

## When to Use Bracket Notation?

Useful when the property name is stored inside a variable.

```javascript
const student = {

    name: "Rokon",

    age: 23

};

let key = "name";

console.log(student[key]);
```

### Output

```
Rokon
```

---

# Updating Properties

## Definition

You can change the value of an existing property.

---

## Example

```javascript
const student = {

    name: "Rokon",

    age: 23

};

student.age = 24;

console.log(student);
```

### Output

```javascript
{
    name: "Rokon",
    age: 24
}
```

---

## Update Multiple Properties

```javascript
const product = {

    name: "Laptop",

    price: 50000

};

product.price = 45000;

product.name = "Gaming Laptop";

console.log(product);
```

### Output

```javascript
{
    name: "Gaming Laptop",
    price: 45000
}
```

---

# Adding Properties

## Definition

New properties can be added at any time.

---

## Example

```javascript
const student = {

    name: "Rokon"

};

student.age = 23;

student.country = "Bangladesh";

console.log(student);
```

### Output

```javascript
{
    name: "Rokon",
    age: 23,
    country: "Bangladesh"
}
```

---

## Real Project Example

```javascript
const user = {

    name: "John"

};

user.email = "john@gmail.com";

user.role = "Admin";

console.log(user);
```

---

# Deleting Properties

## Definition

The `delete` keyword removes a property from an object.

---

## Syntax

```javascript
delete object.property;
```

---

## Example

```javascript
const student = {

    name: "Rokon",

    age: 23,

    cgpa: 3.90

};

delete student.cgpa;

console.log(student);
```

### Output

```javascript
{
    name: "Rokon",
    age: 23
}
```

---

## Another Example

```javascript
const car = {

    brand: "Toyota",

    color: "Black",

    price: 25000

};

delete car.price;

console.log(car);
```

### Output

```javascript
{
    brand: "Toyota",
    color: "Black"
}
```

---

# CRUD Operations with Objects

| Operation | Description |
|------------|-------------|
| Create | Create a new object |
| Read | Access properties |
| Update | Change property values |
| Delete | Remove properties |

Example

```javascript
const student = {

    name: "Rokon"

};

// Create
student.age = 23;

// Read
console.log(student.name);

// Update
student.age = 24;

// Delete
delete student.name;

console.log(student);
```

---

# Real Project Example

User Profile

```javascript
const user = {

    name: "John",

    email: "john@gmail.com",

    isVerified: true

};

console.log(user.name);

user.isVerified = false;

user.phone = "01712345678";

delete user.email;

console.log(user);
```

---

# Best Practices

✅ Use `const` when creating objects.

```javascript
const user = {};
```

---

✅ Use **dot notation** whenever possible.

```javascript
user.name
```

---

✅ Use meaningful property names.

```javascript
firstName

lastName

email

phone
```

---

# Common Mistakes

## Accessing Wrong Property

```javascript
const user = {

    name: "Rokon"

};

console.log(user.age);
```

Output

```
undefined
```

---

## Forgetting Quotes in Bracket Notation

❌

```javascript
user[name]
```

✅

```javascript
user["name"]
```

---

## Deleting a Non-Existing Property

```javascript
delete user.salary;
```

No error occurs, but nothing is deleted.

---

# Interview Questions

## What is an Object?

An object is a collection of key-value pairs used to store related data.

---

## What is a Property?

A property is a key-value pair inside an object.

---

## How do you access object properties?

- Dot Notation

```javascript
user.name
```

- Bracket Notation

```javascript
user["name"]
```

---

## How do you update a property?

```javascript
user.age = 24;
```

---

## How do you add a property?

```javascript
user.country = "Bangladesh";
```

---

## How do you delete a property?

```javascript
delete user.age;
```

---

# Summary Table

| Topic | Description |
|---------|-------------|
| Object | Collection of key-value pairs |
| Property | Key-value pair inside an object |
| Create | `{}` |
| Access | Dot / Bracket notation |
| Update | `object.property = value` |
| Add | `object.newProperty = value` |
| Delete | `delete object.property` |
| CRUD | Create, Read, Update, Delete |