# JavaScript Arrays (Part 1)

This section covers:

- What is an Array?
- Creating Arrays
- Accessing Array Elements
- Updating Elements
- Adding Elements
- Removing Elements
- Array Length

---

# What is an Array?

## Definition

An **Array** is a special JavaScript object used to store **multiple values in a single variable**.

Each value inside an array is called an **element**.

Every element has an **index**, and indexing starts from **0**.

---

## Why Do We Use Arrays?

Instead of creating multiple variables,

```javascript
let subject1 = "Math";
let subject2 = "English";
let subject3 = "Physics";
```

Use an array.

```javascript
const subjects = ["Math", "English", "Physics"];
```

Arrays make code:

- Easier to read
- Easier to manage
- Easier to loop through
- Easier to modify

---

# Array Structure

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];
```

```
Index

0        1        2

↓

Apple   Mango   Orange
```

---

# Creating Arrays

There are several ways to create arrays.

---

## Method 1 (Most Common)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits);
```

### Output

```javascript
["Apple","Mango","Orange"]
```

---

## Method 2 (Empty Array)

```javascript
const numbers = [];

console.log(numbers);
```

### Output

```javascript
[]
```

---

## Method 3 (Mixed Data Types)

```javascript
const data = [

    "Rokon",

    23,

    true,

    null

];

console.log(data);
```

### Output

```javascript
["Rokon",23,true,null]
```

---

# Accessing Array Elements

## Definition

Array elements are accessed using their **index number**.

Remember:

The first element starts at index **0**.

---

## Syntax

```javascript
array[index]
```

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits[0]);

console.log(fruits[1]);

console.log(fruits[2]);
```

### Output

```
Apple

Mango

Orange
```

---

## Access Last Element

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits[fruits.length - 1]);
```

### Output

```
Orange
```

---

## Access Non-Existing Index

```javascript
const fruits = [

    "Apple",

    "Mango"

];

console.log(fruits[10]);
```

### Output

```
undefined
```

---

# Updating Elements

## Definition

You can change an existing element by assigning a new value to its index.

---

## Syntax

```javascript
array[index] = newValue;
```

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

fruits[1] = "Banana";

console.log(fruits);
```

### Output

```javascript
["Apple","Banana","Orange"]
```

---

## Update Multiple Elements

```javascript
const numbers = [

    10,

    20,

    30

];

numbers[0] = 100;

numbers[2] = 300;

console.log(numbers);
```

### Output

```javascript
[100,20,300]
```

---

# Adding Elements

There are different ways to add elements.

The most common method is **push()**.

(We'll learn `push()` in detail in Part 2.)

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango"

];

fruits.push("Orange");

console.log(fruits);
```

### Output

```javascript
["Apple","Mango","Orange"]
```

---

## Add Multiple Elements

```javascript
const numbers = [

    1,

    2

];

numbers.push(3,4,5);

console.log(numbers);
```

### Output

```javascript
[1,2,3,4,5]
```

---

# Removing Elements

The most common method is **pop()**.

(We'll learn `pop()` in detail in Part 2.)

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

fruits.pop();

console.log(fruits);
```

### Output

```javascript
["Apple","Mango"]
```

---

