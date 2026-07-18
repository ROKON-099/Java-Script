# JavaScript Array Traversal using `while` Loop

The **`while` loop** is used to traverse an array when you want to repeat a block of code as long as a condition remains `true`.

Unlike the `for` loop, the initialization and update are written separately.

---

# Table of Contents

- What is a while Loop?
- Why Use a while Loop?
- Syntax
- How it Works
- Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is a while Loop?

## Definition

A `while` loop repeatedly executes a block of code while the specified condition is `true`.

---

# Why Use a while Loop?

We use a `while` loop to:

- Traverse arrays
- Process data until a condition becomes false
- Handle dynamic iterations
- Read unknown-length data

---

# Syntax

```javascript
let i = 0;

while(i < array.length){

    console.log(array[i]);

    i++;

}
```

---

# Example 1 (Print Array)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

let i = 0;

while(i < fruits.length){

    console.log(fruits[i]);

    i++;

}
```

### Output

```javascript
Apple
Mango
Orange
```

---

# Example 2 (Sum of Numbers)

```javascript
const numbers = [

    10,

    20,

    30,

    40

];

let i = 0;

let sum = 0;

while(i < numbers.length){

    sum += numbers[i];

    i++;

}

console.log(sum);
```

### Output

```javascript
100
```

---

# Example 3 (Reverse Traversal)

```javascript
const colors = [

    "Red",

    "Green",

    "Blue"

];

let i = colors.length - 1;

while(i >= 0){

    console.log(colors[i]);

    i--;

}
```

### Output

```javascript
Blue
Green
Red
```

---

# Real Project Example

## Shopping Cart

```javascript
const cart = [

    "Laptop",

    "Mouse",

    "Keyboard"

];

let i = 0;

while(i < cart.length){

    console.log(cart[i]);

    i++;

}
```

---

# Best Practices

- ✅ Always update the loop variable.
- ✅ Use `array.length` instead of fixed numbers.
- ✅ Keep the condition simple.

---

# Common Mistakes

## Forgetting `i++`

Wrong

```javascript
while(i < array.length){

    console.log(array[i]);

}
```

This creates an **infinite loop**.

---

# Interview Questions

### When is a `while` loop useful?

When the number of iterations is not known beforehand.

---

### Does a `while` loop check the condition first?

✅ Yes.

---

# Summary Table

| Feature | Description |
|---------|-------------|
| Loop | `while` |
| Checks Condition | Before execution |
| Runs At Least Once | ❌ No |
| Best Use | Unknown number of iterations |

---

# Final Notes

The `while` loop is useful when the number of iterations is dynamic. For array traversal, `for` is usually preferred because it is shorter and easier to read.