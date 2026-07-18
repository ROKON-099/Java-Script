# JavaScript Array Method - shift()

The `shift()` method is one of the most commonly used array methods in JavaScript. It is used to **remove the first element** from an array.

---

# Table of Contents

- What is shift()?
- Why Use shift()?
- Syntax
- Parameters
- Return Value
- How shift() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is shift()?

## Definition

The `shift()` method removes the **first element** from an array.

It shifts all remaining elements one position to the left.

It modifies the **original array** and returns the **removed element**.

---

# Why Use shift()?

We use `shift()` when we need to:

- Remove the first item
- Process a queue
- Remove the oldest notification
- Remove the first task
- Process API data one by one

---

# Syntax

```javascript
array.shift();
```

---

# Parameters

`shift()` does **not** accept any parameters.

```javascript
array.shift();
```

---

# Return Value

`shift()` returns the **removed first element**.

Example

```javascript
const fruits = ["Apple", "Mango", "Orange"];

let removed = fruits.shift();

console.log(removed);
```

### Output

```
Apple
```

---

# How shift() Works

Before

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
shift()
```

↓

Removed

```
Apple
```

↓

After

```javascript
["Mango","Orange"]
```

Notice that every remaining element moves one position to the left.

---

# Example 1 (Basic)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

fruits.shift();

console.log(fruits);
```

### Output

```javascript
["Mango","Orange"]
```

### Explanation

- `"Apple"` is removed.
- `"Mango"` becomes the first element.
- `"Orange"` becomes the second element.
- The original array is modified.

---

# Example 2 (Store Removed Element)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

const removedFruit = fruits.shift();

console.log(removedFruit);

console.log(fruits);
```

### Output

```
Apple

["Mango","Orange"]
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

numbers.shift();

console.log(numbers);
```

### Output

```javascript
[20,30,40]
```

---

# Example 4 (Objects)

