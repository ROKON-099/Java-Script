# JavaScript Array Method - shift()

The `shift()` method is one of the most commonly used array methods in JavaScript. It is used to **remove the first element** from an array.

---

# Table of Contents

- What is shift()?
- Why Use shift()?
- Syntax
- Parameters
- Return Value
- How shift() Works
- Basic Examples
- Multiple Examples
- Real Project Examples
- Best Practices
- Common Mistakes
- Interview Questions
- Summary Table

---

# What is shift()?

## Definition

The `shift()` method removes the **first element** from an array.

It shifts all remaining elements one position to the left.

It modifies the **original array** and returns the **removed element**.

---

# Why Use shift()?

We use `shift()` when we need to:

- Remove the first item
- Process a queue
- Remove the oldest notification
- Remove the first task
- Process API data one by one

---

# Syntax

```javascript
array.shift();
```

---

# Parameters

`shift()` does **not** accept any parameters.

```javascript
array.shift();
```

---

# Return Value

`shift()` returns the **removed first element**.

Example

```javascript
const fruits = ["Apple", "Mango", "Orange"];

let removed = fruits.shift();

console.log(removed);
```

### Output

```
Apple
```

---

# How shift() Works

Before

```javascript
["Apple","Mango","Orange"]
```

↓

```javascript
shift()
```

↓

Removed

```
Apple
```

↓

After

```javascript
["Mango","Orange"]
```

Notice that every remaining element moves one position to the left.

---

# Example 1 (Basic)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

fruits.shift();

console.log(fruits);
```

### Output

```javascript
["Mango","Orange"]
```

### Explanation

- `"Apple"` is removed.
- `"Mango"` becomes the first element.
- `"Orange"` becomes the second element.
- The original array is modified.

---

# Example 2 (Store Removed Element)

```javascript
const fruits = [

    "Apple",

    "Mango",

    "Orange"

];

const removedFruit = fruits.shift();

console.log(removedFruit);

console.log(fruits);
```

### Output

```
Apple

["Mango","Orange"]
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

numbers.shift();

console.log(numbers);
```

### Output

```javascript
[20,30,40]
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

const removedUser = users.shift();

console.log(removedUser);

console.log(users);
```

### Output

```javascript
{ name: "John" }

[
    { name: "Sara" }
]
```

---

# Example 5 (Empty Array)

```javascript
const numbers = [];

const removed = numbers.shift();

console.log(removed);

console.log(numbers);
```

### Output

```
undefined

[]
```

---

# Example 6 (Multiple shift())

```javascript
const colors = [

    "Red",

    "Blue",

    "Green"

];

colors.shift();

colors.shift();

console.log(colors);
```

### Output

```javascript
["Green"]
```

---

# Example 7 (Using Variables)

```javascript
const tasks = [

    "Study",

    "Exercise",

    "Sleep"

];

let firstTask = tasks.shift();

console.log(firstTask);
```

### Output

```
Study
```

---

# Example 8 (Single Element Array)

```javascript
const items = [

    "Laptop"

];

items.shift();

console.log(items);
```

### Output

```javascript
[]
```

---

# Real Project Example 1

## Queue System

```javascript
const queue = [

    "Customer 1",

    "Customer 2",

    "Customer 3"

];

const servedCustomer = queue.shift();

console.log(servedCustomer);

console.log(queue);
```

### Output

```
Customer 1

["Customer 2","Customer 3"]
```

---

# Real Project Example 2

## Notification System

```javascript
const notifications = [

    "Message",

    "Payment",

    "Order"

];

notifications.shift();

console.log(notifications);
```

### Output

```javascript
["Payment","Order"]
```

---

# Real Project Example 3

## Todo List

```javascript
const todos = [

    "Wake Up",

    "Study",

    "Exercise"

];

const completedTask = todos.shift();

console.log(completedTask);

console.log(todos);
```

### Output

```
Wake Up

["Study","Exercise"]
```

---

# Real Project Example 4

## Playlist

```javascript
const playlist = [

    "Song A",

    "Song B",

    "Song C"

];

playlist.shift();

console.log(playlist);
```

### Output

```javascript
["Song B","Song C"]
```

---

# Real Project Example 5

## Order Processing

```javascript
const orders = [

    "#1001",

    "#1002",

    "#1003"

];

const processingOrder = orders.shift();

console.log(processingOrder);

console.log(orders);
```

### Output

```
#1001

["#1002","#1003"]
```

---

# Best Practices

✅ Use `shift()` only when removing the **first element**.

---

✅ Store the removed element if it is needed later.

```javascript
const firstItem = array.shift();
```

---

✅ Check if the array is empty before calling `shift()`.

```javascript
if(array.length > 0){

    array.shift();

}
```

---

✅ Use meaningful variable names.

```javascript
removedTask

servedCustomer

firstMessage
```

---

# Common Mistakes

## Mistake 1

Expecting `shift()` to return the updated array.

Wrong

```javascript
const result = numbers.shift();

console.log(result);
```

Output

```
10
```

It returns the **removed element**, not the updated array.

Correct

```javascript
numbers.shift();

console.log(numbers);
```

---

## Mistake 2

Passing a parameter.

Wrong

```javascript
numbers.shift(10);
```

`shift()` ignores all parameters.

Correct

```javascript
numbers.shift();
```

---

## Mistake 3

Using `shift()` on an empty array.

```javascript
const arr = [];

console.log(arr.shift());
```

### Output

```
undefined
```

---

## Mistake 4

Using the wrong method.

To remove the **last element**, use

```javascript
pop()
```

instead of

```javascript
shift()
```

---

## Mistake 5

Forgetting that indexes change after `shift()`.

Before

```javascript
["Apple","Mango","Orange"]
```

After

```javascript
shift()
```

Result

```javascript
["Mango","Orange"]
```

Now,

```javascript
array[0]
```

is

```
"Mango"
```

not `"Apple"`.

---

# Interview Questions

## What does `shift()` do?

It removes the **first element** from an array.

---

## Does `shift()` modify the original array?

✅ Yes.

---

## What does `shift()` return?

The removed first element.

---

## Does `shift()` take any parameters?

❌ No.

---

## What happens if the array is empty?

It returns

```javascript
undefined
```

---

## Which method removes the last element?

```javascript
pop()
```

---

## Which method adds an element at the beginning?

```javascript
unshift()
```

---

## What happens to the remaining elements after `shift()`?

They move one position to the left.

---

# Summary Table

| Feature | Description |
|---------|-------------|
| Method | `shift()` |
| Purpose | Remove the first element |
| Parameters | None |
| Returns | Removed first element |
| Changes Original Array | ✅ Yes |
| Removes From | Beginning of the array |
| Common Uses | Queue, Notifications, Todo List, Order Processing |

---

# Quick Comparison

| Method | Action | Returns | Changes Original Array |
|---------|--------|---------|------------------------|
| `push()` | Add to end | New length | ✅ Yes |
| `pop()` | Remove from end | Removed element | ✅ Yes |
| `unshift()` | Add to beginning | New length | ✅ Yes |
| `shift()` | Remove from beginning | Removed element | ✅ Yes |

---

# Final Notes

The `shift()` method is commonly used in applications where the **oldest item needs to be processed first**. Typical use cases include:

- ✅ Queue systems (FIFO)
- ✅ Customer service queues
- ✅ Notification management
- ✅ Task processing
- ✅ Order processing
- ✅ Playlist management

Mastering `shift()` helps you understand queue-based data processing and prepares you for more advanced array operations.