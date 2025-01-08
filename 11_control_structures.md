### Summary: Control Structures in JavaScript

Control structures allow you to control the flow of execution in your code. This includes conditional statements and loops, which are fundamental to programming.

---

### **1. Conditional Statements**

#### **If Statements**

- Execute a block of code if a condition is true.
- Syntax:
  ```javascript
  if (condition) {
    // Code to execute if condition is true
  }
  ```

#### **If-Else Statements**

- Add an alternative block to execute if the condition is false.
- Syntax:
  ```javascript
  if (condition) {
    // Code if condition is true
  } else {
    // Code if condition is false
  }
  ```

#### **If-Else If Statements**

- Chain multiple conditions.
- Syntax:
  ```javascript
  if (condition1) {
    // Code for condition1
  } else if (condition2) {
    // Code for condition2
  } else {
    // Fallback code if none of the above conditions are true
  }
  ```

#### **Example**:

```javascript
const password = prompt("Enter your password:");

if (password === "hello") {
  console.log("Access granted");
} else if (password === "Hello") {
  console.log("Access granted with case sensitivity");
} else {
  console.log("Access denied");
}
```

---

### **2. Loops**

#### **For Loops**

- Execute a block of code multiple times.

#### **For-Of Loop**

- Used to iterate over arrays or iterable objects.
- Syntax:
  ```javascript
  const array = ["Item1", "Item2"];
  for (const item of array) {
    console.log(item);
  }
  ```

**Example**:

```javascript
const hobbies = ["Sports", "Cooking"];
for (const hobby of hobbies) {
  console.log(hobby); // Outputs: Sports, Cooking
}
```

---

### **3. Key Points**

#### **Comparison Operators**:

- `===`: Strict equality (value and type must match).
- `!==`: Strict inequality.
- `<`, `>`, `<=`, `>=`: Relational comparisons.

#### **Prompt Function**:

- Used to get user input in the browser:
  ```javascript
  const input = prompt("Enter something:");
  console.log(input);
  ```

#### **For Loops in Arrays**:

- Use the `for-of` loop to iterate through arrays easily.

---

### **4. Example Combining If Statements and Loops**

```javascript
const passwords = ["hello", "world", "JavaScript"];

for (const password of passwords) {
  if (password === "JavaScript") {
    console.log("Special password found!");
  } else {
    console.log(`Password checked: ${password}`);
  }
}
```

**Output**:

```
Password checked: hello
Password checked: world
Special password found!
```

---

### **5. Practical Use**

Control structures like `if-else` and `for-of` loops are foundational in all JavaScript applications, enabling you to handle dynamic conditions and iterate over data effectively. They are widely used in React, for tasks like conditional rendering and iterating over component lists.
