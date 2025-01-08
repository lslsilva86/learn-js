### Destructuring in Function Parameter Lists

Destructuring can also be applied directly in function parameter lists, enabling you to "pull out" specific properties or elements from an object or array argument, simplifying access within the function body.

---

### **1. Destructuring Objects in Parameters**

- Instead of accessing object properties using **dot notation**, destructuring allows you to declare variables directly within the parameter list.

**Example Without Destructuring**:

```javascript
function storeOrder(order) {
  localStorage.setItem("id", order.id);
  localStorage.setItem("currency", order.currency);
}
```

**Example With Destructuring**:

```javascript
function storeOrder({ id, currency }) {
  localStorage.setItem("id", id);
  localStorage.setItem("currency", currency);
}
```

- **Key Notes**:
  - The function still accepts **one parameter**, which is the object.
  - The destructured variables (`id`, `currency`) are locally scoped to the function.

**Calling the Function**:

```javascript
storeOrder({ id: 5, currency: "USD", amount: 15.99 });
```

---

### **2. Destructuring Arrays in Parameters**

- Similar syntax applies to arrays, allowing you to extract elements directly.

**Example Without Destructuring**:

```javascript
function processScores(scores) {
  const firstScore = scores[0];
  const secondScore = scores[1];
  console.log(firstScore, secondScore);
}
```

**Example With Destructuring**:

```javascript
function processScores([firstScore, secondScore]) {
  console.log(firstScore, secondScore);
}
```

**Calling the Function**:

```javascript
processScores([95, 88, 76]); // Output: 95 88
```

---

### **3. Combining Destructuring with Default Values**

- Default values can be assigned during destructuring, useful when certain properties or elements might be missing.

**Example**:

```javascript
function storeOrder({ id = 0, currency = "USD", amount = 0 }) {
  console.log(`Order ID: ${id}, Currency: ${currency}, Amount: ${amount}`);
}

storeOrder({ id: 5, currency: "EUR" });
// Output: Order ID: 5, Currency: EUR, Amount: 0
```

---

### **4. Advantages of Using Destructuring in Parameters**

- **Simplifies Code**: Eliminates repetitive access via dot notation.
- **Improves Readability**: Makes the function signature self-documenting by showing what properties are required upfront.
- **Cleaner Function Body**: Reduces boilerplate code inside the function.

---

### **Practical Example**

Destructuring is particularly useful in React for working with props or state:

**Without Destructuring**:

```javascript
function UserDetails(props) {
  console.log(props.name, props.age);
}
```

**With Destructuring**:

```javascript
function UserDetails({ name, age }) {
  console.log(name, age);
}
```

**Usage**:

```javascript
<UserDetails name="John" age={30} />
```

Destructuring in function parameters is a modern and elegant feature that simplifies code, especially when working with objects or arrays. It makes functions cleaner, more expressive, and easier to maintain.
