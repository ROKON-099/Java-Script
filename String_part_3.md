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
## Example

```javascript
let text = "Hi ";

console.log(text.repeat(3));
```

Output

```
Hi Hi Hi
```

---

## Real Project Example

```javascript
console.log("-".repeat(40));
```

Output

```
----------------------------------------
```

Useful for console formatting.

---

# 5. charAt()

## Definition

The `charAt()` method returns the character at a specified index.

---

## Syntax

```javascript
string.charAt(index)
```

---

## Example

```javascript
let language = "JavaScript";

console.log(language.charAt(0));
```

### Output

```
J
```

---

## Example

```javascript
console.log(language.charAt(4));
```

Output

```
S
```

---

## Another Way

```javascript
console.log(language[4]);
```

Output

```
S
```

Modern JavaScript usually prefers bracket notation.

---

# 6. indexOf()

## Definition

The `indexOf()` method returns the **first index** of a specified value.

If the value is not found, it returns **-1**.

---

## Syntax

```javascript
string.indexOf(searchValue)
```

---

## Example

```javascript
let language = "JavaScript";

console.log(language.indexOf("Script"));
```

### Output

```
4
```

---

## Example

```javascript
console.log(language.indexOf("Python"));
```

Output

```
-1
```

---

## Real Project Example

```javascript
let email = "admin@gmail.com";

if(email.indexOf("@") !== -1){
    console.log("Valid Email");
}
```

Output

```
Valid Email
```

---

# 7. lastIndexOf()

## Definition

The `lastIndexOf()` method returns the **last occurrence** of a value.

---

## Syntax

```javascript
string.lastIndexOf(searchValue)
```

---

## Example

```javascript
let text = "Java Java Java";

console.log(text.lastIndexOf("Java"));
```

### Output

```
10
```

---

## Example

```javascript
let sentence = "one two one";

console.log(sentence.lastIndexOf("one"));
```

Output

```
8
```

---

# Real Project Example

```javascript
let file = "photo.backup.jpg";

console.log(file.lastIndexOf("."));
```

Output

```
12
```

Useful for finding file extensions.

---

# Summary Table

| Method | Purpose | Returns |
|----------|----------|----------|
| replace() | Replace first match | String |
| replaceAll() | Replace all matches | String |
| split() | Convert string to array | Array |
| repeat() | Repeat string | String |
| charAt() | Character at index | String |
| indexOf() | First occurrence | Number |
| lastIndexOf() | Last occurrence | Number |

---

# Most Frequently Used

⭐⭐⭐⭐⭐

- split()
- replace()
- indexOf()

⭐⭐⭐⭐

- replaceAll()
- charAt()

⭐⭐⭐

- repeat()
- lastIndexOf()

---

# Common Mistakes

### replace()

❌ Expecting all matches to be replaced.

```javascript
"Java Java".replace("Java","JS")
```

Output

```
JS Java
```

---

### split()

Using the wrong separator.

```javascript
"HTML CSS".split(",")
```

Output

```javascript
["HTML CSS"]
```

---

### indexOf()

Always check for `-1`.

```javascript
if(text.indexOf("Java") !== -1){
    console.log("Found");
}
```

---

# Interview Questions

## Q1. What is the difference between replace() and replaceAll()?

| replace() | replaceAll() |
|------------|--------------|
| Replaces first occurrence | Replaces all occurrences |

---

## Q2. Which method converts a string into an array?

```
split()
```

---

## Q3. Which method repeats a string?

```
repeat()
```

---

## Q4. Which method returns the first occurrence?

```
indexOf()
```

---

## Q5. Which method returns the last occurrence?

```
lastIndexOf()
```

---

## Q6. Which method returns a character at a specific position?

```
charAt()
```
