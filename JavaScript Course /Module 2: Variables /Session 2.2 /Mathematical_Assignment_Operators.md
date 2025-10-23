# Session 2.2 - Mathematical Assignment Operators

In JavaScript, basic mathematical assignment operators provide a shorthand method for performing calculations and assigning the resulting value back to the original variable. These operators function similarly to arithmetic operators, combining distinct arithmetic operations with assignment. Remember, they facilitate mathematical calculations on numerical values and allow for the return of a resultant value.

### Arithmetic Operators:

- `+` **Addition**:

      let z = x + y;
- `-` **Subtraction**:

      let z = x - y;
- `*` **Multiplication**:

      let z = x * y;
- `/` **Division**:

      let z = x / y;
- `%` **Modulo** - (returns the remainder of a division):

      let z = x % y;
- `**` **Exponentiation**:

      let z = x ** y;

Suppose we perform a calculation using variables declared with `let`:

    let x = 12;
    let y = 4;

    // The + is an arithmetic operator.
    let z = x + y; 

    console.log(z); // 16
    console.log(x); // 12 (x is unchanged)

The variable `x` remains unchanged because the addition operation creates a new value rather than modifying `x`.

### Mathematical Assignment Operators:

Mathematical assignment operators are a shorthand that combines an arithmetic operation with the `=` (assignment) operator. They modify the variable's value directly. :gear:

This is the fundamental assignment operator `=`, used to assign a value to a variable.

    let x = 10; // Assigns the value 10 to x
Here are the common mathematical assignment operators in JavaScript:

- `+=` **Addition Assignment**:

      x += y; // equivalent to x = x + y;
Adds the right operand to the left operand and assigns the result to the left operand.

      let x = 5;
      x += 3; // x is now 8 (5 + 3)
- `-=` **Subtraction Assignment**:

      x -= y; // equivalent to x = x - y;
Subtracts the right operand from the left operand and assigns the result to the left operand.

      let x = 10;
      x -= 4; // x is now 6 (10 - 4)
- `*=` **Multiplication Assignment**:

      x *= y; // equivalent to x = x * y;
Multiplies the left operand by the right operand and assigns the result to the left operand.

      let x = 2;
      x *= 5; // x is now 10 (2 * 5)
- `/=` **Division Assignment**:

      x /= y; // equivalent to x = x / y;
Divides the left operand by the right operand and assigns the result to the left operand.

      let x = 12;
      x /= 3; // x is now 4 (12 / 3)
- `%=` **Remainder Assignment**:

      x %= y; // equivalent to x = x % y;
Divides the left operand by the right operand and assigns the remainder to the left operand.

      let x = 10;
      x %= 3; // x is now 1 (remainder of 10 / 3)
- `**=` **Exponentiation Assignment**:

      x **= y; // equivalent to x = x ** y;
Raises the left operand to the power of the right operand and assigns the result to the left operand.

      let x = 2;
      x **= 3; // x is now 8 (2 to the power of 3)
      
:bulb: The primary distinction is their purpose: arithmetic operators perform calculations, while mathematical assignment operators perform a calculation and then immediately assign the result back to the original variable. The general form of a compound assignment operator is `op=`, where `op` is a mathematical operator and `=` is the assignment operator.

Let's say a compound mathematical assignment operator is a shorthand way to perform an arithmetic operation and assign the result to the same variable. For example, instead of writing `x = x + 5;`, you can use the more concise `x += 5;`.

Because these operators offer a more compact and often more readable way to modify variable values compared to explicitly writing out the full `variable = variable op value` expression.

Here is the summary of assignment operators in a table:
| Operator | Description               | Example   | Equivalent To |
| -------- | ------------------------- | --------- | ------------- |
| `+=`     | Addition assignment       | `x += y`  | `x = x + y`   |
| `-=`     | Subtraction assignment    | `x -= y`  | `x = x - y`   |
| `*=`     | Multiplication assignment | `x *= y`  | `x = x * y`   |
| `/=`     | Division assignment       | `x /= y`  | `x = x / y`   |
| `%=`     | Remainder assignment      | `x %= y`  | `x = x % y`   |
| `**=`    | Exponentiation assignment | `x **= y` | `x = x ** y`  |

### Summary:

Mathematical assignment operators in JavaScript combine arithmetic operations with assignment, allowing you to modify variable values directly. They make your code cleaner, shorter, and more expressive—perfect for updating counters, totals, and scores.
