### JavaScript Writeup: Strict Mode, Variables, Comments, Data Types, and Control Structures

This writeup covers essential JavaScript concepts, including **strict mode**, **variables**, **comments**, **data types**, and **control structures** like `if`, `switch`, `while`, and `do-while` loops.

---

## **1. Strict Mode in JavaScript**
Strict mode is a feature in JavaScript that enforces stricter parsing and error handling in your code. It helps you write cleaner, more secure, and optimized JavaScript.

### **Key Features of Strict Mode:**
- Prevents the use of undeclared variables.
- Disallows duplicate parameter names in functions.
- Throws errors for assignments to non-writable properties.
- Makes `eval` and `arguments` behave more predictably.
- Prohibits the use of `with` statements.

### **How to Enable Strict Mode:**
Add the `"use strict";` directive at the beginning of a script or function.

#### **Example:**
```javascript
"use strict";

x = 10; // Throws an error because 'x' is not declared
```

#### **References:**
1. [Sentry.io: JavaScript Use Strict](https://sentry.io/answers/javascript-use-strict/)
2. [MDN: Strict Mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)

---

## **2. JavaScript Variables**
Variables are used to store data in JavaScript. You can declare variables using `var`, `let`, or `const`.

### **Variable Syntax:**
```javascript
keyword | variable name | assignment operator | variable value
var x = 100;
let y = 200;
const z = 300;
```

### **Differences Between `var`, `let`, and `const`:**
| Feature                  | `var`                     | `let`                     | `const`                   |
|--------------------------|---------------------------|---------------------------|---------------------------|
| **Redeclare**            | Allowed (no error)        | Not allowed (error)       | Not allowed (error)       |
| **Access Before Declare**| `undefined`              | Throws an error          | Throws an error          |
| **Scope**                | Function or global scope | Block scope              | Block scope              |
| **Add to Window Object** | Yes                      | No                       | No                       |

#### **Examples:**
```javascript
var a = 10;
var a = 20; // No error

let b = 30;
let b = 40; // Error: Identifier 'b' has already been declared

const c = 50;
c = 60; // Error: Assignment to constant variable
```

---

## **3. JavaScript Comments**
Comments are used to explain code and make it more readable. They are ignored by the JavaScript engine.

### **Types of Comments:**
1. **Single-line Comment:**
   ```javascript
   // This is a single-line comment
   ```

2. **Multi-line Comment:**
   ```javascript
   /*
   This is a
   multi-line comment
   */
   ```

---

## **4. JavaScript Data Types**
JavaScript has 8 basic data types:

### **1. Numbers:**
```javascript
let length = 16;
let weight = 7.5;
```

### **2. Strings:**
```javascript
let color = "Yellow";
let lastName = "Johnson";
```

### **3. Booleans:**
```javascript
let x = true;
let y = false;
```

### **4. Objects:**
```javascript
const person = { firstName: "John", lastName: "Doe" };
```

### **5. Arrays:**
```javascript
const cars = ["Saab", "Volvo", "BMW"];
```

### **6. Dates:**
```javascript
const date = new Date("2022-03-25");
```

### **7. Undefined:**
```javascript
let z; // z is undefined
```

### **8. Null:**
```javascript
let value = null; // Represents an intentional absence of any object value
```

---

## **5. Control Structures**

### **1. `if` Condition:**
Used to execute a block of code if a condition is true.
```javascript
if (condition) {
  // Block of code
}
```

#### **Example:**
```javascript
let age = 18;
if (age >= 18) {
  console.log("You are an adult.");
}
```

---

### **2. `switch` Statement:**
Used to perform different actions based on different conditions.
```javascript
switch (condition) {
  case 1:
    // Code for case 1
    break;
  case 2:
    // Code for case 2
    break;
  default:
    // Code if no case matches
}
```

#### **Example:**
```javascript
let day = 3;
switch (day) {
  case 1:
    console.log("Monday");
    break;
  case 2:
    console.log("Tuesday");
    break;
  default:
    console.log("Invalid day");
}
```

---

### **3. `while` Loop:**
Repeats a block of code as long as a condition is true.
```javascript
while (condition) {
  // Code block to be executed
}
```

#### **Example:**
```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

---

### **4. `do-while` Loop:**
Similar to `while`, but the block of code is executed at least once, even if the condition is false.
```javascript
do {
  // Code block to be executed
} while (condition);
```

#### **Example:**
```javascript
let j = 0;
do {
  console.log(j);
  j++;
} while (j < 5);
```

---

## **Summary**
- **Strict Mode:** Enforces stricter rules for cleaner and safer code.
- **Variables:** Use `var`, `let`, or `const` to declare variables.
- **Comments:** Use `//` for single-line and `/* ... */` for multi-line comments.
- **Data Types:** JavaScript has 8 basic data types, including numbers, strings, booleans, objects, arrays, and dates.
- **Control Structures:** Use `if`, `switch`, `while`, and `do-while` to control the flow of your program.

By mastering these concepts, you can write efficient and maintainable JavaScript code.
