# JavaScript Array Method - join()

The `join()` method is one of the most useful array methods in JavaScript. It is used to **convert an array into a string** by joining all elements together.

You can choose any separator such as a comma, space, dash, or any custom character.

Unlike `splice()` or `push()`, the `join()` method **does not modify the original array**.

---

# Table of Contents

- What is join()?
- Why Use join()?
- Syntax
- Parameters
- Return Value
- How join() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is join()?

## Definition

The `join()` method combines all elements of an array into a **single string**.

The elements are separated by a specified separator.

If no separator is provided, JavaScript uses a comma (`,`).

---

# Why Use join()?

We use `join()` when we need to:

- Convert an array into a string
- Display lists
- Generate CSV data
- Create URLs
- Format user input
- Build readable text

---

# Syntax

```javascript
array.join();

array.join(separator);
```

---

# Parameters

| Parameter | Description |
|-----------|-------------|
| separator | Optional. Character(s) placed between elements |

Common separators

```javascript
","

" "

"-"

"|"

"/"
```

---

# Return Value

Returns a **string**.

The original array is **not modified**.

---

# How join() Works

Array

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
join()
```

↓

Result

```javascript
"Apple,Mango,Orange"
```

---

Array

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
join(" - ")
```

↓

Result

```javascript
"Apple - Mango - Orange"
```

---

# Example 1 (Default Separator)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits.join());
```

### Output

```javascript
Apple,Mango,Orange
```

### Explanation

Since no separator is provided, JavaScript uses a comma (`,`).

---

# Example 2 (Space Separator)

```javascript
const words = [

    "I",

    "Love",

    "JavaScript"

];

console.log(words.join(" "));
```

### Output

```javascript
I Love JavaScript
```

---

# Example 3 (Dash Separator)

```javascript
const numbers = [

    10,

    20,

    30

];

console.log(numbers.join("-"));
```

### Output

```javascript
10-20-30
```

---

# Example 4 (Pipe Separator)

```javascript
const colors = [

    "Red",

    "Green",

    "Blue"

];

console.log(colors.join(" | "));
```

### Output

```javascript
Red | Green | Blue
```

---

