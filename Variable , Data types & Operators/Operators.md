# JavaScript Operators

## What is an Operator?

An **Operator** is a symbol that performs an operation on one or more values (operands).

```javascript
let sum = 10 + 5;

console.log(sum); // 15
```

## Types of Operators

1. Arithmetic Operators
2. Assignment Operators
3. Comparison Operators
4. Logical Operators
5. Increment & Decrement Operators
6. String Operator
7. Ternary Operator
8. Type Operator

## 1. Arithmetic Operators

Used for mathematical calculations.

| Operator | Meaning | Example |
| -------- | ------- | ------- |
| `+` | Addition | `10 + 5` |
| `-` | Subtraction | `10 - 5` |
| `*` | Multiplication | `10 * 5` |
| `/` | Division | `10 / 5` |
| `%` | Modulus | `10 % 3` |
| `**` | Exponent | `2 ** 3` |

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

## 2. Assignment Operators

Used to assign or update values.

| Operator | Example | Same As |
| -------- | ------- | ------- |
| `=` | `x = 5` | Assign value |
| `+=` | `x += 2` | `x = x + 2` |
| `-=` | `x -= 2` | `x = x - 2` |
| `*=` | `x *= 2` | `x = x * 2` |
| `/=` | `x /= 2` | `x = x / 2` |
| `%=` | `x %= 2` | `x = x % 2` |

```javascript
let x = 10;

x += 5;
console.log(x); // 15

x -= 3;
console.log(x); // 12
```

## 3. Comparison Operators

Used to compare two values.

| Operator | Meaning | Example |
| -------- | ------- | ------- |
| `==` | Equal (value only) | `5 == "5"` |
| `===` | Strict Equal | `5 === "5"` |
| `!=` | Not Equal | `5 != 4` |
| `!==` | Strict Not Equal | `5 !== "5"` |
| `>` | Greater Than | `10 > 5` |
| `<` | Less Than | `5 < 10` |
| `>=` | Greater Than or Equal | `5 >= 5` |
| `<=` | Less Than or Equal | `5 <= 10` |

```javascript
console.log(10 > 5);
console.log(10 == "10");
console.log(10 === "10");
```

## 4. Logical Operators

Used to combine conditions.

| Operator | Meaning |
| -------- | ------- |
| `&&` | AND |
| `||` | OR |
| `!` | NOT |

```javascript
let age = 20;
let hasID = true;

console.log(age >= 18 && hasID);
console.log(age < 18 || hasID);
console.log(!hasID);
```

## 5. Increment & Decrement Operators

Increase or decrease a value by **1**.

| Operator | Meaning |
| -------- | ------- |
| `++` | Increment |
| `--` | Decrement |

```javascript
let count = 5;

count++;
console.log(count); // 6

count--;
console.log(count); // 5
```

## 6. String Operator

The `+` operator joins strings.

```javascript
let firstName = "MD";
let lastName = "Rokonuzzaman";

console.log(firstName + " " + lastName);
```

Output:

```javascript
MD Rokonuzzaman
```

## 7. Ternary Operator

A short way to write an `if...else`.

**Syntax**

```javascript
condition ? trueValue : falseValue;
```

```javascript
let age = 20;

let result = age >= 18 ? "Adult" : "Minor";

console.log(result);
```

## 8. Type Operator

The `typeof` operator returns the data type of a value.

```javascript
console.log(typeof "Hello");
console.log(typeof 100);
console.log(typeof true);
console.log(typeof []);
console.log(typeof {});
```

## Operator Precedence

Operators with higher precedence execute first.

```javascript
let result = 10 + 5 * 2;

console.log(result);
```

Output:

```javascript
20
```

Because `*` has higher precedence than `+`.

## Summary

| Category | Purpose |
| -------- | ------- |
| Arithmetic | Mathematical calculations |
| Assignment | Assign or update values |
| Comparison | Compare values |
| Logical | Combine conditions |
| Increment/Decrement | Increase or decrease by 1 |
| String | Join strings |
| Ternary | Short `if...else` |
| Type | Check data type |

## Easy Way to Remember

- `+ - * / % **` → Arithmetic
- `= += -= *= /= %=` → Assignment
- `== === != > < >= <=` → Comparison
- `&& || !` → Logical
- `++ --` → Increment / Decrement
- `+` → String Concatenation
- `? :` → Ternary
- `typeof` → Type Checking

## Interview Questions

### Q1. What is the difference between `==` and `===`?

- `==` compares **only values** (type conversion occurs).
- `===` compares **both value and data type**.

```javascript
console.log(5 == "5"); // true
console.log(5 === "5"); // false
```

### Q2. What is the difference between `&&` and `||`?

- `&&` (AND): **All conditions must be true.**
- `||` (OR): **At least one condition must be true.**

```javascript
console.log(true && false); // false
console.log(true || false); // true
```