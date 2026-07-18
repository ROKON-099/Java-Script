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

# Example 3 (Using Index)

```javascript
const colors = [

    "Red",

    "Green",

    "Blue"

];

for(let i = 0; i < colors.length; i++){

    console.log(i, colors[i]);

}
```

### Output

```javascript
0 Red

1 Green

2 Blue
```

---

# Example 4 (Sum of Array)

```javascript
const numbers = [

    10,

    20,

    30,

    40

];

let sum = 0;

for(let i = 0; i < numbers.length; i++){

    sum += numbers[i];

}

console.log(sum);
```

### Output

```javascript
100
```

---

# Example 5 (Find Largest Number)

```javascript
const numbers = [

    20,

    60,

    15,

    80,

    40

];

let largest = numbers[0];

for(let i = 1; i < numbers.length; i++){

    if(numbers[i] > largest){

        largest = numbers[i];

    }

}

console.log(largest);
```

### Output

```javascript
80
```

---

# Example 6 (Print Even Numbers)

```javascript
const numbers = [

    2,

    5,

    8,

    11,

    20

];

for(let i = 0; i < numbers.length; i++){

    if(numbers[i] % 2 === 0){

        console.log(numbers[i]);

    }

}
```

### Output

```javascript
2
8
20
```

---

# Example 7 (Update Every Element)

```javascript
const prices = [

    100,

    200,

    300

];

for(let i = 0; i < prices.length; i++){

    prices[i] = prices[i] + 50;

}

console.log(prices);
```

### Output

```javascript
[150,250,350]
```

---

# Example 8 (Reverse Traversal)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

for(let i = fruits.length - 1; i >= 0; i--){

    console.log(fruits[i]);

}
```

### Output

```javascript
Orange
Mango
Apple
```

---

# Example 9 (Search an Element)

```javascript
const students = [

    "Rahim",

    "Karim",

    "Rokon"

];

let found = false;

for(let i = 0; i < students.length; i++){

    if(students[i] === "Rokon"){

        found = true;

        break;

    }

}

console.log(found);
```

### Output

```javascript
true
```

---

# Example 10 (Count Elements)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange",

    "Banana"

];

let count = 0;

for(let i = 0; i < fruits.length; i++){

    count++;

}

console.log(count);
```

### Output

```javascript
4
```

---

# Real Project Example 1

## Shopping Cart

```javascript
const cart = [

    "Laptop",

    "Mouse",

    "Keyboard"

];

for(let i = 0; i < cart.length; i++){

    console.log(cart[i]);

}
```

---

# Real Project Example 2

## Student Result

```javascript
const marks = [

    80,

    75,

    95

];

let total = 0;

for(let i = 0; i < marks.length; i++){

    total += marks[i];

}

console.log(total);
```

### Output

```javascript
250
```

---

# Real Project Example 3

## Product Price

```javascript
const prices = [

    100,

    200,

    300

];

for(let i = 0; i < prices.length; i++){

    console.log("Price:", prices[i]);

}
```

---

# Real Project Example 4

## Attendance List

```javascript
const students = [

    "Rahim",

    "Karim",

    "Rokon"

];

for(let i = 0; i < students.length; i++){

    console.log("Present:", students[i]);

}
```

---

# Best Practices

✅ Use `array.length` instead of writing fixed numbers.

```javascript
for(let i = 0; i < array.length; i++)
```

---

✅ Use meaningful variable names.

```javascript
students

products

prices

marks
```

---

✅ Keep loop logic simple and readable.

---

# Common Mistakes

## Mistake 1

Using `<=`

Wrong

```javascript
for(let i = 0; i <= array.length; i++)
```

Correct

```javascript
for(let i = 0; i < array.length; i++)
```

---

## Mistake 2

Forgetting `i++`

Wrong

```javascript
for(let i = 0; i < array.length;){

}
```

This creates an infinite loop.

---

## Mistake 3

Starting from the wrong index.

Wrong

```javascript
for(let i = 1; i < array.length; i++)
```

This skips the first element.

---

## Mistake 4

Accessing an invalid index.

```javascript
array[array.length]
```

returns

```javascript
undefined
```

---

# Interview Questions

### What is the purpose of a `for` loop?

It repeats a block of code until a condition becomes false.

---

### Why is `array.length` used?

To avoid going beyond the last element.

---

### Which index does an array start from?

```javascript
0
```

---

### How do you print an array in reverse order?

```javascript
for(let i = array.length - 1; i >= 0; i--){

    console.log(array[i]);

}
```

---

### How do you find the sum of all elements?

Use a variable and add each element inside the loop.

---

# Summary Table

| Feature | Description |
|---------|-------------|
| Loop | `for` |
| Purpose | Traverse an array |
| Starts From | `0` |
| Ends At | `array.length - 1` |
| Access Element | `array[i]` |
| Changes Array | Optional |
| Common Uses | Print, Search, Sum, Update, Traverse |

---

# Final Notes

The **`for` loop** is the foundation of array traversal in JavaScript. Before learning advanced methods like `for...of`, `map()`, `filter()`, and `reduce()`, you should be comfortable using the `for` loop because it gives you complete control over the array index and iteration process.