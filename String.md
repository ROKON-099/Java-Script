# JavaScript Strings

## What is a String?

### Definition

A **String** is a sequence of characters used to represent text in JavaScript.

A string can contain:

- Letters
- Numbers
- Symbols
- Spaces
- Special Characters

Strings are enclosed in:

- Single Quotes (`' '`)
- Double Quotes (`" "`)
- Backticks (`` ` ` ``)

---

## Why Do We Use Strings?

Strings are used to store textual data such as:

- User Name
- Email
- Password
- Address
- Messages
- Product Name
- City Name

---

## Creating Strings

There are three ways to create a string.

### 1. Using Double Quotes

```javascript
let name = "Rokon";

console.log(name);
```

### Output

```
Rokon
```

---

### 2. Using Single Quotes

```javascript
let country = 'Bangladesh';

console.log(country);
```

### Output

```
Bangladesh
```

---

### 3. Using Backticks (Template Literals)

```javascript
let language = `JavaScript`;

console.log(language);
```

### Output

```
JavaScript
```

---

## String Examples

```javascript
let firstName = "MD";
let lastName = "Rokonuzzaman";

console.log(firstName);
console.log(lastName);
```

### Output

```
MD
Rokonuzzaman
```

---

## String Length

### Definition

The **length** property returns the total number of characters in a string.

It counts:

- Letters
- Numbers
- Spaces
- Symbols

Everything counts as one character.

---

## Syntax

```javascript
string.length
```

---

## Example 1

```javascript
let name = "JavaScript";

console.log(name.length);
```

### Output

```
10
```

---

## Example 2

```javascript
let text = "Hello World";

console.log(text.length);
```

### Output

```
11
```

Explanation

```
H e l l o _ W o r l d
1 2 3 4 5 6 7 8 9 10 11

Space is also counted.
```

---

## Real Project Example

Check password length.

```javascript
let password = "abc12345";

if(password.length >= 8){
    console.log("Strong Password");
}else{
    console.log("Weak Password");
}
```

### Output

```
Strong Password
```

---

# Character Access

## Definition

Each character in a string has its own position called an **index**.

JavaScript starts counting from **0**.

---

## Example

```javascript
let language = "JavaScript";
```

```
Character

J  a  v  a  S  c  r  i  p  t

Index

0  1  2  3  4  5  6  7  8  9
```

---

## Access Using Index

```javascript
let language = "JavaScript";

console.log(language[0]);
console.log(language[1]);
console.log(language[4]);
```

### Output

```
J
a
S
```

---

## Last Character

```javascript
let language = "JavaScript";

console.log(language[language.length-1]);
```

### Output

```
t
```

---

## Loop Through a String

```javascript
let text = "Code";

for(let i=0;i<text.length;i++){

    console.log(text[i]);

}
```

### Output

```
C
o
d
e
```

---

# Immutable

## Definition

Strings are **immutable**.

Immutable means **once a string is created, its characters cannot be changed directly**.

You cannot modify an existing character using its index.

---

## Wrong Example

```javascript
let name = "Rokon";

name[0] = "M";

console.log(name);
```

### Output

```
Rokon
```

Nothing changes.

---

## Why?

JavaScript does not allow changing individual characters of a string.

Instead, create a new string.

---

## Correct Way

```javascript
let name = "Rokon";

name = "Mokon";

console.log(name);
```

### Output

```
Mokon
```

---

## Another Example

```javascript
let text = "Hello";

text = text + " World";

console.log(text);
```

### Output

```
Hello World
```

JavaScript creates a **new string** instead of changing the old one.

---

# Escape Characters

## Definition

Escape characters allow special characters to be included inside a string.

They start with a backslash (`\`).

---
## Common Escape Characters

| Escape | Meaning |
|---------|---------|
| `\"` | Double Quote |
| `\'` | Single Quote |
| `\\` | Backslash |
| `\n` | New Line |
| `\t` | Tab |

---

## Double Quote Example

```javascript
let text = "He said, \"Hello\"";

console.log(text);
```

### Output

```
He said, "Hello"
```

---

## Single Quote Example

```javascript
let text = 'It\'s JavaScript';

console.log(text);
```

### Output

```
It's JavaScript
```

---

## New Line

```javascript
let text = "HTML\nCSS\nJavaScript";

console.log(text);
```

### Output

```
HTML
CSS
JavaScript
```

---

## Tab

```javascript
let text = "Name\tAge";

console.log(text);
```

### Output

```
Name    Age
```

---

## Backslash

```javascript
let path = "C:\\Users\\Admin";

console.log(path);
```

### Output

```
C:\Users\Admin
```

---

# Best Practices

✅ Use double quotes or single quotes consistently.

```javascript
let name = "Rokon";
```

---

✅ Use template literals when inserting variables.

```javascript
let name = "Rokon";

console.log(`Welcome ${name}`);
```

---

✅ Use `.length` instead of manually counting characters.

---

# Common Mistakes

### Forgetting Quotes

❌

```javascript
let name = Rokon;
```

Error

---

### Wrong Index

```javascript
let name = "Java";

console.log(name[10]);
```

Output

```
undefined
```

---

### Trying to Modify a Character

❌

```javascript
let name = "Java";

name[0] = "C";
```

Output

```
Java
```

---

# Interview Questions

## What is a String?

A string is a sequence of characters used to represent text in JavaScript.

---

## What is String Length?

The `length` property returns the total number of characters in a string.

---

## What does Immutable mean?

Immutable means the value cannot be changed after it is created. Strings in JavaScript are immutable.

---

## What is Character Index?

An index is the position of a character inside a string. Indexing starts from **0**.

---

## Summary

| Topic | Description |
|---------|-------------|
| String | Sequence of characters |
| Quotes | Single, Double, Backticks |
| length | Returns total characters |
| Character Access | Uses index starting from 0 |
| Immutable | Characters cannot be changed directly |
| Escape Characters | Special characters inside strings |
