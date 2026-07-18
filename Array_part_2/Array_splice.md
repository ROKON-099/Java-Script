# JavaScript Array Method - splice()

The `splice()` method is one of the most powerful array methods in JavaScript. It is used to **add, remove, or replace elements** in an array.

Unlike `slice()`, the `splice()` method **modifies the original array**.

---

# Table of Contents

- What is splice()?
- Why Use splice()?
- Syntax
- Parameters
- Return Value
- How splice() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is splice()?

## Definition

The `splice()` method changes the contents of an array by:

- Removing elements
- Adding new elements
- Replacing existing elements

It modifies the **original array**.

---

# Why Use splice()?

We use `splice()` when we need to:

- Remove items
- Insert new items
- Replace existing items
- Update array data
- Manage dynamic lists

---

# Syntax

```javascript
array.splice(start, deleteCount);

array.splice(start, deleteCount, item1);

array.splice(start, deleteCount, item1, item2, ...);
```

---

# Parameters

| Parameter | Description |
|-----------|-------------|
| start | Index where the operation begins |
| deleteCount | Number of elements to remove |
| item1, item2... | New elements to insert (Optional) |

---

# Return Value

Returns an array containing the **removed elements**.

The original array is modified.

---

# How splice() Works

Original Array

```javascript
["Apple","Mango","Orange","Banana"]
```

↓

```javascript
splice(1,2)
```

↓

Removed

```javascript
["Mango","Orange"]
```

↓

Remaining Array

```javascript
["Apple","Banana"]
```

---

# Example 1 (Remove Elements)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange",

    "Banana"

];

fruits.splice(1,2);

console.log(fruits);
```

### Output

```javascript
["Apple","Banana"]
```

### Explanation

- Start from index **1**
- Remove **2** elements
- Original array changes

---

# Example 2 (Store Removed Elements)

```javascript
const numbers = [

    10,

    20,

    30,

    40

];

const removed = numbers.splice(1,2);

console.log(removed);

console.log(numbers);
```

### Output

```javascript
[20,30]

[10,40]
```

---

# Example 3 (Add Elements)

```javascript
const colors = [

    "Red",

    "Blue"

];

colors.splice(1,0,"Green");

console.log(colors);
```

### Output

```javascript
["Red","Green","Blue"]
```

### Explanation

- Start at index **1**
- Remove **0** elements
- Insert `"Green"`

---

# Example 4 (Replace Elements)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

fruits.splice(1,1,"Banana");

console.log(fruits);
```

### Output

```javascript
["Apple","Banana","Orange"]
```

---

# Example 5 (Replace Multiple Elements)

```javascript
const numbers = [

    10,

    20,

    30,

    40

];

numbers.splice(1,2,100,200);

console.log(numbers);
```

### Output

```javascript
[10,100,200,40]
```

---

# Example 6 (Insert Multiple Elements)

```javascript
const letters = [

    "A",

    "D"

];

letters.splice(

    1,

    0,

    "B",

    "C"

);

console.log(letters);
```

### Output

```javascript
["A","B","C","D"]
```

---

# Example 7 (Remove All Elements After an Index)

```javascript
const data = [

    1,

    2,

    3,

    4,

    5

];

data.splice(2);

console.log(data);
```

### Output

```javascript
[1,2]
```

### Explanation

Everything from index **2** onward is removed.

---

# Example 8 (Negative Index)

```javascript
const numbers = [

    10,

    20,

    30,

    40

];

numbers.splice(-2,1);

console.log(numbers);
```

### Output

```javascript
[10,20,40]
```

---

# Real Project Example 1

## Remove Product from Shopping Cart

```javascript
const cart = [

    "Laptop",

    "Mouse",

    "Keyboard"

];

const index = cart.indexOf("Mouse");

cart.splice(index,1);

console.log(cart);
```

