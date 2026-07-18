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

