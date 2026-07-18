# JavaScript Data Types

## What is a Data Type?

A **data type** tells JavaScript what kind of value a variable stores.

**Example**

```javascript
let name = "Rokon"; // String
let age = 23;       // Number
```

---

# Types of Data

JavaScript has **2 main types** of data.

1. Primitive Data Types
2. Non-Primitive (Reference) Data Types

---

# 1. Primitive Data Types

## Definition

A **Primitive Data Type** stores a **single value**. It is **immutable** (cannot be changed directly).

There are **7 Primitive Data Types** in JavaScript.

| Data Type | Description | Example |
|-----------|-------------|---------|
| String | Text | `"Hello"` |
| Number | Integer or Decimal | `10`, `3.14` |
| Boolean | True or False | `true` |
| Undefined | Variable declared but no value assigned | `undefined` |
| Null | Intentionally empty value | `null` |
| BigInt | Very large integer | `12345678901234567890n` |
| Symbol | Unique identifier | `Symbol("id")` |

---

## Examples

### String

```javascript
let name = "Rokon";
console.log(name);
```

### Number

```javascript
let age = 23;
let price = 99.99;
```

### Boolean

```javascript
let isStudent = true;
```

### Undefined

```javascript
let city;
console.log(city);
```

### Null

```javascript
let car = null;
```

### BigInt

```javascript
let bigNumber = 123456789012345678901234567890n;
```

### Symbol

```javascript
let id = Symbol("userId");
```

---

# 2. Non-Primitive (Reference) Data Types

## Definition

A **Non-Primitive Data Type** can store **multiple values**.

These are called **Reference Types** because they are stored by reference (memory address).

Examples include:

- Object
- Array
- Function

---

## Object

Objects store data in **key-value pairs**.

```javascript
let student = {
    name: "Rokon",
    age: 23,
    country: "Bangladesh"
};

console.log(student.name);
```

---

## Array

An array stores **multiple values** in a single variable.

```javascript
let fruits = ["Apple", "Mango", "Orange"];

console.log(fruits[0]);
```

---

## Function

A function is a reusable block of code.

```javascript
function greet() {
    console.log("Hello!");
}

greet();
```

---

# Primitive vs Non-Primitive

| Feature | Primitive | Non-Primitive |
|---------|-----------|---------------|
| Stores | Single Value | Multiple Values |
| Mutable |  No (Immutable) |  Yes (Mutable) |
| Stored By | Value | Reference |
| Size | Fixed | Dynamic |
| Examples | String, Number, Boolean | Object, Array, Function |

---

# Easy Example

## Primitive

```javascript
let a = 10;
let b = a;

b = 20;

console.log(a); // 10
console.log(b); // 20
```

**Explanation:**
- `b` gets a **copy** of `a`.
- Changing `b` does **not** change `a`.

---

## Non-Primitive

```javascript
let person1 = {
    name: "Rokon"
};

let person2 = person1;

person2.name = "Rahim";

console.log(person1.name); // Rahim
console.log(person2.name); // Rahim
```

**Explanation:**
- `person1` and `person2` point to the **same object**.
- Changing one also changes the other.

---

# Easy Way to Remember

## Primitive =  Single Box

```
age = 23
```

Each variable has its **own copy**.

---

## Non-Primitive = 📍 Address

```
person ------\
              ---> { name: "Rokon" }
friend ------/
```

Both variables point to the **same object** in memory.

---

# Interview Question

**Q: What is the difference between Primitive and Non-Primitive Data Types?**

**Answer:**

- Primitive data types store a **single value** and are copied by **value**.
- Non-primitive data types store **multiple values** and are copied by **reference**.
- Primitive values are immutable, while non-primitive values are mutable.