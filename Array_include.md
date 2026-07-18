# JavaScript Array Method - includes()

The `includes()` method is one of the most useful array methods in JavaScript. It is used to check whether an array contains a specific element.

Unlike `indexOf()`, `includes()` returns a **Boolean value (`true` or `false`)**, making it simple and readable.

---

# Table of Contents

- What is includes()?
- Why Use includes()?
- Syntax
- Parameters
- Return Value
- How includes() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is includes()?

## Definition

The `includes()` method checks whether a specified element exists inside an array.

If the element exists, it returns

```javascript
true
```

Otherwise, it returns

```javascript
false
```

It **does not modify** the original array.

---

# Why Use includes()?

We use `includes()` when we need to:

- Check if an item exists
- Validate user input
- Check permissions
- Verify selected products
- Prevent duplicate values
- Search simple values in an array

---

# Syntax

```javascript
array.includes(value);

array.includes(value, startIndex);
```

---

# Parameters

| Parameter | Description |
|-----------|-------------|
| value | The value to search for |
| startIndex | Optional. Index to start searching from |

---

# Return Value

Returns

```javascript
true
```

if the value exists.

Returns

```javascript
false
```

if the value does not exist.

---

# How includes() Works

Array

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
includes("Mango")
```

↓

Result

```javascript
true
```

---

Array

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
includes("Banana")
```

↓

Result

```javascript
false
```

---

# Example 1 (Basic)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits.includes("Mango"));
```

### Output

```javascript
true
```

### Explanation

"Mango" exists inside the array.

---

# Example 2 (Value Not Found)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits.includes("Banana"));
```

### Output

```javascript
false
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

console.log(numbers.includes(30));
```

### Output

```javascript
true
```

---

