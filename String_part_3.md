# JavaScript String Methods (Part 3)

This section covers more useful string methods:

- replace()
- replaceAll()
- split()
- repeat()
- charAt()
- indexOf()
- lastIndexOf()

---

# 1. replace()

## Definition

The `replace()` method replaces the **first occurrence** of a specified value in a string.

It returns a **new string** without changing the original string.

---

## Syntax

```javascript
string.replace(searchValue, newValue)
```

---

## Example

```javascript
let text = "I love Java. Java is easy.";

let result = text.replace("Java", "JavaScript");

console.log(result);
```

### Output

```
I love JavaScript. Java is easy.
```

Only the **first** `"Java"` is replaced.

---

## Original String

```javascript
console.log(text);
```

Output

```
I love Java. Java is easy.
```

---

## Real Project Example

Replace spaces with underscores.

```javascript
let fileName = "My Resume.pdf";

console.log(fileName.replace(" ", "_"));
```

Output

```
My_Resume.pdf
```

---

# 2. replaceAll()

## Definition

The `replaceAll()` method replaces **all occurrences** of a value.

---

## Syntax

```javascript
string.replaceAll(searchValue, newValue)
```

---

## Example

```javascript
let text = "Java Java Java";

console.log(text.replaceAll("Java", "JS"));
```

### Output

```
JS JS JS
```

---

## Real Project Example

```javascript
let message = "Hello User. Hello Admin.";

console.log(message.replaceAll("Hello", "Welcome"));
```

Output

```
Welcome User. Welcome Admin.
```

---

# Difference Between replace() and replaceAll()

| replace() | replaceAll() |
|------------|--------------|
| Replaces first match only | Replaces every match |
| More common | Useful for multiple replacements |

---

# 3. split()

## Definition

The `split()` method converts a string into an array.

---

## Syntax

```javascript
string.split(separator)
```

---

## Example

```javascript
let text = "HTML CSS JavaScript";

console.log(text.split(" "));
```

### Output

```javascript
["HTML","CSS","JavaScript"]
```

---

## Split by Comma

```javascript
let fruits = "Apple,Mango,Orange";

console.log(fruits.split(","));
```

Output

```javascript
["Apple","Mango","Orange"]
```

---

## Split Every Character

```javascript
let word = "Code";

console.log(word.split(""));
```

Output

```javascript
["C","o","d","e"]
```

---

## Real Project Example

Tags

```javascript
let skills = "HTML,CSS,JavaScript,React";

let skillArray = skills.split(",");

console.log(skillArray);
```

---

# 4. repeat()

## Definition

The `repeat()` method repeats a string a specified number of times.

---

## Syntax

```javascript
string.repeat(count)
```

---

## Example

```javascript
let star = "*";

console.log(star.repeat(10));
```

### Output

```
**********
```

---

