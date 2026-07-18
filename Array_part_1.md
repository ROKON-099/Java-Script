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

# Array Length

## Definition

The `length` property returns the total number of elements in an array.

---

## Syntax

```javascript
array.length
```

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits.length);
```

### Output

```
3
```

---

## Get Last Element Using length

```javascript
const colors = [

    "Red",

    "Blue",

    "Green",

    "Black"

];

console.log(colors[colors.length - 1]);
```

### Output

```
Black
```

---

# Real Project Example 1

## Student Subjects

```javascript
const subjects = [

    "Math",

    "English",

    "Physics"

];

console.log(subjects[1]);
```

### Output

```
English
```

---

# Real Project Example 2

## Shopping Cart

```javascript
const cart = [

    "Laptop",

    "Mouse"

];

cart.push("Keyboard");

console.log(cart);
```

### Output

```javascript
["Laptop","Mouse","Keyboard"]
```

---

# Real Project Example 3

## Remove Completed Task

```javascript
const tasks = [

    "Study",

    "Exercise",

    "Sleep"
];

tasks.pop();

console.log(tasks);
```

### Output

```javascript
["Study","Exercise"]
```

---

# Real Project Example 4

## Total Products

```javascript
const products = [

    "Phone",

    "Laptop",

    "Monitor",

    "Keyboard"
];

console.log(products.length);
```

### Output

```
4
```

---

# Best Practices

✅ Use `const` when creating arrays.

```javascript
const numbers = [];
```

---

✅ Use meaningful variable names.

```javascript
students

products

orders

employees
```

---

✅ Access the last element using:

```javascript
array[array.length - 1]
```

---

✅ Keep similar data inside one array.

```javascript
["HTML","CSS","JavaScript"]
```

---

# Common Mistakes

## Wrong First Index

Wrong

```javascript
fruits[1]
```

for the first element.

Correct

```javascript
fruits[0]
```

---

## Accessing an Invalid Index

```javascript
console.log(fruits[100]);
```

Output

```
undefined
```

---

## Forgetting Square Brackets

Wrong

```javascript
const fruits = {};
```

Correct

```javascript
const fruits = [];
```

---

## Confusing Array Length with Last Index

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits.length);
```

Output

```
3
```

Last Index

```
2
```

---

# Interview Questions

## What is an Array?

An array is a collection of multiple values stored in a single variable.

---

## What is the first index of an array?

```
0
```

---

## How do you access the first element?

```javascript
array[0]
```

---

## How do you access the last element?

```javascript
array[array.length - 1]
```

---

## How do you update an array element?

```javascript
array[index] = value;
```

---

## Which method adds an element to the end?

```javascript
push()
```

---

## Which method removes the last element?

```javascript
pop()
```

---

## Which property returns the total number of elements?

```javascript
length
```

---

# Summary Table

| Topic | Description | Example |
|--------|-------------|---------|
| Array | Collection of multiple values | `["A","B"]` |
| Create | Create an array | `[]` |
| Access | Get an element | `array[0]` |
| Update | Change an element | `array[1] = "New"` |
| Add | Add to the end | `push()` |
| Remove | Remove from the end | `pop()` |
| Length | Total elements | `array.length` |
| Last Element | Access last item | `array[array.length - 1]` |

---

# Most Frequently Used

⭐⭐⭐⭐⭐

- Array Creation
- Accessing Elements
- Updating Elements
- `push()`
- `pop()`
- `length`

⭐⭐⭐⭐

- Mixed Arrays
- Last Element Access

---

# Final Notes

Arrays are one of the most important data structures in JavaScript. They are used extensively in:

- ✅ React Lists
- ✅ API Responses
- ✅ Shopping Carts
- ✅ User Data
- ✅ Product Lists
- ✅ Database Records

Mastering array creation, indexing, updating, and the `length` property is essential before learning advanced array methods and looping.