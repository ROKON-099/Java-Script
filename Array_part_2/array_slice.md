# JavaScript Array Method - slice()

The `slice()` method is one of the most useful array methods in JavaScript. It is used to **copy a portion of an array** into a new array without modifying the original array.

Unlike `splice()`, the `slice()` method **does not change the original array**.

---

# Table of Contents

- What is slice()?
- Why Use slice()?
- Syntax
- Parameters
- Return Value
- How slice() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is slice()?

## Definition

The `slice()` method returns a **shallow copy** of a selected portion of an array.

It copies elements from the original array into a **new array**.

The original array remains unchanged.

---

# Why Use slice()?

We use `slice()` when we need to:

- Copy part of an array
- Get specific elements
- Create a backup of an array
- Display paginated data
- Avoid modifying the original array

---

# Syntax

```javascript
array.slice(start);

array.slice(start, end);
```

---

# Parameters

| Parameter | Description |
|-----------|-------------|
| start | Starting index (included) |
| end | Ending index (excluded, optional) |

---

# Return Value

Returns a **new array** containing the selected elements.

The original array is **not modified**.

---

# How slice() Works

Array

```javascript
["Apple","Mango","Orange","Banana"]
```

↓

```javascript
slice(1,3)
```

↓

New Array

```javascript
["Mango","Orange"]
```

Original Array

```javascript
["Apple","Mango","Orange","Banana"]
```

---

# Example 1 (Basic)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange",

    "Banana"

];

const result = fruits.slice(1,3);

console.log(result);

console.log(fruits);
```

### Output

```javascript
["Mango","Orange"]

["Apple","Mango","Orange","Banana"]
```

### Explanation

- Starts from index **1**
- Stops before index **3**
- Returns a new array
- Original array remains unchanged

---

# Example 2 (Only Start Index)

```javascript
const numbers = [

    10,

    20,

    30,

    40,

    50

];

console.log(numbers.slice(2));
```

### Output

```javascript
[30,40,50]
```

---

# Example 3 (Copy Entire Array)

```javascript
const colors = [

    "Red",

    "Green",

    "Blue"

];

const copy = colors.slice();

console.log(copy);
```

### Output

```javascript
["Red","Green","Blue"]
```

---

# Example 4 (Negative Index)

```javascript
const numbers = [

    10,

    20,

    30,

    40,

    50

];

console.log(numbers.slice(-2));
```

