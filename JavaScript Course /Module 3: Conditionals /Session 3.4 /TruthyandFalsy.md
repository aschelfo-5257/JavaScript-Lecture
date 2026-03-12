# Session 3.4 - Truthy and Falsy

In the previous session, we saw the values `truthy` and `falsy` in JavaScript. It determines how non-boolean values behave in a Boolean context, such as conditional statements (`if`,`else`) and logical operations (`&&`,`||`,`!`). The objective is to build more concise and expressive code by letting developers check the "existence" or "validity" of a variable without explicit comparisons. :gear:

### Truthy Values:

A `truthy` is a value that is considered `true` when encountered in the Boolean context. All values in JavaScript are truthy unless they are explicitly defined as falsy. Common truthy values include:

- Any non-zero number (e.g., `42`, `-1`, `3.14`).

- Any non-empty string (e.g., `"hello"`, `"false"`, `"0"`).

- Objects (e.g., `{}`, a non-empty object).

- Arrays (e.g., `[]`, a non-empty object).

- Functions

- Symbols

If these are used in a condition, the code block will execute.

    if (" ") {
      // This WILL run because a string with a space is truthy
    }
      
    if ([]) {
      // This WILL run because empty arrays are truthy
    }

Let's assume I intend to set `ScoreCount`. If the truthy is true, it executes a code block. Otherwise, the score does not exist.

    let ScoreCount = 10;

    if (ScoreCount) {
      console.log("You have the score!");
    } else {
      console.log('You need to improve score!'); // This does not exist.
    }

### Falsy Values:

There are only a few values in JavaScript that are considered `falsy`. Memorizing these is the easiest way to understand the concept, as every other value is truthy.

- `false` (the keyword)

- `0`, `-0`, and `0n` (BigInt zero)

- `""`, `''`, and ` ` (Empty strings)

- `null`

- `undefined`

- `NaN` (Not-a-Number)

If any of these are the condition of an if statement, the block will not execute.

    if (0) { 
      // This will NOT run because 0 is falsy
    }
    
    const name = "";
    if (name) {
      // This will NOT run because empty strings are falsy
    }

Suppose I want to log in to a user account. If the login is falsy, you must log in. Otherwise, the user may access.

    const username = "";
    if (username) {
      // This block is skipped because "" is falsy.
      console.log("User is logged in.");
    } else {
      console.log("Please log in."); // This block executes.
    }

### Truthy and Falsy Assignment:

Let us recall logical operators. We utilize a short-circuit evaluation, which implies that instead of just returning `true` or `false`, they return the value of one of the operands based on its truthiness assignment.

**OR (`||`):**

The OR operator returns the first truthy value it encounters. If all values are falsy, it returns the last value.

    const name = "" || "Guest"; 
    // Result: "Guest" (because "" is falsy)
    
    const points = 100 || 0;
    // Result: 100 (because 100 is truthy)

**AND (`&&`):**

The AND operator returns the first falsy value it encounters. If all values are truthy, it returns the last value.

    const user = { name: "John" };
    const result = user && user.name;
    // Result: "John" (both are truthy, returns the last one)
    
    const isLoggedIn = false && "Dashboard";
    // Result: false (returns the first falsy value immediately)

**NOT (`!`):**

The NOT operator always converts the value into a strict Boolean (`true` or `false`).

    const isNoisy = !""; // Result: true (empty string is falsy, NOT flips it)
    const isZero = !10;  // Result: false (10 is truthy, NOT flips it)

**Note:** Sometimes you only desire to see if a variable exists, and you do not need to assign any specific value. It is defined by how value behaves while evaluating a Boolean expression.

:bulb: The terms `truthy` and `falsy` relate to how non-boolean values, such as numbers, strings, or even objects, are interpreted in situations that require boolean evaluation, such as conditional expressions (e.g., if statements) or comparative analysis.

**Key Concepts:**

Any value that is not included in the list above is deemed to be true and will be evaluated as a result. This occurs in several common "gotchas," where items that appear to be null are actually true.

- **Objects & Arrays:** Even an empty object `{}` or empty array `[]` is truthy.
  
- **Non-Empty Strings:** The strings `"0"` and `"false"` are truthy because of their character elements.

- **Non-Zero Numbers:** Any number that is not equal to zero, regardless of negative numbers such as `-1`, is accurate.

- **Functions:** Any function, even an empty one such as `function(){}`, is truthy.

**Execution Patterns:**

**Short-circuiting:** The initial truthy value that the `||` operator identifies is returned.

- `const user = inputName || "Guest";` (Uses "Guest" if `inputName` is `""` or `null`)

**Guard Clauses:** An initial falsy value or the last truthy value is returned by the `&&` operator.

- `user && user.login();` (Only calls login if user is truthy)

**Explicit Conversion:** To determine the implementation of a value, utilize Boolean() or `!!`.

- `!!0` returns `false`; `!![]` returns `true`.

**Strict Equality:** To avoid unexpected results from automatic type coercion, use the strict equality operator (`===`).

- Handling `null` and `undefined`: Because they are different types, strict equality `null === undefined` is `false`, compared to loose equality where `null == undefined` is `true`.

When writing code, you can streamline your logic by leveraging these characteristics. Instead of performing explicit checks to determine if a string is empty or null, you can evaluate the string in a boolean context. For example, instead of writing code that checks if a variable `myString` is not equal to null and not equal to an empty string, you can simply use `if (myString)` to achieve the same result.

| **Data Type**  | **Truthy Examples**              | **Falsy Examples**  |
|----------------|----------------------------------|---------------------|
| **Boolean**    | true                             | false               |
| **Number**     | `1`, `-42`, `3.14`, `Infinity`   | `0`,`-0`,`NaN`      |
| **String**     | `"hello"`, `"0"`, `" "`(space)   | `""`(empty)         |
| **Object**     | `{}`, `[]`, `new Date()`         | `null`              |
| **Other**      | `Symbol()`, `10n`                | `undefined`, `0n`   |

### Summary:

The concepts of truthy and falsy describe how non-boolean values are evaluated in a boolean context. Understanding these concepts helps in writing cleaner, more concise code and improves readability by clearly indicating checks for valid, non-empty input.

For more information and interactive examples, refer to https://developer.mozilla.org/en-US/docs/Glossary/Falsy
