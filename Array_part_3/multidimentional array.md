# JavaScript Array Traversal using `for...of`

The **`for...of` loop** is a modern JavaScript loop introduced in **ES6**. It is used to iterate directly over the values of an array.

Unlike the `for` loop, you do not need to use an index.

---

# Table of Contents

- What is `for...of`?
- Why Use `for...of`?
- Syntax
- How it Works
- Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is `for...of`?

## Definition

The `for...of` loop iterates over the **values** of an iterable object such as an array.

---

# Why Use `for...of`?

We use `for...of` to:

- Traverse arrays easily
- Avoid using indexes
- Write cleaner code
- Improve readability

---

# Syntax

```javascript
for(const element of array){

    // code

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

for(const fruit of fruits){

    console.log(fruit);

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

    30

];

for(const number of numbers){

    console.log(number);

}
```

### Output

```javascript
10
20
30
```

---

# Example 3 (Sum of Numbers)

```javascript
const numbers = [

    10,

    20,

    30

];

let sum = 0;

for(const number of numbers){

    sum += number;

}

console.log(sum);
```

### Output

```javascript
60
```

---

# Example 4 (Objects)

```javascript
const users = [

    {

        name: "John"

    },

    {

        name: "Sara"

    }

];

for(const user of users){

    console.log(user.name);

}
```

### Output

```javascript
John
Sara
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

for(const item of cart){

    console.log(item);

}
```

---

# Best Practices

- ✅ Use `for...of` when you only need array values.
- ✅ Use meaningful variable names.
- ✅ Prefer `const` if the value will not change.

---

# Common Mistakes

## Mistake 1

Trying to get the index.

Wrong

```javascript
for(const item of array){

    console.log(item.index);

}
```

`for...of` gives values, **not indexes**.

---

## Mistake 2

Using `for...in` instead of `for...of`.

```javascript
for...in
```

returns indexes.

```javascript
for...of
```

returns values.

---

# Interview Questions

### What does `for...of` iterate over?

Array values.

---

### Does `for...of` provide indexes?

❌ No.

---

### Which version of JavaScript introduced `for...of`?

ES6.

---

# Summary Table

| Feature | Description |
|---------|-------------|
| Loop | `for...of` |
| Iterates Over | Values |
| Index Available | ❌ No |
| Introduced In | ES6 |
| Best Use | Simple array traversal |

---

# Final Notes

The `for...of` loop is cleaner and easier to read than the traditional `for` loop when you only need the array values. It is widely used in modern JavaScript applications.

# JavaScript Array Traversal using `for...of`

The **`for...of` loop** is a modern JavaScript loop introduced in **ES6**. It is used to iterate directly over the values of an array.

Unlike the `for` loop, you do not need to use an index.

---

# Table of Contents

- What is `for...of`?
- Why Use `for...of`?
- Syntax
- How it Works
- Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is `for...of`?

## Definition

The `for...of` loop iterates over the **values** of an iterable object such as an array.

---

# Why Use `for...of`?

We use `for...of` to:

- Traverse arrays easily
- Avoid using indexes
- Write cleaner code
- Improve readability

---

# Syntax

```javascript
for(const element of array){

    // code

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

for(const fruit of fruits){

    console.log(fruit);

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

    30

];

for(const number of numbers){

    console.log(number);

}
```

### Output

```javascript
10
20
30
```

---

# Example 3 (Sum of Numbers)

```javascript
const numbers = [

    10,

    20,

    30

];

let sum = 0;

for(const number of numbers){

    sum += number;

}

console.log(sum);
```

### Output

```javascript
60
```

---

# Example 4 (Objects)

```javascript
const users = [

    {

        name: "John"

    },

    {

        name: "Sara"

    }

];

for(const user of users){

    console.log(user.name);

}
```

### Output

```javascript
John
Sara
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

for(const item of cart){

    console.log(item);

}
```

---

# Best Practices

- ✅ Use `for...of` when you only need array values.
- ✅ Use meaningful variable names.
- ✅ Prefer `const` if the value will not change.

---

# Common Mistakes

## Mistake 1

Trying to get the index.

Wrong

```javascript
for(const item of array){

    console.log(item.index);

}
```

`for...of` gives values, **not indexes**.

---

## Mistake 2

Using `for...in` instead of `for...of`.

```javascript
for...in
```

returns indexes.

```javascript
for...of
```

returns values.

---

# Interview Questions

### What does `for...of` iterate over?

Array values.

---

### Does `for...of` provide indexes?

❌ No.

---

### Which version of JavaScript introduced `for...of`?

ES6.

---

# Summary Table

| Feature | Description |
|---------|-------------|
| Loop | `for...of` |
| Iterates Over | Values |
| Index Available | ❌ No |
| Introduced In | ES6 |
| Best Use | Simple array traversal |

---

# Final Notes

The `for...of` loop is cleaner and easier to read than the traditional `for` loop when you only need the array values. It is widely used in modern JavaScript applications.