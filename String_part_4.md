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

