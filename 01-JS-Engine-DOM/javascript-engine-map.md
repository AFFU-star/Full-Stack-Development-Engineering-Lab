# JavaScript Engine Architecture

## Why Should We Learn This?

Before writing JavaScript code, developers should understand how the browser executes that code.

Understanding the JavaScript engine helps us:

- Debug errors faster
- Write efficient applications
- Understand memory behavior
- Master asynchronous programming

---

# Browser Architecture

Browser

├── HTML Parser

├── CSS Engine

├── JavaScript Engine

└── Rendering Engine

---

# JavaScript Engine Components

JavaScript Engine

├── Memory Heap

├── Call Stack

└── Event Queue

---

## Memory Heap

Purpose:

Stores objects, arrays and dynamic data.

Example:

```javascript
let student = {
  name: "Affaan",
  cgpa: 9.2
};

Call Stack

Purpose:

Tracks function execution.

Example:
function greet() {
  console.log("Hello");
}

greet();
Execution Flow:

Global()
↓
greet()
↓
console.log()
Event Queue

Purpose:

Stores asynchronous callbacks.

Example:
setTimeout(() => {
  console.log("Done");
}, 1000);
DOM Interaction

HTML

↓

DOM Tree

↓

JavaScript

↓

User Interaction

Example:
document.getElementById("title")

" JavaScript accesses and updates DOM elements through the DOM API. "

Industry Relevance

Where is this used?

React Applications
Node.js Applications
Chrome Browser
Modern Frontend Frameworks
