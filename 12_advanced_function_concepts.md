### Summary: Advanced Function Concepts in JavaScript

JavaScript's flexibility with functions enables powerful and expressive programming patterns. These concepts are foundational for modern JavaScript applications and frameworks like React.

---

### **1. Selecting DOM Elements**

- **Direct DOM Manipulation**:
  - JavaScript can manipulate the DOM manually using methods like `querySelector`.
  - Example:
    ```javascript
    const element = document.querySelector("#myElement");
    element.remove(); // Removes the selected element
    ```
- **React vs. Vanilla JS**:
  - In React, DOM manipulation is handled declaratively through state and JSX, so manual DOM interaction is rare.

---

### **2. Passing Functions as Arguments**

- Functions in JavaScript can be passed as **values** to other functions, enabling dynamic behavior.

**Using `setTimeout`**:

```javascript
function handleTimeout() {
  console.log("Timed out");
}

// Pass the function as a value
setTimeout(handleTimeout, 2000); // Executes after 2 seconds
```

**Anonymous Functions**:

- Instead of defining a separate function, you can pass an anonymous function:

```javascript
setTimeout(() => {
  console.log("Timed out");
}, 2000);
```

**Important**:

- When passing functions as arguments, **omit parentheses** unless you want to execute the function immediately:

  ```javascript
  // Pass the function (correct)
  setTimeout(handleTimeout, 2000);

  // Execute immediately and pass the return value (incorrect for this use case)
  setTimeout(handleTimeout(), 2000);
  ```

**Custom Functions**:

- Functions can also accept other functions as parameters:

  ```javascript
  function greeter(greetFn) {
    greetFn();
  }

  greeter(() => console.log("Hi")); // Output: Hi
  ```

---

### **3. Nested Functions**

- Functions can be defined **inside other functions**. Inner functions are **scoped** to their containing function and cannot be accessed outside.

**Example**:

```javascript
function init() {
  function greet() {
    console.log("Hi");
  }
  greet(); // Inner function executed here
}

init(); // Executes greet via init
// greet(); // Error: greet is not defined outside init
```

**Use in React**:

- Nested functions are common for encapsulating logic or creating closures in React components.

---

### **4. Key Features in Action**

#### **setTimeout Example**:

```javascript
setTimeout(() => console.log("This is delayed"), 3000); // Executes after 3 seconds
```

#### **Custom Function with Callback**:

```javascript
function processArray(arr, callback) {
  for (const item of arr) {
    callback(item);
  }
}

processArray([1, 2, 3], (num) => console.log(num * 2));
// Output: 2, 4, 6
```

#### **Nested Function Example**:

```javascript
function outer() {
  const outerVar = "I am outer";

  function inner() {
    console.log(outerVar); // Access outer scope
  }

  inner();
}

outer(); // Output: I am outer
```

---

### **5. Use Cases**

- **Passing Functions**:
  - Dynamic behavior in libraries (e.g., `setTimeout`, event handlers).
  - React: Passing event handlers as props.
- **Nested Functions**:
  - Encapsulating logic.
  - Creating closures to manage scope and variables.
- **Anonymous Functions**:
  - Cleaner and more concise code for single-use functions.

---

### **6. Summary**

- **Passing Functions**:
  - Functions can be passed as values to other functions.
  - Anonymous functions and arrow functions provide concise syntax.
- **Nested Functions**:
  - Functions defined inside others are scoped to their parent.
  - Useful for encapsulation and managing dependencies.
- **React Connection**:
  - React heavily relies on passing and defining functions (e.g., event handlers, functional components). These patterns are essential for React development.
