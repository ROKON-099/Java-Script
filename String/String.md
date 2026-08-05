# JavaScript String Basics 

## What is a String?

A **String** is a sequence of characters used to store text.

```javascript
let name = "Rokon";
let message = "Welcome to JavaScript";

console.log(name);
```



# 1. length

The `length` property returns the total number of characters in a string.

## Why is it important?

Used for:

- Password Validation
- Username Validation
- Character Counting

### Example

```javascript
let password = "abcd1234";

console.log(password.length);
```

Output

```javascript
8
```

### Real Project

```javascript
let password = "abcd1234";

if (password.length >= 8) {
  console.log("Strong Password");
} else {
  console.log("Password must be at least 8 characters.");
}
```



# 2. Character Access

You can access individual characters using **index** or `charAt()`.

### Example

```javascript
let name = "Rokon";

console.log(name[0]);
console.log(name.charAt(1));
```

Output

```javascript
R
o
```

## Real Project

Display the first letter of a user's name.

```javascript
let username = "rokon";

let avatar = username[0].toUpperCase();

console.log(avatar);
```

Output

```javascript
R
```



# 3. Template Literals

Template Literals use **backticks (` `)** and `${}`.

They make string concatenation easier.

### Without Template Literal

```javascript
let name = "Rokon";

console.log("Welcome " + name);
```

### With Template Literal

```javascript
let name = "Rokon";

console.log(`Welcome ${name}`);
```

Output

```javascript
Welcome Rokon
```

## Real Project

```javascript
let product = "Laptop";
let price = 65000;

console.log(`The price of ${product} is ${price} BDT.`);
```



# 4. includes()

Checks whether a string contains another string.

Returns **true** or **false**.

### Example

```javascript
let email = "rokon@gmail.com";

console.log(email.includes("@"));
```

Output

```javascript
true
```

## Real Project

Email Validation

```javascript
let email = "rokongmail.com";

if (!email.includes("@")) {
  console.log("Invalid Email");
}
```



# 5. indexOf()

Returns the first matching index.

### Example

```javascript
let text = "JavaScript";

console.log(text.indexOf("S"));
```

Output

```javascript
4
```

## Real Project

Find the position of `@` in an email.

```javascript
let email = "rokon@gmail.com";

console.log(email.indexOf("@"));
```



# 6. slice()

Extracts part of a string.

Supports **negative index**.

### Example

```javascript
let text = "JavaScript";

console.log(text.slice(0, 4));
console.log(text.slice(-6));
```

Output

```javascript
Java
Script
```

## Real Project

Hide Phone Number

```javascript
let phone = "01712345678";

let hidden = phone.slice(0, 3) + "*****" + phone.slice(-3);

console.log(hidden);
```

Output

```javascript
017*****678
```



# 7. substring()

Works like `slice()`, but **does not support negative index**.

### Example

```javascript
let text = "JavaScript";

console.log(text.substring(0, 4));
```

Output

```javascript
Java
```



# 8. replace()

Replaces only the first matching value.

### Example

```javascript
let text = "I like Java";

console.log(text.replace("Java", "JavaScript"));
```

Output

```javascript
I like JavaScript
```

## Real Project

```javascript
let url = "http://example.com";

console.log(url.replace("http", "https"));
```



# 9. replaceAll()

Replaces every matching value.

### Example

```javascript
let text = "cat cat cat";

console.log(text.replaceAll("cat", "dog"));
```

Output

```javascript
dog dog dog
```

## Real Project

Replace bad words in comments.

```javascript
let comment = "bad bad bad";

console.log(comment.replaceAll("bad", "***"));
```



# 10. trim()

Removes spaces from both ends.

### Example

```javascript
let username = "   Rokon   ";

console.log(username.trim());
```

Output

```javascript
Rokon
```

## Real Project

```javascript
let email = "   rokon@gmail.com   ";

email = email.trim();

console.log(email);
```



# 11. toUpperCase() & toLowerCase()

Convert text to uppercase or lowercase.

### Example

```javascript
let text = "JavaScript";

console.log(text.toUpperCase());
console.log(text.toLowerCase());
```

Output

```javascript
JAVASCRIPT
javascript
```

## Real Project

Case-insensitive Login

```javascript
let email = "Rokon@Gmail.com";

console.log(email.toLowerCase());
```



# 12. split()

Converts a string into an array.

### Example

```javascript
let skills = "HTML,CSS,JavaScript";

console.log(skills.split(","));
```

Output

```javascript
["HTML", "CSS", "JavaScript"]
```

## Real Project

Count Words

```javascript
let sentence = "I Love JavaScript";

console.log(sentence.split(" ").length);
```

Output

```javascript
3
```



# 13. Type Conversion

Convert one data type into another.

## String → Number

```javascript
let price = "500";

console.log(Number(price));
console.log(parseInt(price));
```

## Number → String

```javascript
let age = 23;

console.log(String(age));
console.log(age.toString());
```

## Boolean

```javascript
console.log(Boolean(""));
console.log(Boolean("Hello"));
```

## Real Project

Calculate Total Price

```javascript
let price = "500";
let quantity = "2";

let total = Number(price) * Number(quantity);

console.log(total);
```

Output

```javascript
1000
```



# 14. Regular Expressions (Basic)

Regex is used to search and validate text.

## test()

Returns **true** or **false**.

### Email Validation

```javascript
let email = "rokon@gmail.com";

let pattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

console.log(pattern.test(email));
```

### Phone Validation

```javascript
let phone = "01712345678";

let pattern = /^01[3-9]\d{8}$/;

console.log(pattern.test(phone));
```

### Password Validation

```javascript
let password = "Rokon123";

let pattern = /^(?=.*[A-Z])(?=.*\d).{8,}$/;

console.log(pattern.test(password));
```



# Real Project Exercises

## 1. Search Product

```javascript
let products = ["Laptop", "Phone", "Mouse"];

let search = "lap";

let result = products.filter(product =>
  product.toLowerCase().includes(search.toLowerCase())
);

console.log(result);
```



## 2. Login System

```javascript
let email = "  Rokon@gmail.com ";

email = email.trim().toLowerCase();

console.log(email);
```



## 3. Greeting User

```javascript
let name = "Rokon";

console.log(`Welcome back, ${name}!`);
```



## 4. Generate Username

```javascript
let fullName = "Md Rokonuzzaman";

let username = fullName
  .toLowerCase()
  .replaceAll(" ", "");

console.log(username);
```

Output

```javascript
mdrokonuzzaman
```



## 5. Reverse a String

```javascript
let text = "JavaScript";

let reverse = text.split("").reverse().join("");

console.log(reverse);
```



## 6. Hide Email

```javascript
let email = "rokon@gmail.com";

let hidden =
  email.slice(0, 3) +
  "***" +
  email.slice(email.indexOf("@"));

console.log(hidden);
```

Output

```javascript
rok***@gmail.com
```



## 7. Capitalize First Letter

```javascript
let name = "rokon";

let result =
  name[0].toUpperCase() +
  name.slice(1);

console.log(result);
```

Output

```javascript
Rokon
```



# Most Used String Methods in Software Development

| Method | Common Use |
|--------|------------|
| `length` | Password Validation |
| `trim()` | Login & Signup Forms |
| `includes()` | Search & Email Validation |
| `indexOf()` | Find Character Position |
| `slice()` | Hide Phone, OTP, Email |
| `substring()` | Extract Text |
| `replace()` | Replace First Match |
| `replaceAll()` | Replace All Matches |
| `toUpperCase()` | Display Formatting |
| `toLowerCase()` | Case-Insensitive Search/Login |
| `split()` | Convert String to Array |
| `Template Literals` | Dynamic Messages |
| `Type Conversion` | Form Input & Calculations |
| `Regular Expressions` | Email, Password & Phone Validation |

# Interview Questions

## Q1. What is the difference between `slice()` and `substring()`?

| slice() | substring() |
|-|-|
| Supports negative index | Does not support negative index |
| More flexible | Simpler |



## Q2. What is the difference between `replace()` and `replaceAll()`?

```javascript
let text = "cat cat cat";

console.log(text.replace("cat", "dog"));
// dog cat cat

console.log(text.replaceAll("cat", "dog"));
// dog dog dog
```



## Q3. Why is `trim()` important?

It removes unnecessary spaces before processing user input.

Example:

```javascript
let username = "   rokon   ";

console.log(username.trim());
```



# Conclusion

If you want to become a **Frontend, Backend, MERN Stack, or Full Stack Developer**, these String methods are used almost every day.

**Most Important Topics**

-  length
-  trim()
-  includes()
-  indexOf()
-  slice()
-  replace()
-  replaceAll()
-  split()
-  toLowerCase()
-  toUpperCase()
-  Template Literals
-  Type Conversion
-  Regular Expressions (Regex)

Mastering these topics will help you build **Login Systems, Signup Forms, Search Features, E-commerce Websites, Dashboards, REST APIs, and many real-world web applications.**