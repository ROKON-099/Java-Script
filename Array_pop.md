# JavaScript Array Method - pop()

The `pop()` method is one of the most commonly used array methods in JavaScript. It is used to **remove the last element** from an array.

---

# Table of Contents

- What is pop()?
- Why Use pop()?
- Syntax
- Parameters
- Return Value
- How pop() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is pop()?

## Definition

The `pop()` method removes the **last element** from an array.

It modifies the **original array** and returns the **removed element**.

---

# Why Use pop()?

We use `pop()` when we need to:

- Remove the last item
- Delete the latest notification
- Remove the last task
- Implement Undo functionality
- Remove the most recently added product

---

# Syntax

```javascript
array.pop();
```

---

# Parameters

`pop()` does **not** accept any parameters.

```javascript
array.pop();
```

---

# Return Value

`pop()` returns the **removed element**.

Example

```javascript
const fruits = ["Apple", "Mango", "Orange"];

let removed = fruits.pop();

console.log(removed);
```

### Output

```
Orange
```

---

# How pop() Works

Before

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
pop()
```

↓

Removed

```
Orange
```

↓

After

```javascript
["Apple","Mango"]
```

---

# Example 1 (Basic)

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

### Explanation

- `pop()` removes the last element.
- `"Orange"` is removed.
- The original array is modified.

---

# Example 2 (Store Removed Element)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

const removedFruit = fruits.pop();

console.log(removedFruit);

console.log(fruits);
```

### Output

```
Orange

["Apple","Mango"]
```

---

# Example 3 (Numbers)

```javascript
const numbers = [

    10,

    20,

    30,

    40

];

numbers.pop();

console.log(numbers);
```

### Output

```javascript
[10,20,30]
```

---

