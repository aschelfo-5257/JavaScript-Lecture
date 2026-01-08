# Session 3.2 - Comparison Operators

JavaScript comparison operators are used to compare two values and return a `Boolean value`, which can be either `true` or `false`. These operators are essential for making decisions and controlling the flow of logic in code. They serve to align values effectively. Conditional operators are commonly encountered and follow familiar syntax. :gear:

### Relational Operators:

Relational operators compare values, which commonly include numbers, although they can also compare strings alphabetically if used properly.

- **Greater Than** (`>`)

- **Less Than** (`<`)

- **Greater Than or Equal** (`>=`)

- **Less Than or Equal** (`<=`)

### Equality Operators:

JavaScript differentiates between "loose" equality (which allows type conversion) and "strict" equality (which does not)

- **Loose Equality** (`==`): Returns `true` if operands are equal after converting them to a common type (coercion). For example, `5 == "5"` is `true`.

- **Strict Equality** (`===`): Returns `true` only if operands have the same value and type. For example, `5 === "5"` is `false`.

- **Loose Inequality** (`!=`): Returns `true` if operands are not equal, with type conversion.

- **Strict Inequality** (`!==`): Returns `true` if operands are not equal in value or type.

Remember, comparison operators are often used within `if...else` statements to determine which block of code should execute.

**Example #1:**

Suppose we will use relational operators `>=` and `<=` to check if a value falls within a specific numeric range:

      let age = 16;

      if (age >= 18) {
        console.log("Eligible to vote.");
      } else {
        console.log("Not eligible to vote");
      }

**Example #2:**

The strict equality operator `===` is the best practice for checking if a value matches a specific target, as it ensures both the value and data type are identical.

      let userRole = "admin";

      if (userRole === "admin") {
        console.log("Access granted to dashboard.");
      } else if (userRole === "editor") {
        console.log("Access granted to content management.");
      } else {
        console.log("Access denied.");
      }

**Example #3:**

The `!==` operator checks if values are not equal. This is useful for excluding specific conditions.

      let currentStatus = "offline";

      if (currentStatus !== "online") {
        console.log("Connection failed. Please retry.");
      }

### Handling `null` and `undefined`:

Special care is needed when comparing `null` and `undefined`.

- `null == undefined` returns `true` (loose equality).

- `null === undefined` returns `false` (strict equality).

- `null >= 0` is `true`, while `null == 0` and `null > 0` are `false`, due to specific type coercion rules. 

:bulb: All comparison operators inherently result in either `true` or `false`. The key concepts revolve around their primary use in conditional logic and how JavaScript handles different types during comparisons. It can be used to determine if one value is greater than, less than, equal to, or not equal to another value.

**Type Coercion (Loose Equality == and !=):**

- The standard equality (`==`) and inequality (`!=`) operators perform type coercion.

- If the operands are of different data types, JavaScript attempts to convert them to a common type (usually a number) before making the comparison.

- For example, the expression `2 == "2"` evaluates to `true` because the string `"2"` is converted to the number `2` before the comparison.

**No Type Coercion (Strict Equality `===` and `!==`):**

- The strict equality (`===`) and strict inequality (`!==`) operators do not perform type conversion.

- The comparison is only true if both the value and the data type are identical.

- For example, the expression `2 === "2"` evaluates to `false` because a number and a string are different types, regardless of their value.

**Important:** It is generally recommended to use the strict operators (`===` and `!==`) to avoid unexpected behavior and potential bugs caused by automatic type coercion.

Here are the comparison operator tables:

| **Operator** | **Name**              | **Description**                                                       | **Type of Coercion?** | **Example** | **Result** |
|--------------|-----------------------|-----------------------------------------------------------------------|-----------------------|-------------|------------|
| `==`         | Equality              | Returns true if operands are equal after type coercion.               | Yes                   | `x == "5"`  | `true`     |
| `===`        | Strict Equality       | Returns true if operands are equal and of the same type.              | No                    | `x === "5"` | `false`    |
| `!=`         | Inequality            | Returns true if operands are not equal, with type coercion.           | Yes                   | `x != 8`    | `true`     |
| `!==`        | Strict Inequality     | Returns true if operands are not equal or not the same type.          | No                    | `x !== "5"` | `true`     |
| `>`          | Greater Than          | Returns true if the left value is greater than the right.             | Yes                   | `x > 8`     | `false`    |
| `<`          | Less Than             | Returns true if the left value is less than the right.                | Yes                   | `x < 8`     | `true`     |
| `>=`         | Greater Than or Equal | Returns true if the left value is greater than or equal to the right. | Yes                   | `x >= 5`    | `true`     |
| `<=`         | Less Than or Equal    | Returns true if the left value is less than or equal to the right.    | Yes                   | `x <= 4`    | `false`    |

### Summary:

In JavaScript, comparison operators are used to test values against each other, returning a `boolean` result. "Loose" performs type coercion, meaning it tries to convert both values to the same type (usually numbers) before comparing them. "Strict" does not convert types. If the types are different, it immediately returns `false`.
