### Functions in JavaScript

1. **Purpose of Functions**:

   - Encapsulate reusable blocks of code.
   - Execute code on-demand by invoking the function.
   - Enhance code clarity and maintainability.

2. **Defining Functions**:

   - Use the `function` keyword followed by a name, parentheses, and curly braces:
     ```javascript
     function greet() {
       console.log("Hello!");
     }
     ```
   - Invoke the function using its name with parentheses:
     ```javascript
     greet(); // Output: Hello!
     ```

3. **Parameters**:

   - Functions can accept input values (parameters) to make them reusable with varying data:
     ```javascript
     function greetUser(userName, message) {
       console.log(userName + ": " + message);
     }
     greetUser("Max", "Hello!"); // Output: Max: Hello!
     ```
   - Use default parameter values if no value is provided during the function call:
     ```javascript
     function greetUser(userName, message = "Hello!") {
       console.log(userName + ": " + message);
     }
     greetUser("Max"); // Output: Max: Hello!
     ```

4. **Returning Values**:

   - Use the `return` keyword to return a value from the function:
     ```javascript
     function createGreeting(userName, message) {
       return `Hi, I am ${userName}. ${message}`;
     }
     const greeting = createGreeting("Max", "Hello!");
     console.log(greeting); // Output: Hi, I am Max. Hello!
     ```

5. **Naming Conventions**:

   - Function names should describe their purpose clearly.
   - Follow **camelCase** for naming.

6. **Best Practices**:

   - Use functions to avoid code repetition.
   - Prefer meaningful names for functions, variables, and parameters.
   - Store returned values in variables or constants for better readability and structure.

7. **Example Workflow**:

   ```javascript
   function calculateSum(a, b) {
     return a + b;
   }

   const result = calculateSum(5, 10);
   console.log(result); // Output: 15
   ```

By understanding and utilizing functions, you can write clean, modular, and efficient JavaScript code. Functions play a central role in React for defining components and managing behavior.
