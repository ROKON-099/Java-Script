 # JavaScript Variables

## What is a Variable?

A **variable** is a named container used to store data in memory. You can store different types of values such as numbers, strings, booleans, arrays, objects, or functions. Variables make it easy to reuse and update data throughout your program.

### Example

```javascript
let name = "Rokon";
const age = 23;

console.log(name); // Rokon
console.log(age);  // 23
```

---

# Why Do We Use Variables?

Variables help us:

- Store data
- Reuse values
- Update values when needed
- Make code easier to read and maintain

Without Variables

```javascript
console.log("Rokon");
console.log("Rokon");
console.log("Rokon");
```

With Variables

```javascript
let name = "Rokon";

console.log(name);
console.log(name);
console.log(name);
```

---

# Variable Naming Rules

A variable name:

- Must begin with a letter, `_`, or `$`.
- Cannot begin with a number.
- Cannot contain spaces.
- Is case-sensitive.
- Cannot use JavaScript reserved keywords.

### Valid

```javascript
let name = "Rokon";
let firstName = "Rokon";
let _age = 23;
let $price = 100;
```

### Invalid

```javascript
let 1name = "Rokon";
let first name = "Rokon";
let let = 10;
```

---

# JavaScript is Case-Sensitive

These are different variables.

```javascript
let name = "Rokon";
let Name = "Rahim";
let NAME = "Karim";
```

---

# Variable Declaration

There are three ways to declare variables in JavaScript.

- var
- let
- const

---

# var

## Definition

`var` is the old way of declaring variables in JavaScript. It is **function-scoped**, can be **redeclared**, and can be **reassigned**.

### Syntax

```javascript
var variableName = value;
```

### Example

```javascript
var name = "Rokon";

var name = "Rahim"; // Redeclare
name = "Karim";     // Reassign

console.log(name);
```

### Scope Example

```javascript
if (true) {
    var city = "Dhaka";
}

console.log(city); // Dhaka
```

---

# let

## Definition

`let` is the modern way of declaring variables. It is **block-scoped**. It can be **reassigned**, but **cannot be redeclared** in the same block.

### Syntax

```javascript
let variableName = value;
```

### Example

```javascript
let age = 23;

age = 24;

console.log(age);
```

### Error

```javascript
let age = 23;

// let age = 24;  Error
```

### Scope Example

```javascript
if (true) {
    let city = "Dhaka";
}

// console.log(city);  Error
```

---

# const

## Definition

`const` declares a constant variable. It is **block-scoped** and **must be initialized** when declared. It cannot be reassigned or redeclared.

### Syntax

```javascript
const variableName = value;
```

### Example

```javascript
const PI = 3.1416;

console.log(PI);
```

### Error

```javascript
const PI = 3.1416;

// PI = 3.14;  Error
```

---

# const with Objects

The variable cannot be reassigned, but the object's properties can be changed.

```javascript
const person = {
    name: "Rokon",
    age: 23
};

person.age = 24;

console.log(person);
```

---

# const with Arrays

Array elements can be changed.

```javascript
const numbers = [10, 20, 30];

numbers.push(40);

console.log(numbers);
```

---

# Primitive Data Types

Variables can store primitive values.

```javascript
let name = "Rokon";      // String
let age = 23;            // Number
let isStudent = true;    // Boolean
let salary = null;       // Null
let address;             // Undefined
```

---

# Non-Primitive Data Types

Variables can also store complex data.

```javascript
let person = {
    name: "Rokon",
    age: 23
};

let numbers = [10, 20, 30];

function greet() {
    console.log("Hello");
}
```

---

# Variable Scope

JavaScript has three types of scope.

## Global Scope

Accessible everywhere.

```javascript
let name = "Rokon";

function show() {
    console.log(name);
}

show();
```

---

## Function Scope

```javascript
function test() {
    var age = 23;

    console.log(age);
}

// console.log(age);  Error
```

---

## Block Scope

```javascript
if (true) {
    let city = "Dhaka";
    const country = "Bangladesh";
}

// console.log(city);  Error
// console.log(country);  Error
```

---

# Hoisting

JavaScript moves variable declarations to the top of their scope before execution.

## var

```javascript
console.log(name);

var name = "Rokon";
```

Output

```
undefined
```

---

## let

```javascript
console.log(age);

let age = 23;
```

Output

```
ReferenceError
```

---

## const

```javascript
console.log(PI);

const PI = 3.1416;
```

Output

```
ReferenceError
```

---

# Temporal Dead Zone (TDZ)

The **Temporal Dead Zone (TDZ)** is the time between entering a block and the point where a `let` or `const` variable is declared.

```javascript
{
    // TDZ starts

    // console.log(age);

    let age = 23;

    console.log(age);
}
```

---

# Comparison

| Feature | var | let | const |
|----------|-----|-----|-------|
| Scope | Function | Block | Block |
| Redeclare |  Yes |  No |  No |
| Reassign |  Yes |  Yes |  No |
| Hoisted |  Yes |  Yes (TDZ) |  Yes (TDZ) |
| Must Initialize |  No |  No |  Yes |
| Modern Use |  Rarely |  Yes |  Most Preferred |

---

# Best Practices

 Use **const** by default.

```javascript
const company = "Google";
```

Use **let** only when the value needs to change.

```javascript
let score = 0;

score++;
```

Avoid using **var** in modern JavaScript.

---

# Summary

- Variables store data.
- JavaScript has three variable keywords: **var**, **let**, and **const**.
- **const** is the safest and most commonly used.
- **let** is used for changing values.
- **var** is the old syntax and should generally be avoided.
- Variable names are case-sensitive.
- Prefer meaningful variable names.