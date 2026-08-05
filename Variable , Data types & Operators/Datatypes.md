# JavaScript Data Types

## What is a Data Type?

A **Data Type** tells JavaScript what kind of value a variable stores.

```javascript
let name = "Rokon"; // String
let age = 23; // Number
```

## Types of Data

JavaScript has **2 main types** of data:

1. Primitive Data Types
2. Non-Primitive (Reference) Data Types

## 1. Primitive Data Types

Primitive data types store a **single value** and are **immutable**.

There are **7 primitive data types**:

| Data Type | Description | Example |
| ---------- | ----------- | ------- |
| String | Text | `"Hello"` |
| Number | Integer or Decimal | `10`, `3.14` |
| Boolean | `true` or `false` | `true` |
| Undefined | Variable declared but not assigned | `undefined` |
| Null | Intentionally empty value | `null` |
| BigInt | Very large integer | `123456789n` |
| Symbol | Unique identifier | `Symbol("id")` |

### Examples

```javascript
let name = "Rokon";
let age = 23;
let isStudent = true;
let city;
let car = null;
let bigNumber = 12345678901234567890n;
let id = Symbol("userId");
```

## 2. Non-Primitive (Reference) Data Types

Non-Primitive data types can store **multiple values** and are stored **by reference**.

### Object

```javascript
const student = {
  name: "Rokon",
  age: 23,
};

console.log(student.name);
```

### Array

```javascript
const fruits = ["Apple", "Mango", "Orange"];

console.log(fruits[0]);
```

### Function

```javascript
function greet() {
  console.log("Hello!");
}

greet();
```

## Primitive vs Non-Primitive

| Feature | Primitive | Non-Primitive |
| -------- | --------- | ------------- |
| Stores | Single Value | Multiple Values |
| Mutable | No | Yes |
| Copied By | Value | Reference |
| Examples | String, Number, Boolean | Object, Array, Function |

### Primitive Example

```javascript
let a = 10;
let b = a;

b = 20;

console.log(a); // 10
console.log(b); // 20
```

**Explanation:** `b` gets a copy of `a`, so changing `b` does not affect `a`.

### Non-Primitive Example

```javascript
let person1 = {
  name: "Rokon",
};

let person2 = person1;

person2.name = "Rahim";

console.log(person1.name); // Rahim
console.log(person2.name); // Rahim
```

**Explanation:** Both variables point to the same object, so changing one also changes the other.

## Easy Way to Remember

- **Primitive** = Each variable has its **own copy**.
- **Non-Primitive** = Multiple variables can point to the **same object**.

## Interview Question

**Q:** What is the difference between Primitive and Non-Primitive Data Types?

**Answer:**  
Primitive data types store a single value and are copied **by value**, while Non-Primitive data types store multiple values and are copied **by reference**.