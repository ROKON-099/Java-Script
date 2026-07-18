# JavaScript Loops

## What is a Loop?

A **loop** is a programming structure that allows you to execute the same block of code multiple times until a specified condition becomes false.

Instead of writing the same code repeatedly, you can use loops to automate repetitive tasks.

---

# Why Do We Use Loops?

Loops help us:

- Execute code multiple times
- Iterate through arrays
- Process data efficiently
- Reduce duplicate code
- Improve readability

---

# Types of Loops

1. for Loop
2. while Loop
3. do...while Loop
4. for...of Loop
5. for...in Loop

---

# 1. for Loop

## Definition

The `for` loop is used when the number of iterations is known.

## Syntax

```javascript
for (initialization; condition; update) {
    // code
}
```

### Parts of a for Loop

| Part | Purpose |
|------|----------|
| Initialization | Runs once before the loop starts |
| Condition | Checked before every iteration |
| Update | Runs after each iteration |

---

## Example

```javascript
for(let i = 1; i <= 5; i++){
    console.log(i);
}
```

### Output

```
1
2
3
4
5
```

---

## Step by Step

Iteration 1

```
i = 1

1 <= 5

true

Print 1

i++
```

Iteration 2

```
i = 2

Print 2
```

...

Iteration 5

```
Print 5
```

Iteration 6

```
i = 6

6 <= 5

false

Loop Stops
```

---

# Real Project Example

Display product numbers.

```javascript
for(let i = 1; i <= 10; i++){
    console.log(`Product ${i}`);
}
```

---

# 2. while Loop

## Definition

The `while` loop executes as long as the condition remains true.

## Syntax

```javascript
while(condition){
    // code
}
```

---

## Example

```javascript
let i = 1;

while(i <= 5){
    console.log(i);
    i++;
}
```

### Output

```
1
2
3
4
5
```

---

# Real Project Example

Loading data from an API until all pages are fetched.

---

# 3. do...while Loop

## Definition

The `do...while` loop executes the code **at least once**, even if the condition is false.

## Syntax

```javascript
do{

}while(condition);
```

---

## Example

```javascript
let i = 10;

do{
    console.log(i);
    i++;
}while(i < 5);
```

### Output

```
10
```

---

# Why?

The code inside `do` executes first.

Then JavaScript checks the condition.

---

# 4. for...of Loop

## Definition

The `for...of` loop is used to iterate over iterable objects like arrays and strings.

---

## Example

```javascript
const fruits = ["Apple","Mango","Orange"];

for(const fruit of fruits){
    console.log(fruit);
}
```

### Output

```
Apple
Mango
Orange
```

---

# String Example

```javascript
const name = "Rokon";

for(const letter of name){
    console.log(letter);
}
```

### Output

```
R
o
k
o
n
```

---

# Real Project Example

Display all products.

```javascript
for(const product of products){
    console.log(product.name);
}
```

---

# 5. for...in Loop

## Definition

The `for...in` loop is used to iterate over object properties.

---

## Example

```javascript
const student = {
    name: "Rokon",
    age: 23,
    country: "Bangladesh"
};

for(const key in student){
    console.log(key);
}
```

### Output

```
name
age
country
```

---

## Get Values

```javascript
for(const key in student){
    console.log(student[key]);
}
```

### Output

```
Rokon
23
Bangladesh
```

---

# Loop Control Statements

## break

Stops the loop immediately.

### Example

```javascript
for(let i=1;i<=10;i++){

    if(i===5){
        break;
    }

    console.log(i);

}
```

### Output

```
1
2
3
4
```

---

## continue

Skips the current iteration.

### Example

```javascript
for(let i=1;i<=5;i++){

    if(i===3){
        continue;
    }

    console.log(i);

}
```

### Output

```
1
2
4
5
```

---

# Nested Loop

A loop inside another loop.

```javascript
for(let row=1; row<=3; row++){

    for(let col=1; col<=3; col++){

        console.log(row,col);

    }

}
```

---

# Common Loop Examples

## Print Numbers

```javascript
for(let i=1;i<=100;i++){
    console.log(i);
}
```

---

## Print Even Numbers

```javascript
for(let i=2;i<=20;i+=2){
    console.log(i);
}
```

---

## Print Odd Numbers

```javascript
for(let i=1;i<=20;i+=2){
    console.log(i);
}
```

---

## Sum of Numbers

```javascript
let sum = 0;

for(let i=1;i<=5;i++){
    sum += i;
}

console.log(sum);
```

Output

```
15
```

---

## Multiplication Table

```javascript
let number = 5;

for(let i=1;i<=10;i++){
    console.log(`${number} x ${i} = ${number*i}`);
}
```

---

# Which Loop Should You Use?

| Loop | Best Use |
|------|----------|
| for | Known number of iterations |
| while | Unknown number of iterations |
| do...while | Run at least once |
| for...of | Arrays & Strings |
| for...in | Objects |

---

# Best Practices

✅ Use `for` when you know how many times to loop.

✅ Use `for...of` for arrays.

✅ Use `for...in` for objects.

✅ Avoid infinite loops.

---

# Common Mistakes

## Forgetting Update

❌

```javascript
let i = 1;

while(i<=5){

    console.log(i);

}
```

Infinite Loop

---

## Wrong Condition

```javascript
for(let i=1;i>=10;i++){
}
```

The loop never executes.

---

# Interview Questions

## What is a loop?

A loop is a control structure that repeatedly executes a block of code while a condition remains true.

---

## Difference between for and while

| for | while |
|------|--------|
| Known iterations | Unknown iterations |
| Initialization inside loop | Initialization outside loop |
| Compact syntax | More flexible |

---

## Difference between for...of and for...in

| for...of | for...in |
|------------|-----------|
| Arrays | Objects |
| Returns values | Returns keys |

---

# Summary

| Loop | Used For |
|------|----------|
| for | Fixed iterations |
| while | Unknown iterations |
| do...while | Executes at least once |
| for...of | Arrays & Strings |
| for...in | Objects |
| break | Exit loop |
| continue | Skip current iteration |