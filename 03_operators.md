### Operators in JavaScript

1. **Arithmetic Operators**:

   - Perform basic math operations:
     - Addition (`+`), Subtraction (`-`), Multiplication (`*`), Division (`/`):
       ```javascript
       console.log(10 + 5); // Output: 15
       console.log("Hello" + "World"); // Output: HelloWorld
       console.log(10 - 5); // Output: 5
       console.log(10 * 2); // Output: 20
       console.log(10 / 2); // Output: 5
       ```

2. **Comparison Operators**:

   - Used to compare values, returning a Boolean (`true` or `false`):
     - Equality (`===`): Checks for strict equality (same value and type).
       ```javascript
       console.log(10 === 5); // Output: false
       console.log(10 === 10); // Output: true
       ```
     - Greater (`>`), Smaller (`<`), Greater or Equal (`>=`), Smaller or Equal (`<=`):
       ```javascript
       console.log(10 > 5); // Output: true
       console.log(5 <= 5); // Output: true
       ```

3. **Conditional Statements**:

   - Operators are often used in `if` statements to control code execution:
     ```javascript
     if (10 === 10) {
       console.log("Condition met!"); // Output: Condition met!
     }
     ```

4. **Key Notes**:
   - The `+` operator can add numbers or concatenate strings.
   - `===` is preferred over `==` for strict type and value equality.
   - Comparison operators (`>`, `<`, etc.) are widely used in conditional logic.

These operators are foundational for building dynamic applications, enabling tasks like calculations, user input validation, and conditional rendering.
