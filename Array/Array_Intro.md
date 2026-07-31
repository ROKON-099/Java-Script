# JavaScript Arrays (Part 1)

This section covers:

- What is an Array?
- Creating Arrays
- Accessing Array Elements
- Updating Elements
- Adding Elements
- Removing Elements
- Array Length

---

# What is an Array?

## Definition

An **Array** is a special JavaScript object used to store **multiple values in a single variable**.

Each value inside an array is called an **element**.

Every element has an **index**, and indexing starts from **0**.

---

## Why Do We Use Arrays?

Instead of creating multiple variables,

```javascript
let subject1 = "Math";
let subject2 = "English";
let subject3 = "Physics";
```

Use an array.

```javascript
const subjects = ["Math", "English", "Physics"];
```

Arrays make code:

- Easier to read
- Easier to manage
- Easier to loop through
- Easier to modify

---

# Array Structure

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];
```

```
Index

0        1        2

↓

Apple   Mango   Orange
```

---

# Creating Arrays

There are several ways to create arrays.

---

## Method 1 (Most Common)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits);
```

### Output

```javascript
["Apple","Mango","Orange"]
```

---

## Method 2 (Empty Array)

```javascript
const numbers = [];

console.log(numbers);
```

### Output

```javascript
[]
```

---

## Method 3 (Mixed Data Types)

```javascript
const data = [

    "Rokon",

    23,

    true,

    null

];

console.log(data);
```

### Output

```javascript
["Rokon",23,true,null]
```

---

# Accessing Array Elements

## Definition

Array elements are accessed using their **index number**.

Remember:

The first element starts at index **0**.

---

## Syntax

```javascript
array[index]
```

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits[0]);

console.log(fruits[1]);

console.log(fruits[2]);
```

### Output

```
Apple

Mango

Orange
```

---

## Access Last Element

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits[fruits.length - 1]);
```

### Output

```
Orange
```

---

## Access Non-Existing Index

```javascript
const fruits = [

    "Apple",

    "Mango"

];

console.log(fruits[10]);
```

### Output

```
undefined
```

---

# Updating Elements

## Definition

You can change an existing element by assigning a new value to its index.

---

## Syntax

```javascript
array[index] = newValue;
```

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

fruits[1] = "Banana";

console.log(fruits);
```

### Output

```javascript
["Apple","Banana","Orange"]
```

---

## Update Multiple Elements

```javascript
const numbers = [

    10,

    20,

    30

];

numbers[0] = 100;

numbers[2] = 300;

console.log(numbers);
```

### Output

```javascript
[100,20,300]
```

---

# Adding Elements

There are different ways to add elements.

The most common method is **push()**.

(We'll learn `push()` in detail in Part 2.)

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango"

];

fruits.push("Orange");

console.log(fruits);
```

### Output

```javascript
["Apple","Mango","Orange"]
```

---

## Add Multiple Elements

```javascript
const numbers = [

    1,

    2

];

numbers.push(3,4,5);

console.log(numbers);
```

### Output

```javascript
[1,2,3,4,5]
```

---

# Removing Elements

The most common method is **pop()**.

(We'll learn `pop()` in detail in Part 2.)

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

fruits.pop();

console.log(fruits);
```

### Output

```javascript
["Apple","Mango"]
```

---

# Array Length

## Definition

The `length` property returns the total number of elements in an array.

---

## Syntax

```javascript
array.length
```

---

## Example

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits.length);
```

### Output

```
3
```

---

## Get Last Element Using length

```javascript
const colors = [

    "Red",

    "Blue",

    "Green",

    "Black"

];

console.log(colors[colors.length - 1]);
```

### Output

```
Black
```

---

# Real Project Example 1

## Student Subjects

```javascript
const subjects = [

    "Math",

    "English",

    "Physics"

];

console.log(subjects[1]);
```

### Output

```
English
```

---

# Real Project Example 2

## Shopping Cart

```javascript
const cart = [

    "Laptop",

    "Mouse"

];

cart.push("Keyboard");

console.log(cart);
```

### Output

```javascript
["Laptop","Mouse","Keyboard"]
```

---

# Real Project Example 3

## Remove Completed Task

```javascript
const tasks = [

    "Study",

    "Exercise",

    "Sleep"
];

tasks.pop();

console.log(tasks);
```

### Output

```javascript
["Study","Exercise"]
```

---

# Real Project Example 4

## Total Products

```javascript
const products = [

    "Phone",

    "Laptop",

    "Monitor",

    "Keyboard"
];

console.log(products.length);
```

### Output

```
4
```

---

# Best Practices

✅ Use `const` when creating arrays.

```javascript
const numbers = [];
```

---

✅ Use meaningful variable names.

```javascript
students

products

orders

employees
```

---

✅ Access the last element using:

```javascript
array[array.length - 1]
```

---

✅ Keep similar data inside one array.

```javascript
["HTML","CSS","JavaScript"]
```

---

# Common Mistakes

## Wrong First Index

Wrong

```javascript
fruits[1]
```

for the first element.

Correct

```javascript
fruits[0]
```

---

## Accessing an Invalid Index

```javascript
console.log(fruits[100]);
```

Output

```
undefined
```

---

## Forgetting Square Brackets

Wrong

```javascript
const fruits = {};
```

Correct

```javascript
const fruits = [];
```

---

## Confusing Array Length with Last Index

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

console.log(fruits.length);
```

Output

```
3
```

Last Index

```
2
```

---

# Interview Questions

## What is an Array?

An array is a collection of multiple values stored in a single variable.

---

## What is the first index of an array?

```
0
```

---

## How do you access the first element?

```javascript
array[0]
```

---

## How do you access the last element?

```javascript
array[array.length - 1]
```

---

## How do you update an array element?

```javascript
array[index] = value;
```

---

## Which method adds an element to the end?

```javascript
push()
```

---

## Which method removes the last element?

```javascript
pop()
```

---

## Which property returns the total number of elements?

```javascript
length
```

---

# Summary Table

| Topic | Description | Example |
|--------|-------------|---------|
| Array | Collection of multiple values | `["A","B"]` |
| Create | Create an array | `[]` |
| Access | Get an element | `array[0]` |
| Update | Change an element | `array[1] = "New"` |
| Add | Add to the end | `push()` |
| Remove | Remove from the end | `pop()` |
| Length | Total elements | `array.length` |
| Last Element | Access last item | `array[array.length - 1]` |

---

# Most Frequently Used

⭐⭐⭐⭐⭐

- Array Creation
- Accessing Elements
- Updating Elements
- `push()`
- `pop()`
- `length`

⭐⭐⭐⭐

- Mixed Arrays
- Last Element Access

---

# Final Notes

Arrays are one of the most important data structures in JavaScript. They are used extensively in:

-  React Lists
-  API Responses
-  Shopping Carts
-  User Data
-  Product Lists
-  Database Records

Mastering array creation, indexing, updating, and the `length` property is essential before learning advanced array methods and looping.


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
# Example 4 (Boolean)

```javascript
const values = [

    true,

    false

];

console.log(values.includes(true));
```

### Output

```javascript
true
```

---

# Example 5 (Using startIndex)

```javascript
const numbers = [

    10,

    20,

    30,

    40

];

console.log(numbers.includes(20,2));
```

### Output

```javascript
false
```

### Explanation

Searching starts from index **2**.

Index 2 contains

```
30
```

So

```
20
```

is not found.

---

# Example 6 (Empty Array)

```javascript
const data = [];

console.log(data.includes(100));
```

### Output

```javascript
false
```

---

# Example 7 (Case Sensitive)

```javascript
const fruits = [

    "Apple",

    "Mango"

];

console.log(fruits.includes("apple"));
```

### Output

```javascript
false
```

### Explanation

JavaScript is case-sensitive.

```
Apple
```

is different from

```
apple
```

---

# Example 8 (Duplicate Values)

```javascript
const numbers = [

    10,

    20,

    20,

    30

];

console.log(numbers.includes(20));
```

### Output

```javascript
true
```

---

# Real Project Example 1

## Shopping Cart

```javascript
const cart = [

    "Laptop",

    "Mouse"

];

console.log(cart.includes("Laptop"));
```

### Output

```javascript
true
```

---

# Real Project Example 2

## User Role

```javascript
const roles = [

    "Admin",

    "Editor",

    "User"

];

console.log(roles.includes("Admin"));
```

### Output

```javascript
true
```

---

# Real Project Example 3

## Prevent Duplicate Student

```javascript
const students = [

    "Rahim",

    "Karim"

];

const newStudent = "Rahim";

if(!students.includes(newStudent)){

    students.push(newStudent);

}

console.log(students);
```

### Output

```javascript
["Rahim","Karim"]
```

---

# Real Project Example 4

## Allowed Countries

```javascript
const countries = [

    "Bangladesh",

    "India",

    "Japan"

];

console.log(countries.includes("Bangladesh"));
```

### Output

```javascript
true
```

---

# Real Project Example 5

## Favorite Programming Languages

```javascript
const languages = [

    "JavaScript",

    "Python",

    "Java"

];

console.log(languages.includes("Python"));
```

### Output

```javascript
true
```

---

# Best Practices

 Use `includes()` when you only need to know whether a value exists.

---

 Use meaningful variable names.

```javascript
products

students

roles

languages
```

---

 Use `includes()` instead of `indexOf()` for readability.

```javascript
if(products.includes("Laptop")){

}
```

---

# Common Mistakes

## Mistake 1

Expecting `includes()` to return an index.

Wrong

```javascript
const result = numbers.includes(20);

console.log(result);
```

Output

```javascript
true
```

It returns a Boolean, **not an index**.

---

## Mistake 2

Ignoring case sensitivity.

```javascript
const fruits = ["Apple"];

console.log(fruits.includes("apple"));
```

Output

```javascript
false
```

---

## Mistake 3

Using `includes()` to find an object.

```javascript
const users = [

    {

        name:"John"

    }

];

console.log(users.includes({

    name:"John"

}));
```

Output

```javascript
false
```

Objects are compared by **reference**, not by value.

---

## Mistake 4

Confusing `includes()` with `indexOf()`.

```javascript
includes()
```

returns

```javascript
true/false
```

while

```javascript
indexOf()
```

returns

```javascript
index / -1
```

---

# Interview Questions

## What does `includes()` do?

Checks whether a value exists in an array.

---

## What does `includes()` return?

```javascript
true
```

or

```javascript
false
```

---

## Does `includes()` modify the original array?

 No.

---

## Is `includes()` case-sensitive?

 Yes.
---

## Can `includes()` search from a specific index?

 Yes.

```javascript
array.includes(value, startIndex);
```

---

## Which method returns an index?

```javascript
indexOf()
```

---

## Which method returns true or false?

```javascript
includes()
```

---

# Summary Table

| Feature | Description |
|---------|-------------|
| Method | `includes()` |
| Purpose | Check whether a value exists |
| Parameters | value, startIndex (optional) |
| Returns | `true` or `false` |
| Changes Original Array |  No |
| Common Uses | Validation, Search, Permissions, Duplicate Check |

---

# Quick Comparison

| Method | Returns | Modifies Array |
|---------|----------|----------------|
| `includes()` | `true` / `false` |  No |
| `indexOf()` | Index / `-1` |  No |
| `lastIndexOf()` | Last Index / `-1` |  No |

---

# Final Notes

The `includes()` method is one of the easiest and most readable ways to check if an array contains a value. It is widely used in:

-  Form validation
-  Shopping cart applications
-  Authentication & authorization
-  Duplicate prevention
-  Search functionality
-  Permission checking

Mastering `includes()` will make your JavaScript code cleaner, more readable, and easier to maintain.



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
# Real Project Example 1

## Remove a Product

```javascript
const cart = [

    "Laptop",

    "Mouse",

    "Keyboard"

];

const index = cart.indexOf("Mouse");

cart.splice(index,1);

console.log(cart);
```

### Output

```javascript
["Laptop","Keyboard"]
```

---

# Real Project Example 2

## Check Student

```javascript
const students = [

    "Rahim",

    "Karim",

    "Rokon"

];

console.log(students.indexOf("Karim"));
```

### Output

```javascript
1
```

---

# Real Project Example 3

## Update Status

```javascript
const status = [

    "Pending",

    "Approved",

    "Rejected"

];

const index = status.indexOf("Approved");

status[index] = "Completed";

console.log(status);
```

### Output

```javascript
[
    "Pending",
    "Completed",
    "Rejected"
]
```

---

# Real Project Example 4

## Search Category

```javascript
const categories = [

    "HTML",

    "CSS",

    "JavaScript"

];

console.log(categories.indexOf("CSS"));
```

### Output

```javascript
1
```

---

# Real Project Example 5

## User Role

```javascript
const roles = [

    "User",

    "Editor",

    "Admin"

];

console.log(roles.indexOf("Admin"));
```

### Output

```javascript
2
```

---

# Best Practices

✅ Use `indexOf()` when you need the position of an element.

---

✅ Always check for `-1`.

```javascript
const index = array.indexOf(value);

if(index !== -1){

    console.log("Found");

}
```

---

✅ Use meaningful variable names.

```javascript
productIndex

studentIndex

userIndex
```

---

# Common Mistakes

## Mistake 1

Ignoring `-1`.

Wrong

```javascript
const index = fruits.indexOf("Banana");

fruits[index] = "Apple";
```

Always check

```javascript
if(index !== -1)
```

---

## Mistake 2

Expecting the last occurrence.

```javascript
const arr = [10,20,20];

console.log(arr.indexOf(20));
```

Output

```javascript
1
```

Use `lastIndexOf()` for the last occurrence.

---

## Mistake 3

Using `indexOf()` with objects.

```javascript
const users = [

    {

        name:"John"

    }

];

console.log(users.indexOf({

    name:"John"

}));
```

Output

```javascript
-1
```

Objects are compared by reference.

---

## Mistake 4

Ignoring case sensitivity.

```javascript
["Apple"].indexOf("apple");
```

Output

```javascript
-1
```

---

# Interview Questions

## What does `indexOf()` return?

The index of the first matching element.

---

## What does it return if the element is not found?

```javascript
-1
```

---

## Does `indexOf()` modify the original array?

 No.

---

## Can it search from a specific index?

 Yes.

```javascript
array.indexOf(value,startIndex);
```

---

## Does `indexOf()` return the first or last occurrence?

The **first** occurrence.

---

## Which method returns the last occurrence?

```javascript
lastIndexOf()
```

---

## Which method returns `true` or `false` instead of an index?

```javascript
includes()
```

---

# Summary Table

| Feature | Description |
|---------|-------------|
| Method | `indexOf()` |
| Purpose | Find the first index of a value |
| Parameters | value, startIndex (optional) |
| Returns | Index or `-1` |
| Changes Original Array |  No |
| Common Uses | Search, Update, Remove, Validation |

---

# Quick Comparison

| Method | Returns | Modifies Array |
|---------|----------|----------------|
| `includes()` | `true` / `false` |  No |
| `indexOf()` | First Index / `-1` |  No |
| `lastIndexOf()` | Last Index / `-1` |  No |

---

# Final Notes

The `indexOf()` method is essential when you need the **position** of an element rather than just checking if it exists. It is widely used in:

-  Search functionality
-  Updating array elements
-  Removing items with `splice()`
-  Data validation
-  Form processing
-  Menu and navigation systems

Mastering `indexOf()` is an important step before learning more advanced array methods such as `find()`, `findIndex()`, and `filter()`.
