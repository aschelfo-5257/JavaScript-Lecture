# Session 3.3 - Logical Operators

JavaScript logical operators enable the combination or negation of conditions to control program flow, make decisions, and provide alternative values. In a prior session, comparison operators assessed the relationship between two values, consistently resulting in a boolean (`true` or `false`). Their primary application is to link several conditions within `if`, `else if`, and `else` statements. :gear:

### Three Main Logical Operators:
Logical operators allow you to combine or modify Boolean expressions to dictate how a program executes.

- `&&` **(AND):** Returns `true` if both operands are `true` [2].

- `||` **(OR):** Returns `true` if at least one operand is `true` [2].

- `!` **(NOT):** Reverses the boolean value of an operand (e.g., `!true` is `false`) [2].

### Short-Circuit Evaluation:

Short-circuiting occurs when JavaScript evaluates a logical expression from left to right and pauses once the final result is obtained. This indicates that the remaining parts of the expression are completely ignored and never executed.

**Logical AND (`&&`):** If the first operand is `falsy`, the expression immediately returns that falsy value. It does not check the second operand because the overall result cannot possibly be `true`.

- If `age >= 18` is `true` and `hasLicense` is `true`, then the whole expression `age >= 18 && hasLicense` is `true` and the message `"You can drive."` is printed.

      const age = 25;
      const hasLicense = true;
      
      // Both conditions must be true
      if (age >= 18 && hasLicense) {
          console.log("You can drive."); // This will run
      }
      
      console.log(hasLicense);

**Logical OR (`||`)**: If the first operand is `truthy`, the expression immediately returns that truthy value. It skips the second operand because the result is already known to be `true`.

- If `isWeekend` is `true`, the condition `isWeekend || isHoliday` evaluates to `true`, so `"Relax!"` is printed. If both `isWeekend` and `isHoliday` were false, then nothing would print. 

      const isWeekend = true;
      const isHoliday = false;
      
      // Only one condition needs to be true
      if (isWeekend || isHoliday) {
          console.log("Relax!"); // This will run
      }
      
      console.log(isWeekend);
      console.log(isHoliday);

### Negating Conditions:

In JavaScript, logical negation is achieved using the exclamation mark (`!`), known as the logical NOT operator. This unary operator inverts the Boolean value of its operand. 

- `!isRaining` means "if it is NOT raining". Since `isRaining` is `false`, so `!isRaining` is `true`, which makes the `if` condition true and prints `"Go outside."`.

      const isRaining = false;
      
      // If it is NOT raining
      if (!isRaining) {
          console.log("Go outside."); // This will run
      }
      
      console.log(isRaining);

In short:

- `!true` becomes `false`.

- `!false` becomes `true`.

**Caution:** Be mindful when using short-circuiting with functions that have side effects (like updating a database), as they might not run if the expression short-circuits earlier than expected.

:bulb: Logical operators in JavaScript are used to combine or modify boolean (true/false) conditions to control the flow of a program. When used with conditions (like comparisons `>`), logical operators typically return a Boolean value (`true` or `false`). Short-circuit evaluates operands from left to right and stops as soon as the result is determined.

**Decision Making & Control Flow:**

They combine multiple conditions in `if` statements and loops.

- **AND (`&&`):** Ensures a block of code runs only if all conditions are met (e.g., user is logged in AND has permissions).

- **OR (`||`):** Runs code if at least one condition is met (e.g., it is a weekend OR a holiday).

**Value Selection & Defaulting:**

Unlike many other languages, JavaScript's `&&` and `||` return the original value of one of the operands rather than a simple Boolean.

- **Fallback Values:** The `||` operator is frequently used to set defaults (e.g., `let name = userInput || "Guest"`), where it returns the second value if the first is "falsy".

- **Guard Clauses:** The `&&` operator can act as a "gate," only evaluating the right-side expression if the left-side is true.

To understand Logical AND (`&&`), OR (`||`), and NOT (`!`), think of them as tools to combine or reverse conditions that result in `true` or `false`.

      const a = true;
      const b = false;
      
      console.log("a AND b:", a && b);  // false because both are not true
      console.log("a OR b:", a || b);   // true because at least one is true
      console.log("NOT a:", !a);        // false because a is true, NOT reverses it
      console.log("NOT b:", !b);        // true because b is false, NOT reverses it

These operators utilize short-circuit evaluation, meaning that they stop evaluating as soon as the final result is determined. For example, in `false && someFunction()`, the function is never called because the outcome is already known to be false.

Here is a table summarizing the logical operators in JavaScript:

| **Operator** | **Syntax** | **Core Purpose**                | **Typical Return Value**                   |
|--------------|------------|---------------------------------|--------------------------------------------|
| **AND**      | `&&`       | Returns `true` if both are true | First "falsy" value or last "truthy" value |
| **OR**       | `'`        |                                 | `'`                                        |
| **NOT**      | `!`        | Inverts the Boolean value       | Always a Boolean (`true` or `false`)       |

### Summary:

JavaScript employs logical operators to combine or invert Boolean values, influencing program flow. While mainly used with Booleans, they can be applied to various value types. The optimization of logical operators is characterized by short-circuit evaluation, which enhances performance by preventing unnecessary computations.

For more information and interactive examples, refer to https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_operators
