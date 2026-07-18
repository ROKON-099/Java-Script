# JavaScript Operators

## What is an Operator?

An **operator** is a symbol that performs an operation on one or more values (operands).

**Example**

```javascript
let sum = 10 + 5;
console.log(sum); // 15
```

Here:
- `10` and `5` are **operands**.
- `+` is the **operator**.

---

# Types of Operators

1. Arithmetic Operators
2. Assignment Operators
3. Comparison Operators
4. Logical Operators
5. Increment & Decrement Operators
6. String Operators
7. Ternary Operator
8. Type Operators

---

# 1. Arithmetic Operators

Used to perform mathematical calculations.

| Operator | Meaning | Example | Result |
|----------|---------|---------|--------|
| + | Addition | 10 + 5 | 15 |
| - | Subtraction | 10 - 5 | 5 |
| * | Multiplication | 10 * 5 | 50 |
| / | Division | 10 / 5 | 2 |
| % | Modulus (Remainder) | 10 % 3 | 1 |
| ** | Exponent | 2 ** 3 | 8 |

### Example

```javascript
let a = 10;
let b = 3;

console.log(a + b);
console.log(a - b);
console.log(a * b);
console.log(a / b);
console.log(a % b);
console.log(a ** b);
```

---

# 2. Assignment Operators

Used to assign values.

| Operator | Example | Same As |
|----------|---------|---------|
| = | x = 5 | Assign value |
| += | x += 2 | x = x + 2 |
| -= | x -= 2 | x = x - 2 |
| *= | x *= 2 | x = x * 2 |
| /= | x /= 2 | x = x / 2 |
| %= | x %= 2 | x = x % 2 |

### Example

```javascript
let x = 10;

x += 5;
console.log(x); // 15

x -= 3;
console.log(x); // 12
```

---

# 3. Comparison Operators

Used to compare two values.

| Operator | Meaning | Example |
|----------|---------|---------|
| == | Equal (value only) | 5 == "5" → true |
| === | Strict Equal | 5 === "5" → false |
| != | Not Equal | 5 != 4 |
| !== | Strict Not Equal | 5 !== "5" |
| > | Greater Than | 10 > 5 |
| < | Less Than | 5 < 10 |
| >= | Greater Than or Equal | 5 >= 5 |
| <= | Less Than or Equal | 5 <= 10 |

### Example

```javascript
console.log(10 > 5);
console.log(10 === "10");
console.log(10 == "10");
```

---

# 4. Logical Operators

Used to combine multiple conditions.

| Operator | Meaning |
|----------|---------|
| && | AND |
| \|\| | OR |
| ! | NOT |

### Example

```javascript
let age = 20;
let hasID = true;

console.log(age >= 18 && hasID);
console.log(age < 18 || hasID);
console.log(!hasID);
```

---

# 5. Increment & Decrement Operators

Increase or decrease a value by 1.

| Operator | Meaning |
|----------|---------|
| ++ | Increment |
| -- | Decrement |

### Example

```javascript
let count = 5;

count++;
console.log(count); // 6

count--;
console.log(count); // 5
```

---

# 6. String Operator

The `+` operator joins strings.

### Example

```javascript
let firstName = "MD";
let lastName = "Rokonuzzaman";

console.log(firstName + " " + lastName);
```

Output

```
MD Rokonuzzaman
```

---

# 7. Ternary Operator

A short way to write an if...else statement.

### Syntax

```javascript
condition ? trueValue : falseValue;
```

### Example

```javascript
let age = 20;

let result = age >= 18 ? "Adult" : "Minor";

console.log(result);
```

---

# 8. Type Operator

The `typeof` operator returns the data type.

### Example

```javascript
console.log(typeof "Hello");
console.log(typeof 100);
console.log(typeof true);
console.log(typeof []);
console.log(typeof {});
```

---

# Operator Priority (Precedence)

```javascript
let result = 10 + 5 * 2;
console.log(result);
```

Output

```
20
```

Because multiplication (`*`) has higher precedence than addition (`+`).

---

# Summary

| Category | Purpose |
|----------|---------|
| Arithmetic | Mathematical calculations |
| Assignment | Assign values |
| Comparison | Compare values |
| Logical | Combine conditions |
| Increment/Decrement | Increase or decrease by 1 |
| String | Join strings |
| Ternary | Short if...else |
| Type | Check data type |

---

# Easy Way to Remember

- ➕ ➖ ✖️ ➗ → **Arithmetic**
- = += -= → **Assignment**
- == === > < → **Comparison**
- && || ! → **Logical**
- ++ -- → **Increment / Decrement**
- + (String) → **Concatenation**
- ? : → **Ternary**
- typeof → **Type Checking**

---

# Interview Questions

### Q1. What is the difference between `==` and `===`?

- `==` compares only values (type conversion happens).
- `===` compares both value and data type.

```javascript
console.log(5 == "5");   // true
console.log(5 === "5");  // false
```

---

### Q2. What is the difference between `&&` and `||`?

- `&&` (AND): All conditions must be true.
- `||` (OR): At least one condition must be true.

```javascript
console.log(true && false); // false
console.log(true || false); // true
```