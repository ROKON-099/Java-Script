# JavaScript Array Traversal using `for` Loop

The **`for` loop** is the most commonly used loop for traversing (iterating through) arrays in JavaScript.

It allows you to access every element one by one using its **index**.

---

# Table of Contents

- What is a for Loop?
- Why Use a for Loop?
- Syntax
- How a for Loop Works
- Array Index
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is a for Loop?

## Definition

A `for` loop repeatedly executes a block of code until a specified condition becomes `false`.

When working with arrays, it is mainly used to access every element using its index.

---

# Why Use a for Loop?

We use a `for` loop to:

- Traverse an array
- Print array elements
- Calculate totals
- Search data
- Update array values
- Process API data

---

# Syntax

```javascript
for(initialization; condition; update){

    // code

}
```

---

## Array Syntax

```javascript
for(let i = 0; i < array.length; i++){

    console.log(array[i]);

}
```

---

# Understanding the Loop

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];
```

| Iteration | i | fruits[i] |
|-----------|---|-----------|
| 1 | 0 | Apple |
| 2 | 1 | Mango |
| 3 | 2 | Orange |

When `i` becomes `3`, the condition

```javascript
i < fruits.length
```

becomes

```javascript
3 < 3
```

which is `false`, so the loop stops.

---

# Example 1 (Print All Elements)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

for(let i = 0; i < fruits.length; i++){

    console.log(fruits[i]);

}
```

### Output

```javascript
Apple
Mango
Orange
```

---

# Example 2 (Numbers)

```javascript
const numbers = [

    10,

    20,

    30,

    40

];

for(let i = 0; i < numbers.length; i++){

    console.log(numbers[i]);

}
```

### Output

```javascript
10
20
30
40
```

---

