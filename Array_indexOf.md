# JavaScript Array Method - indexOf()

The `indexOf()` method is one of the most commonly used array methods in JavaScript. It is used to find the **index (position)** of a specific element in an array.

If the element is not found, it returns **-1**.

---

# Table of Contents

- What is indexOf()?
- Why Use indexOf()?
- Syntax
- Parameters
- Return Value
- How indexOf() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is indexOf()?

## Definition

The `indexOf()` method searches an array for a specified element and returns the **index of its first occurrence**.

If the element does not exist, it returns

```javascript
-1
```

It **does not modify** the original array.

---

# Why Use indexOf()?

We use `indexOf()` when we need to:

- Find an element's position
- Check if a value exists
- Remove an item using its index
- Update an element
- Search data inside an array

---

# Syntax

```javascript
array.indexOf(value);

array.indexOf(value, startIndex);
```

---

# Parameters

| Parameter | Description |
|-----------|-------------|
| value | The value to search for |
| startIndex | Optional. The index to start searching from |

---

# Return Value

Returns

- Index of the first matching element
- `-1` if the value is not found

---

# How indexOf() Works

Array

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
indexOf("Mango")
```

↓

Result

```javascript
1
```

---

Array

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
indexOf("Banana")
```

↓

Result

```javascript
-1
```

---

# Example 1 (Basic)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits.indexOf("Mango"));
```

### Output

```javascript
1
```

### Explanation

"Mango" is located at index **1**.

---

# Example 2 (Value Not Found)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits.indexOf("Banana"));
```

### Output

```javascript
-1
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

console.log(numbers.indexOf(30));
```

### Output

```javascript
2
```

---

# Example 4 (Duplicate Values)

```javascript
const numbers = [

    10,

    20,

    20,

    30

];

console.log(numbers.indexOf(20));
```

### Output

```javascript
1
```

### Explanation

`indexOf()` always returns the **first matching index**.

---

# Example 5 (Using startIndex)

```javascript
const numbers = [

    10,

    20,

    30,

    20

];

console.log(numbers.indexOf(20,2));
```

### Output

```javascript
3
```

### Explanation

Searching starts from index **2**, so the second `20` is found.

---

# Example 6 (Empty Array)

```javascript
const data = [];

console.log(data.indexOf(100));
```

### Output

```javascript
-1
```

---

# Example 7 (Case Sensitive)

```javascript
const fruits = [

    "Apple",

    "Mango"

];

console.log(fruits.indexOf("apple"));
```

### Output

```javascript
-1
```

### Explanation

JavaScript is case-sensitive.

---

# Example 8 (Store Index)

```javascript
const colors = [

    "Red",

    "Green",

    "Blue"

];

const index = colors.indexOf("Blue");

console.log(index);
```

### Output

```javascript
2
```

---

