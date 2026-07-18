# JavaScript Strings (Part 4)

This section covers:

- Reverse a String (3 Methods)
- Real Project Examples
- Common Mistakes
- Interview Questions
- Summary Table

---

# Reverse a String

## What is String Reversal?

Reversing a string means changing the order of its characters from the last character to the first.

Example

```
JavaScript

↓

tpircSavaJ
```

---

# Method 1 (Most Popular)

## split() + reverse() + join()

### Explanation

Step 1

Convert the string into an array.

```
"Java"

↓

["J","a","v","a"]
```

Step 2

Reverse the array.

```
["a","v","a","J"]
```

Step 3

Join the array back into a string.

```
"avaJ"
```

---

## Code

```javascript
let text = "JavaScript";

let reverseText = text.split("").reverse().join("");

console.log(reverseText);
```

### Output

```
tpircSavaJ
```

---

## Step by Step

```javascript
let text = "Code";

console.log(text.split(""));
```

Output

```javascript
["C","o","d","e"]
```

---

```javascript
console.log(text.split("").reverse());
```

Output

```javascript
["e","d","o","C"]
```

---

```javascript
console.log(text.split("").reverse().join(""));
```

Output

```
edoC
```

---

## Advantages

✅ Easy

✅ Short

✅ Most commonly used

---

# Method 2 (Using for Loop)

## Explanation

Start from the last character.

Move toward the first character.

Store every character inside a new string.

---

## Code

```javascript
let text = "JavaScript";

let reverse = "";

for(let i = text.length - 1; i >= 0; i--){

    reverse += text[i];

}

console.log(reverse);
```

### Output

```
tpircSavaJ
```

---

## Visualization

```
Java

Index

0 1 2 3

J a v a

↓

Start

3

↓

a

↓

2

↓

v

↓

1

↓

a

↓

0

↓

J

↓

avaJ
```

---

## Advantages

Good for learning loops.

Frequently asked in interviews.

---

# Method 3 (Using for...of Loop)

## Code

```javascript
let text = "JavaScript";

let reverse = "";

for(const letter of text){

    reverse = letter + reverse;

}

console.log(reverse);
```

### Output

```
tpircSavaJ
```

---

## Explanation

Iteration 1

```
J
```

Reverse

```
J
```

Iteration 2

```
a + J

↓

aJ
```

Iteration 3

```
v + aJ

↓

vaJ
```

Continue...

Final

```
tpircSavaJ
```

---

# Which Method is Best?

| Method | Easy | Interview | Real Project |
|---------|------|-----------|--------------|
| split().reverse().join() | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| for Loop | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| for...of | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ |

---

# Real Project Examples

---

## Username Validation

```javascript
let username = "Rokon";

if(username.length >= 5){

    console.log("Valid Username");

}else{

    console.log("Too Short");

}
```

Output

```
Valid Username
```

---

## Email Validation

```javascript
let email = "admin@gmail.com";

if(email.includes("@")){

    console.log("Valid Email");

}
```

Output

```
Valid Email
```

---

## Password Validation

```javascript
let password = "abc12345";

if(password.length >=8){

    console.log("Strong Password");

}
```

Output

```
Strong Password
```

---

## Search Feature

```javascript
let product = "JavaScript Course";

if(product.toLowerCase().includes("javascript")){

    console.log("Found");

}
```

Output

```
Found
```

---

## Remove Extra Spaces

```javascript
let name = "     Rokon     ";

console.log(name.trim());
```

Output

```
Rokon
```

---

## File Extension Check

```javascript
let file = "resume.pdf";

console.log(file.endsWith(".pdf"));
```

Output

```
true
```

---

## Website URL Check

```javascript
let url = "https://google.com";

console.log(url.startsWith("https"));
```

Output

```
true
```

---

## Display User Name

```javascript
let firstName = "MD";
let lastName = "Rokon";

console.log(`${firstName} ${lastName}`);
```

Output

```
MD Rokon
```

---

# Common Mistakes

---

## Forgetting Quotes

❌

```javascript
let text = JavaScript;
```

Error

---

## Wrong Index

```javascript
let text = "Java";

console.log(text[10]);
```

Output

```
undefined
```

---

## Expecting replace() to Replace Everything

❌

```javascript
let text = "Java Java";

console.log(text.replace("Java","JS"));
```

Output

```
JS Java
```

Use

```javascript
replaceAll()
```

---

## Forgetting trim()

```javascript
let username = "   admin   ";

console.log(username === "admin");
```

Output

```
false
```

Correct

```javascript
username.trim()
```

---

## Using == Instead of ===

❌

```javascript
if(name == "Rokon")
```

Prefer

```javascript
if(name === "Rokon")
```

---

# Interview Questions

## What is a String?

A string is a sequence of characters used to represent text.

---

## Are Strings Mutable?

No.

Strings are immutable.

---

## Which method converts a string into an array?

```
split()
```

---

## Which method removes spaces?

```
trim()
```

---

## Which method converts to lowercase?

```
toLowerCase()
```

---

## Which method checks whether text exists?

```
includes()
```

---

## Which method extracts part of a string?

```
slice()
```

---

## Which method joins strings?

```
concat()
```

---

## How do you reverse a string?

Most common solution

```javascript
text.split("").reverse().join("")
```

---

## Which method returns the total number of characters?

```
length
```

---

## Difference Between slice() and substring()

| slice() | substring() |
|-----------|-------------|
| Supports negative index | Doesn't support negative index |

---

# Summary Table

| Topic | Method | Most Used |
|---------|----------|-----------|
| Convert Lowercase | toLowerCase() | ⭐⭐⭐⭐⭐ |
| Convert Uppercase | toUpperCase() | ⭐⭐⭐⭐ |
| Remove Spaces | trim() | ⭐⭐⭐⭐⭐ |
| Extract String | slice() | ⭐⭐⭐⭐⭐ |
| Extract String | substring() | ⭐⭐⭐ |
| Join Strings | concat() | ⭐⭐⭐ |
| Search Text | includes() | ⭐⭐⭐⭐⭐ |
| Check Start | startsWith() | ⭐⭐⭐⭐ |
| Check End | endsWith() | ⭐⭐⭐⭐ |
| Replace Text | replace() | ⭐⭐⭐⭐⭐ |
| Replace All | replaceAll() | ⭐⭐⭐⭐ |
| Convert to Array | split() | ⭐⭐⭐⭐⭐ |
| Repeat Text | repeat() | ⭐⭐ |
| Character Access | charAt() | ⭐⭐⭐ |
| First Position | indexOf() | ⭐⭐⭐⭐ |
| Last Position | lastIndexOf() | ⭐⭐⭐ |
| Reverse String | split().reverse().join() | ⭐⭐⭐⭐⭐ |

---

# Final Notes

For JavaScript, React, and Node.js development, focus on mastering these methods:

- ✅ length
- ✅ toLowerCase()
- ✅ toUpperCase()
- ✅ trim()
- ✅ slice()
- ✅ includes()
- ✅ replace()
- ✅ split()
- ✅ startsWith()
- ✅ endsWith()
- ✅ indexOf()

These methods are used almost every day in real-world projects and are commonly asked in JavaScript interviews.