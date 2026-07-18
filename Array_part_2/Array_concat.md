# JavaScript Array Method - concat()

The `concat()` method is one of the most useful array methods in JavaScript. It is used to **combine two or more arrays** into a **new array**.

Unlike `push()` or `splice()`, the `concat()` method **does not modify the original array**.

---

# Table of Contents

- What is concat()?
- Why Use concat()?
- Syntax
- Parameters
- Return Value
- How concat() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is concat()?

## Definition

The `concat()` method combines two or more arrays and returns a **new array**.

The original arrays remain unchanged.

---

# Why Use concat()?

We use `concat()` when we need to:

- Merge arrays
- Combine API data
- Join product lists
- Merge student lists
- Keep the original arrays unchanged

---

# Syntax

```javascript
array1.concat(array2);

array1.concat(array2, array3);

array1.concat(value1, value2);
```

---

# Parameters

| Parameter | Description |
|-----------|-------------|
| array2 | Another array to combine |
| array3 | Additional array (Optional) |
| value | Individual value(s) (Optional) |

---

# Return Value

Returns a **new array** containing all merged values.

The original arrays are **not modified**.

---

# How concat() Works

Array 1

```javascript
["Apple","Mango"]
```

+

Array 2

```javascript
["Orange","Banana"]
```

↓

```javascript
concat()
```

↓

New Array

```javascript
["Apple","Mango","Orange","Banana"]
```

---

# Example 1 (Basic)

```javascript
const fruits1 = [

    "Apple",

    "Mango"

];

const fruits2 = [

    "Orange",

    "Banana"

];

const allFruits = fruits1.concat(fruits2);

console.log(allFruits);
```

### Output

```javascript
["Apple","Mango","Orange","Banana"]
```

### Explanation

- `fruits1` and `fruits2` are merged.
- A new array is created.
- The original arrays remain unchanged.

---

# Example 2 (Three Arrays)

```javascript
const a = [1,2];

const b = [3,4];

const c = [5,6];

const result = a.concat(b,c);

console.log(result);
```

### Output

```javascript
[1,2,3,4,5,6]
```

---

# Example 3 (Array + Values)

```javascript
const numbers = [

    10,

    20

];

const result = numbers.concat(

    30,

    40

);

console.log(result);
```

### Output

```javascript
[10,20,30,40]
```

---

# Example 4 (Empty Array)

```javascript
const numbers = [];

const result = numbers.concat(

    100,

    200

);

console.log(result);
```

### Output

```javascript
[100,200]
```

---

