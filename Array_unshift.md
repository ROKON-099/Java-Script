# JavaScript Array Method - unshift()

The `unshift()` method is one of the most commonly used array methods in JavaScript. It is used to **add one or more elements to the beginning** of an array.

---

# Table of Contents

- What is unshift()?
- Why Use unshift()?
- Syntax
- Parameters
- Return Value
- How unshift() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is unshift()?

## Definition

The `unshift()` method adds one or more elements to the **beginning** of an array.

It shifts all existing elements one position to the right.

It modifies the **original array** and returns the **new length** of the array.

---

# Why Use unshift()?

We use `unshift()` when we need to:

- Add an item to the beginning
- Add the newest notification first
- Add a new task at the top
- Insert priority items
- Manage queue systems

---

# Syntax

```javascript
array.unshift(element1);

array.unshift(element1, element2, element3);
```

---

# Parameters

| Parameter | Description |
|-----------|-------------|
| element1 | First element to add |
| element2 | Second element (Optional) |
| element3 | Third element (Optional) |

You can add one or more elements at once.

---

# Return Value

`unshift()` returns the **new length** of the array.

Example

```javascript
const fruits = ["Mango", "Orange"];

let length = fruits.unshift("Apple");

console.log(length);
```

### Output

```
3
```

---

# How unshift() Works

Before

```javascript
["Mango","Orange"]
```

↓

```javascript
unshift("Apple")
```

↓

After

```javascript
["Apple","Mango","Orange"]
```

All existing elements move one position to the right.

---

# Example 1 (Basic)

```javascript
const fruits = [

    "Mango",

    "Orange"

];

fruits.unshift("Apple");

console.log(fruits);
```

### Output

```javascript
["Apple","Mango","Orange"]
```

### Explanation

- `"Apple"` is added to the beginning.
- `"Mango"` moves to index `1`.
- `"Orange"` moves to index `2`.
- The original array is modified.

---

# Example 2 (Numbers)

```javascript
const numbers = [

    20,

    30,

    40

];

numbers.unshift(10);

console.log(numbers);
```

### Output

```javascript
[10,20,30,40]
```

---

# Example 3 (Multiple Elements)

```javascript
const colors = [

    "Green",

    "Blue"

];

colors.unshift(

    "Red",

    "Black"

);

console.log(colors);
```

### Output

```javascript
["Red","Black","Green","Blue"]
```

---

# Example 4 (Store Return Value)

```javascript
const fruits = [

    "Mango",

    "Orange"

];

const newLength = fruits.unshift("Apple");

console.log(newLength);

console.log(fruits);
```

### Output

```
3

["Apple","Mango","Orange"]
```

---

