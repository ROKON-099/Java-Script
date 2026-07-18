# JavaScript Array Method - sort()

The `sort()` method is one of the most powerful array methods in JavaScript. It is used to **sort the elements of an array**.

By default, `sort()` arranges elements in **ascending alphabetical (Unicode) order**.

It **modifies the original array**.

---

# Table of Contents

- What is sort()?
- Why Use sort()?
- Syntax
- Parameters
- Return Value
- How sort() Works
- Basic Examples
- Sorting Numbers
- Sorting Strings
- Custom Sorting
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is sort()?

## Definition

The `sort()` method sorts the elements of an array.

By default:

- Strings are sorted alphabetically.
- Numbers are sorted as strings (Unicode order).

It modifies the **original array**.

---

# Why Use sort()?

We use `sort()` when we need to:

- Sort numbers
- Sort names
- Display products alphabetically
- Sort prices
- Display rankings
- Arrange data before showing it to users

---

# Syntax

```javascript
array.sort();

array.sort(compareFunction);
```

---

# Parameters

| Parameter | Description |
|-----------|-------------|
| compareFunction | Optional function used for custom sorting |

---

# Return Value

Returns the **sorted array**.

The original array is modified.

---

# How sort() Works

Before

```javascript
["Orange","Apple","Banana"]
```

↓

```javascript
sort()
```

↓

After

```javascript
["Apple","Banana","Orange"]
```

---

# Example 1 (Basic String Sorting)

```javascript
const fruits = [

    "Orange",

    "Apple",

    "Banana"

];

fruits.sort();

console.log(fruits);
```

### Output

```javascript
["Apple","Banana","Orange"]
```

### Explanation

Strings are sorted alphabetically.

---

# Example 2 (Numbers Without Compare Function)

```javascript
const numbers = [

    100,

    20,

    5,

    40

];

numbers.sort();

console.log(numbers);
```

### Output

```javascript
[100,20,40,5]
```

### Explanation

JavaScript compares numbers as **strings** by default.

```
100

20

40

5
```

are sorted alphabetically, not numerically.

---

# Example 3 (Ascending Numbers)

```javascript
const numbers = [

    100,

    20,

    5,

    40

];

numbers.sort(function(a,b){

    return a-b;

});

console.log(numbers);
```

### Output

```javascript
[5,20,40,100]
```

### Explanation

If

```javascript
a-b
```

is negative,

`a` comes before `b`.

---

# Example 4 (Descending Numbers)

```javascript
const numbers = [

    100,

    20,

    5,

    40

];

numbers.sort(function(a,b){

    return b-a;

});

console.log(numbers);
```

### Output

```javascript
[100,40,20,5]
```

---

# Example 5 (Case Sensitive)

```javascript
const names = [

    "John",

    "apple",

    "Banana"

];

names.sort();

console.log(names);
```

### Output

```javascript
["Banana","John","apple"]
```

Uppercase letters come before lowercase letters.

---

# Example 6 (Copy Before Sorting)

```javascript
const numbers = [

    30,

    10,

    20

];

const sorted = numbers.slice().sort(function(a,b){

    return a-b;

});

console.log(sorted);

console.log(numbers);
```

### Output

```javascript
[10,20,30]

[30,10,20]
```

The original array remains unchanged because `slice()` creates a copy.

---

# Example 7 (Sort Objects)

```javascript
const students = [

    {

        name:"Rahim",

        marks:80

    },

    {

        name:"Karim",

        marks:95

    },

    {

        name:"Rokon",

        marks:70

    }

];

students.sort(function(a,b){

    return a.marks-b.marks;

});

console.log(students);
```

### Output

```javascript
[
    { name:"Rokon", marks:70 },
    { name:"Rahim", marks:80 },
    { name:"Karim", marks:95 }
]
```

---

# Example 8 (Sort by String Length)

```javascript
const words = [

    "Java",

    "HTML",

    "JavaScript",

    "CSS"

];

words.sort(function(a,b){

    return a.length-b.length;

});

console.log(words);
```

### Output

```javascript
[
    "CSS",
    "Java",
    "HTML",
    "JavaScript"
]
```

---

