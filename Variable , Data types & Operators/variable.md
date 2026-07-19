 # Js variable 
  In JavaScript, a variable is a container that stores data.
  You use variables to save values like numbers, text, or 
  objects so you can use them later in your program.
  
  ```javascript
let name = "Rokon";
const age = 23;
```

# There are three ways to declare variables 
- var
- let
- const  




## Definition

### var
**Definition:**
`var` is the old way of declaring a variable in JavaScript. It is function-scoped and can be redeclared and reassigned.

**Example**
```javascript
var name = "Rokon";
var name = "Rahim"; 
name = "Karim";     
```

---

### let
**Definition:**
`let` is the modern way of declaring a variable. It is block-scoped and can be reassigned, but it cannot be redeclared in the same scope.

**Example**
```javascript
let age = 23;
age = 24; // Allowed

// let age = 25;  Error
```

---

### const
**Definition:**
`const` is used to declare a constant variable. It is block-scoped and cannot be reassigned or redeclared after its initial value is assigned.

**Example**
```javascript
const PI = 3.1416;

// PI = 3.14;  Error
```

---

## Comparison

| Feature | var | let | const |
|---------|-----|-----|-------|
| Scope | Function | Block | Block |
| Redeclare |  Yes |  No |  No |
| Reassign |  Yes |  Yes |  No |
| Hoisted |  Yes |  Yes (TDZ) |  Yes (TDZ) |

---

## When to Use

- Use **const** by default.
- Use **let** when the value needs to change.
- Avoid **var** in modern JavaScript unless you have a specific reason.

