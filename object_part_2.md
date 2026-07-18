# JavaScript Objects (Part 2A)

This section covers:

- Object Methods
- this Keyword
- Real Project Examples
- Common Mistakes
- Interview Questions

---

# Object Methods

## Definition

An **Object Method** is a function stored inside an object.

Methods allow an object to perform actions.

Unlike properties, methods contain executable code.

---

## Object Structure

```javascript
const person = {

    name: "Rokon",

    age: 23,

    greet: function () {

        console.log("Hello!");

    }

};
```

Here,

| Item | Type |
|------|------|
| name | Property |
| age | Property |
| greet | Method |

---

# Creating an Object Method

## Syntax

```javascript
const object = {

    methodName: function(){

        // code

    }

};
```

---

## Example

```javascript
const student = {

    name: "Rokon",

    greet: function(){

        console.log("Welcome!");

    }

};

student.greet();
```

### Output

```
Welcome!
```

---

# ES6 Short Method Syntax

JavaScript provides a shorter syntax for methods.

Instead of writing:

```javascript
const user = {

    greet: function(){

        console.log("Hello");

    }

};
```

Write

```javascript
const user = {

    greet(){

        console.log("Hello");

    }

};
```

Output

```
Hello
```

This is the preferred syntax in modern JavaScript.

---

# Methods Can Use Properties

```javascript
const student = {

    name: "Rokon",

    greet(){

        console.log("Hello " + this.name);

    }

};

student.greet();
```

Output

```
Hello Rokon
```

---

# Returning Values

Methods can return values.

```javascript
const calculator = {

    add(){

        return 20 + 30;

    }

};

console.log(calculator.add());
```

Output

```
50
```

---

# Multiple Methods

```javascript
const calculator = {

    add(a,b){

        return a+b;

    },

    subtract(a,b){

        return a-b;

    }

};

console.log(calculator.add(20,10));

console.log(calculator.subtract(20,10));
```

Output

```
30

10
```

---

# Why Use Methods?

Methods group behavior with data.

Example

Instead of

```javascript
let name = "Rokon";

function greet(){

    console.log("Hello");

}
```

Use

```javascript
const user = {

    name: "Rokon",

    greet(){

        console.log("Hello");

    }

};
```

Everything related to the user stays inside one object.

---

# The this Keyword

## Definition

The **this** keyword refers to the object that is calling the method.

---

## Example

```javascript
const student = {

    name: "Rokon",

    age: 23,

    introduce(){

        console.log(this.name);

    }

};

student.introduce();
```

Output

```
Rokon
```

---

## Explanation

```
student

↓

introduce()

↓

this

↓

student
```

Therefore,

```javascript
this.name
```

means

```javascript
student.name
```

---

# Access Multiple Properties

```javascript
const student = {

    name: "Rokon",

    age: 23,

    cgpa: 3.90,

    details(){

        console.log(this.name);

        console.log(this.age);

        console.log(this.cgpa);

    }

};

student.details();
```

Output

```
Rokon

23

3.9
```

---

# Without this

```javascript
const student = {

    name: "Rokon",

    greet(){

        console.log(name);

    }

};

student.greet();
```

Output

```
ReferenceError
```

Because JavaScript searches for a variable named `name`, not the object's property.

Correct

```javascript
this.name
```

---

# this in Another Object

```javascript
const car = {

    brand: "Toyota",

    model: "Corolla",

    show(){

        console.log(this.brand);

        console.log(this.model);

    }

};

car.show();
```

Output

```
Toyota

Corolla
```

---

# Real Project Example 1

## User Profile

```javascript
const user = {

    firstName: "MD",

    lastName: "Rokon",

    fullName(){

        return this.firstName + " " + this.lastName;

    }

};

console.log(user.fullName());
```

Output

```
MD Rokon
```

---

# Real Project Example 2

## Shopping Cart

```javascript
const product = {

    name: "Laptop",

    price: 50000,

    discount: 5000,

    finalPrice(){

        return this.price - this.discount;

    }

};

console.log(product.finalPrice());
```

Output

```
45000
```

---

# Real Project Example 3

## Bank Account

```javascript
const account = {

    owner: "Rokon",

    balance: 10000,

    deposit(amount){

        this.balance += amount;

    }

};

account.deposit(5000);

console.log(account.balance);
```

Output

```
15000
```

---

# Real Project Example 4

## Student Result

```javascript
const student = {

    name: "Rokon",

    marks: [80,90,95],

    average(){

        return (80+90+95)/3;

    }

};

console.log(student.average());
```

Output

```
88.33333333333333
```

---

# Best Practices

✅ Use ES6 method syntax.

```javascript
greet(){

}
```

---

✅ Use `this` to access properties inside methods.

```javascript
this.name
```

---

✅ Keep related data and functions inside one object.

---

✅ Use meaningful method names.

Examples

```
login()

logout()

calculateTotal()

getFullName()

addToCart()
```

---

# Common Mistakes

## Forgetting Parentheses

Wrong

```javascript
console.log(user.greet);
```

Output

```
[Function]
```

Correct

```javascript
console.log(user.greet());
```

---

## Forgetting this

Wrong

```javascript
console.log(name);
```

Correct

```javascript
console.log(this.name);
```

---

## Using Arrow Functions as Object Methods

Wrong

```javascript
const user = {

    name: "Rokon",

    greet: () => {

        console.log(this.name);

    }

};
```

`this` inside an arrow function does **not** refer to the object.

Correct

```javascript
const user = {

    name: "Rokon",

    greet(){

        console.log(this.name);

    }

};
```

---

## Typo in Property Names

Wrong

```javascript
this.fullname
```

Correct

```javascript
this.fullName
```

JavaScript property names are case-sensitive.

---

# Interview Questions

## What is an Object Method?

A method is a function stored inside an object.

---

## What is the difference between a Property and a Method?

| Property | Method |
|----------|--------|
| Stores data | Stores a function |
| Example: `name` | Example: `greet()` |

---

## What does `this` refer to?

`this` refers to the object that calls the method.

---

## Why should you use `this`?

It allows a method to access the object's own properties.

---

## Can an object have multiple methods?

Yes.

```javascript
const calculator = {

    add(){},

    subtract(){},

    multiply(){},

    divide(){}

};
```

---

## Which syntax is preferred for object methods?

```javascript
greet(){

}
```

instead of

```javascript
greet: function(){

}
```

---

## Can methods return values?

Yes.

```javascript
square(n){

    return n*n;

}
```

---

# Summary Table

| Topic | Description |
|--------|-------------|
| Method | Function inside an object |
| ES6 Method Syntax | `greet(){}` |
| this | Refers to the current object |
| Access Property | `this.property` |
| Return Value | `return` statement |
| Call Method | `object.method()` |
| Best Practice | Use ES6 methods with `this` |