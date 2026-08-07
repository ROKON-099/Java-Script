# ES6 Import & Export

> Beginner → Advanced Guide for Software Development



#  What is Import & Export?

## English

Import and Export are ES6 Module features that allow us to share code between different JavaScript files.

## বাংলা

Import এবং Export হলো ES6-এর একটি গুরুত্বপূর্ণ Feature যার মাধ্যমে আমরা একটি JavaScript File-এর Variable, Function, Class অথবা Component অন্য File-এ ব্যবহার করতে পারি।

সহজ ভাষায়,

ধরো তুমি একটি React Project বানাচ্ছো।

```
src/
```

এর ভিতরে আছে

```
Navbar.jsx
Footer.jsx
Hero.jsx
App.jsx
```

এখন যদি Import/Export না থাকত তাহলে Navbar, Footer, Hero—সব কোড App.jsx-এর ভিতর লিখতে হতো।

Project বড় হলে App.jsx ৮০০০-১০,০০০ লাইন হয়ে যেত।

তাই React-এ প্রতিটি Component আলাদা File-এ রাখা হয় এবং Import/Export দিয়ে ব্যবহার করা হয়।



#  Why Learn Import & Export?

কারণ React-এর প্রায় প্রতিটি File-এ এটি ব্যবহার করা হয়।

উদাহরণ

```jsx
import Navbar from "./components/Navbar";
```

অথবা

```jsx
import { useState } from "react";
```

Import/Export না জানলে React-এর কোনো Project বুঝতে পারবে না।



#  Theory

ধরো তোমার একটি Library আছে।

Library-তে অনেক বই আছে।

এখন কেউ যদি একটি বই নিতে চায়,

তাহলে Library বইটি বাইরে দেয়।

এটিই Export।

আর যে ব্যক্তি বইটি নেয়,

সে Import করে।

JavaScript-এও একই বিষয়।

```
File A

↓

Export

↓

File B

↓

Import

↓

Use
```



#  Syntax

Named Export

```js
export const name = "Rokon";
```

Import

```js
import { name } from "./user";
```



Default Export

```js
export default Navbar;
```

Import

```js
import Navbar from "./Navbar";
```



# 💻 Example 1

user.js

```js
export const name = "Rokon";
export const age = 23;
```

app.js

```js
import { name, age } from "./user";

console.log(name);
console.log(age);
```

Output

```
Rokon
23
```



# 🔍 Code Explanation

```js
export const name = "Rokon";
```

### Explanation

- `export` → অন্য File-এ পাঠানোর জন্য।
- `const` → Variable তৈরি করছে।
- `"Rokon"` → Value।



```js
import { name } from "./user";
```

### Explanation

- `import` → অন্য File থেকে আনছে।
- `{}` → কারণ এটি Named Export।
- `"./user"` → File Path।



#  Real Project Example

ধরো তুমি একটি E-Commerce Website বানাচ্ছো।

Folder Structure

```
src/

components/

Navbar.jsx

Footer.jsx

ProductCard.jsx

pages/

Home.jsx

Cart.jsx

App.jsx
```

Navbar.jsx

```jsx
const Navbar = () => {
    return <h1>Navbar</h1>;
};

export default Navbar;
```

App.jsx

```jsx
import Navbar from "./components/Navbar";

function App() {
    return (
        <>
            <Navbar />
        </>
    );
}
```

### এখানে কী হলো?

Navbar Component আলাদা File-এ লেখা হয়েছে।

তারপর App.jsx সেটিকে Import করে ব্যবহার করছে।

এটাই Professional React Development-এর Standard।


