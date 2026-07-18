# JavaScript Array Method - reverse()

The `reverse()` method is one of the most commonly used array methods in JavaScript. It is used to **reverse the order of elements** in an array.

Unlike `slice()` and `concat()`, the `reverse()` method **modifies the original array**.

---

# Table of Contents

- What is reverse()?
- Why Use reverse()?
- Syntax
- Parameters
- Return Value
- How reverse() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is reverse()?

## Definition

The `reverse()` method reverses the order of the elements in an array.

It changes the **original array** and also returns the reversed array.

---

# Why Use reverse()?

We use `reverse()` when we need to:

- Reverse a list
- Display the latest items first
- Reverse a playlist
- Reverse search history
- Process data from last to first

---

# Syntax

```javascript
array.reverse();
```

---

# Parameters

The `reverse()` method does **not** take any parameters.

```javascript
array.reverse();
```

---

# Return Value

Returns the **same array** after reversing its elements.

The original array is modified.

---

# How reverse() Works

Original Array

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
reverse()
```

↓

Result

```javascript
["Orange","Mango","Apple"]
```

---

# Example 1 (Basic)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

fruits.reverse();

console.log(fruits);
```

### Output

```javascript
["Orange","Mango","Apple"]
```

### Explanation

The elements are reversed in place.

---

# Example 2 (Numbers)

```javascript
const numbers = [

    10,

    20,

    30,

    40

];

numbers.reverse();

console.log(numbers);
```

### Output

```javascript
[40,30,20,10]
```

---

# Example 3 (Store Return Value)

```javascript
const colors = [

    "Red",

    "Green",

    "Blue"

];

const result = colors.reverse();

console.log(result);

console.log(colors);
```

### Output

```javascript
["Blue","Green","Red"]

["Blue","Green","Red"]
```

Both variables reference the same reversed array.

---

# Example 4 (Single Element)

```javascript
const items = [

    "Laptop"

];

items.reverse();

console.log(items);
```

### Output

```javascript
["Laptop"]
```

---

# Example 5 (Empty Array)

```javascript
const data = [];

data.reverse();

console.log(data);
```

### Output

```javascript
[]
```

---

# Example 6 (Mixed Data Types)

```javascript
const values = [

    "JavaScript",

    100,

    true,

    null

];

values.reverse();

console.log(values);
```

### Output

```javascript
[null,true,100,"JavaScript"]
```

---

