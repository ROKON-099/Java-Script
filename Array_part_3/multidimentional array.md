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

# JavaScript Multidimensional Arrays

A **Multidimensional Array** is an array that contains one or more arrays as its elements.

The most common multidimensional array is a **2D Array (Two-Dimensional Array)**, but JavaScript also supports **3D Arrays** and even higher dimensions.

They are commonly used to represent:

- Tables
- Matrices
- Chess Boards
- Tic-Tac-Toe Boards
- Seating Arrangements
- Student Mark Sheets

---

# Table of Contents

- What is a Multidimensional Array?
- Why Use Multidimensional Arrays?
- Types of Multidimensional Arrays
- Syntax
- Accessing Elements
- Updating Elements
- Looping Through Multidimensional Arrays
- Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is a Multidimensional Array?

## Definition

A multidimensional array is an array whose elements are themselves arrays.

It allows data to be organized into rows and columns.

---

# Why Use Multidimensional Arrays?

We use multidimensional arrays to:

- Store tabular data
- Represent matrices
- Build game boards
- Manage seating arrangements
- Store student marks
- Process spreadsheet-like data

---

# Types of Multidimensional Arrays

## 1. Two-Dimensional (2D) Array

```javascript
[
    [1,2,3],
    [4,5,6],
    [7,8,9]
]
```

---

## 2. Three-Dimensional (3D) Array

```javascript
[
    [
        [1,2],
        [3,4]
    ],
    [
        [5,6],
        [7,8]
    ]
]
```

---

# Syntax

```javascript
const matrix = [

    [value1, value2],

    [value3, value4]

];
```

---

# Accessing Elements

Use multiple indexes.

```javascript
array[row][column]
```

---

# Example 1 (Access Values)

```javascript
const matrix = [

    [10,20,30],

    [40,50,60],

    [70,80,90]

];

console.log(matrix[0][2]);

console.log(matrix[2][1]);
```

### Output

```javascript
30

80
```

---

# Example 2 (Update Values)

```javascript
const matrix = [

    [1,2],

    [3,4]

];

matrix[1][0] = 100;

console.log(matrix);
```

### Output

```javascript
[
    [1,2],
    [100,4]
]
```

---

# Example 3 (Loop Through 2D Array)

```javascript
const matrix = [

    [1,2],

    [3,4],

    [5,6]

];

for(const row of matrix){

    for(const value of row){

        console.log(value);

    }

}
```

### Output

```javascript
1
2
3
4
5
6
```

---

# Example 4 (Using for Loop)

```javascript
const matrix = [

    [10,20],

    [30,40]

];

for(let i = 0; i < matrix.length; i++){

    for(let j = 0; j < matrix[i].length; j++){

        console.log(matrix[i][j]);

    }

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

# Example 5 (Find Total Sum)

```javascript
const matrix = [

    [1,2,3],

    [4,5,6]

];

let sum = 0;

for(const row of matrix){

    for(const value of row){

        sum += value;

    }

}

console.log(sum);
```

### Output

```javascript
21
```

---

# Example 6 (3D Array)

```javascript
const cube = [

    [

        [1,2],

        [3,4]

    ],

    [

        [5,6],

        [7,8]

    ]

];

console.log(cube[1][0][1]);
```

### Output

```javascript
6
```

---

# Real Project Example 1

## Student Marks

```javascript
const marks = [

    [80,90,85],

    [75,88,92],

    [95,91,89]

];

console.log(marks[2][1]);
```

### Output

```javascript
91
```

---

# Real Project Example 2

## Chess Board

```javascript
const chessBoard = [

    ["♜","♞","♝","♛","♚","♝","♞","♜"],

    ["♟","♟","♟","♟","♟","♟","♟","♟"]

];

console.log(chessBoard[0][3]);
```

### Output

```javascript
♛
```

---

# Real Project Example 3

## Classroom Seating

```javascript
const seats = [

    ["A1","A2","A3"],

    ["B1","B2","B3"],

    ["C1","C2","C3"]

];

console.log(seats[1][2]);
```

### Output

```javascript
B3
```

---

# Real Project Example 4

## Tic-Tac-Toe Board

```javascript
const board = [

    ["X","O","X"],

    ["O","X","O"],

    ["X","","O"]

];

console.log(board[2][0]);
```

### Output

```javascript
X
```

---

# Best Practices

- ✅ Use meaningful variable names.

```javascript
matrix

board

students

marks
```

---

- ✅ Use nested loops for traversal.

---

- ✅ Keep the number of dimensions as low as possible for better readability.

---

- ✅ Check indexes before accessing elements.

---

# Common Mistakes

## Mistake 1

Using only one index.

Wrong

```javascript
matrix[1];
```

Output

```javascript
[40,50,60]
```

Correct

```javascript
matrix[1][2];
```

Output

```javascript
60
```

---

## Mistake 2

Accessing an invalid index.

```javascript
matrix[10][0];
```

This causes an error because

```javascript
matrix[10]
```

is `undefined`.

---

## Mistake 3

Forgetting nested loops.

Wrong

```javascript
for(const row of matrix){

    console.log(row);

}
```

Output

```javascript
[1,2]

[3,4]
```

Correct

```javascript
for(const row of matrix){

    for(const value of row){

        console.log(value);

    }

}
```

---

# Interview Questions

### What is a multidimensional array?

An array that contains one or more arrays as its elements.

---

### What is the most common multidimensional array?

A **2D Array**.

---

### How do you access an element?

```javascript
array[row][column]
```

---

### How do you traverse a multidimensional array?

Using nested loops.

---

### Can JavaScript create a 3D array?

✅ Yes.

---

### Where are multidimensional arrays used?

- Matrices
- Chess Boards
- Tic-Tac-Toe
- Student Results
- Seating Charts
- Tables

---

# Summary Table

| Feature | Description |
|---------|-------------|
| Structure | Array of arrays |
| Common Type | 2D Array |
| Access | `array[row][column]` |
| Traversal | Nested loops |
| Update | `array[row][column] = value` |
| Common Uses | Matrix, Games, Tables, Marksheets |

---

# Quick Comparison

| Feature | Nested Array | Multidimensional Array |
|---------|--------------|------------------------|
| Meaning | Array inside another array | Two or more dimensions |
| Dimensions | Usually one level | Two or more levels |
| Access | `array[0][1]` | `array[row][column]` or `array[x][y][z]` |
| Examples | `[[1,2],[3,4]]` | `[[[1,2],[3,4]],[[5,6],[7,8]]]` |

---

# Final Notes

Multidimensional arrays are an extension of nested arrays and are essential for representing structured data. They are widely used in:

- ✅ Matrices
- ✅ Chess Boards
- ✅ Tic-Tac-Toe Games
- ✅ Student Mark Sheets
- ✅ Seating Arrangements
- ✅ Spreadsheet-like Applications
- ✅ Grid-based Games

Mastering multidimensional arrays will make it much easier to work with complex data structures and prepare you for advanced JavaScript concepts and real-world projects.