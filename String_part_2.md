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

