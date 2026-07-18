# JavaScript String Methods (Part 2)

This section covers the most commonly used string methods in JavaScript.

- toLowerCase()
- toUpperCase()
- trim()
- slice()
- substring()
- concat()
- includes()
- startsWith()
- endsWith()

---

# 1. toLowerCase()

## Definition

The `toLowerCase()` method converts all characters in a string to lowercase.

It does **not** change the original string. It returns a new string.

---

## Syntax

```javascript
string.toLowerCase()
```

---

## Example

```javascript
let text = "HELLO WORLD";

console.log(text.toLowerCase());
```

### Output

```
hello world
```

---

## Real Project Example

Email comparison.

```javascript
let email = "Admin@Gmail.com";

console.log(email.toLowerCase());
```

Output

```
admin@gmail.com
```

---

# 2. toUpperCase()

## Definition

The `toUpperCase()` method converts all characters to uppercase.

It returns a new string.

---

## Syntax

```javascript
string.toUpperCase()
```

---

## Example

```javascript
let text = "javascript";

console.log(text.toUpperCase());
```

### Output

```
JAVASCRIPT
```

---

## Real Project Example

```javascript
let country = "bangladesh";

console.log(country.toUpperCase());
```

Output

```
BANGLADESH
```

---

# 3. trim()

## Definition

The `trim()` method removes whitespace from the beginning and the end of a string.

It does not remove spaces between words.

---

## Syntax

```javascript
string.trim()
```

---

## Example

```javascript
let text = "    Hello World    ";

console.log(text.trim());
```

### Output

```
Hello World
```

---

## Without trim()

```
"     Hello World     "
```

After trim()

```
"Hello World"
```

---

## Real Project Example

User input.

```javascript
let username = "    Rokon    ";

console.log(username.trim());
```

Output

```
Rokon
```

---

# 4. slice()

## Definition

The `slice()` method extracts a part of a string.

The original string is not changed.

---

## Syntax

```javascript
string.slice(start, end)
```

- Start index is included.
- End index is excluded.

---

## Example

```javascript
let language = "JavaScript";

console.log(language.slice(0,4));
```

### Output

```
Java
```

---

## Example 2

```javascript
console.log(language.slice(4));
```

Output

```
Script
```

---

## Negative Index

```javascript
let text = "JavaScript";

console.log(text.slice(-6));
```

Output

```
Script
```

---

## Real Project Example

```javascript
let phone = "01712345678";

console.log(phone.slice(-4));
```

Output

```
5678
```

---

# 5. substring()

## Definition

The `substring()` method extracts characters from a string.

Unlike `slice()`, it does not accept negative indexes.

---

## Syntax

```javascript
string.substring(start,end)
```

---

## Example

```javascript
let language = "JavaScript";

console.log(language.substring(0,4));
```

### Output

```
Java
```

---

## Example

```javascript
console.log(language.substring(4));
```

Output

```
Script
```

---

## Difference Between slice() and substring()

| slice() | substring() |
|-----------|-------------|
| Supports negative index | Does not support negative index |
| More commonly used | Less commonly used |

---

# 6. concat()

## Definition

The `concat()` method joins two or more strings.

---

## Syntax

```javascript
string.concat(string2)
```

---

## Example

```javascript
let firstName = "MD";
let lastName = "Rokon";

console.log(firstName.concat(" ",lastName));
```

### Output

```
MD Rokon
```

---

## Another Way

```javascript
console.log(firstName + " " + lastName);
```

Modern JavaScript usually uses:

```javascript
`${firstName} ${lastName}`
```

---

# 7. includes()

## Definition

The `includes()` method checks whether a string contains a specific value.

It returns:

- true
- false

---

## Syntax

```javascript
string.includes(searchValue)
```

---

## Example

```javascript
let language = "JavaScript";

console.log(language.includes("Script"));
```

### Output

```
true
```

---

## Example

```javascript
console.log(language.includes("Python"));
```

Output

```
false
```

---

## Real Project Example

```javascript
let email = "admin@gmail.com";

console.log(email.includes("@"));
```

Output

```
true
```

---

# 8. startsWith()

## Definition

The `startsWith()` method checks whether a string starts with specific characters.

Returns:

- true
- false

---

## Syntax

```javascript
string.startsWith(value)
```

---

## Example

```javascript
let language = "JavaScript";

console.log(language.startsWith("Java"));
```

### Output

```
true
```

---

## Example

```javascript
console.log(language.startsWith("Script"));
```

Output

```
false
```

---

## Real Project Example

Check URL.

```javascript
let url = "https://google.com";

console.log(url.startsWith("https"));
```

Output

```
true
```

---

# 9. endsWith()

## Definition

The `endsWith()` method checks whether a string ends with specific characters.

Returns:

- true
- false

---

## Syntax

```javascript
string.endsWith(value)
```

---

## Example

```javascript
let language = "JavaScript";

console.log(language.endsWith("Script"));
```

### Output

```
true
```

---

## Example

```javascript
console.log(language.endsWith("Java"));
```

Output

```
false
```

---

## Real Project Example

Check file extension.

```javascript
let file = "resume.pdf";

console.log(file.endsWith(".pdf"));
```

Output

```
true
```

---

# Summary Table

| Method | Purpose | Returns |
|---------|---------|----------|
| toLowerCase() | Converts to lowercase | New String |
| toUpperCase() | Converts to uppercase | New String |
| trim() | Removes leading and trailing spaces | New String |
| slice() | Extracts part of a string | New String |
| substring() | Extracts part of a string | New String |
| concat() | Joins strings | New String |
| includes() | Checks if text exists | Boolean |
| startsWith() | Checks starting text | Boolean |
| endsWith() | Checks ending text | Boolean |

---

# Most Frequently Used Methods

⭐⭐⭐⭐⭐

- trim()
- toLowerCase()
- includes()
- slice()

⭐⭐⭐⭐

- startsWith()
- endsWith()
- concat()

⭐⭐⭐

- substring()

---

# Interview Questions

## Q1. What is the difference between slice() and substring()?

| slice() | substring() |
|-----------|-------------|
| Supports negative index | Does not support negative index |
| More flexible | Simpler |

---

## Q2. Which method removes extra spaces?

```
trim()
```

---

## Q3. Which method checks whether a string contains another string?

```
includes()
```

---

## Q4. Which method converts a string to lowercase?

```
toLowerCase()
```

---

## Q5. Which method checks the beginning of a string?

```
startsWith()
```

---

## Q6. Which method checks the ending of a string?

```
endsWith()
```