# Session 2.6 - Typeof Operators

The `typeof` operator in JavaScript is a unary operator that helps identify the data type of its operand. It returns a string specifying the variable's type. This operator is essential in JavaScript's dynamic typing environment, enabling developers to take different actions based on the current type of the variable. Understanding how to use `typeof` effectively can enhance code flexibility and reliability.

### **Syntax:**

The syntax is straightforward and can be used with or without parentheses:

      typeof operand;

or

      typeof (operand);

### **Return Values:**

The **typeof** operator returns one of the following strings for a table:

| Type of the operand | Resulting String |
|---------------------|------------------|
| Undefined           | `"undefined"`    |
| Null                | `"object"`       |
| Boolean             | `"boolean"`      |
| Number              | `"number"`       |
| BigInt              | `"bigint"`       |
| String              | `"string"`       |
| Symbol              | `"symbol"`       |
| Function            | `"function"`     |

**Note:**

- `typeof null` returns `"object"`: This is a historical bug in JavaScript that cannot be fixed without breaking existing code. To correctly check for an object that is not null, a common check is `typeof myVar === 'object' && myVar !== null`.

- `typeof NaN` returns `"number"`: `NaN` stands for "Not a Number," but it is technically a special kind of numeric value. To correctly check if a value is actually `NaN`, use the built-in global `isNaN()` function or the more reliable `Number.isNaN()` method.

- `typeof` on a variable that has not been declared will not throw a `ReferenceError`, but will safely return the string `"undefined"`. This is useful for checking if a variable exists in a given scope.

When using the `typeof` operator in JavaScript, you must be mindful of several "gotchas" or non-intuitive behaviors to ensure your code functions correctly.

**Here is a list of examples of usage of the code:**

    console.log(typeof "hello");      // "string"
    console.log(typeof 123);          // "number"
    console.log(typeof true);         // "boolean"
    console.log(typeof undefined);    // "undefined"
    console.log(typeof Symbol('id')); // "symbol"
    console.log(typeof 123n);         // "bigint"
    console.log(typeof null);         // "object" (quirk)
    console.log(typeof {});           // "object"
    console.log(typeof function() {}); // "function"

:bulb: The `typeof` operator is a useful tool in JavaScript for basic type checking in a dynamically typed environment. Key tips involve understanding its return values and common quirks. The operand can be any variable, function, or object whose type you want to find out using the `typeof` operator.

### **Key Tips and Quirks: :key:**

**Returns a string:** `typeof` always returns a string, such as `"number"`, `"string"`, `"boolean"`, `"undefined"`, `"object"`, `"bigint"`, or `"symbol"`.

**Null:** `typeof null` is `"object"`: This is a well-known quirk in JavaScript, so you cannot use `typeof` alone to reliably check for `null`. Use an explicit check: `if (value === null)`.

**Functions return:** `"function"`: Unlike other objects, functions are returned as `"function"`, not `"object"`.

**Handles undeclared variables safely:** `typeof` will return `"undefined"` for undeclared variables without throwing an error, which is useful for checking if something has been declared.

**Use with `let` and `const`:** Avoid using `typeof` on `let` or `const` variables within the same block before they are declared, as this will cause a `ReferenceError`.

**Different behavior with and without parentheses:** `typeof` without parentheses evaluates the type of the value immediately following it. Using parentheses `(typeof expression)` evaluates the type of the entire expression inside the parentheses.

**Type guards:** `typeof` is essential for creating type guards, especially when dealing with union types or unknown values in functions.

### Summary:

The `typeof` operator in JavaScript is a unary operator that returns a string indicating the data type of its operand. It can be applied to variables, literals, or expressions, making it useful for debugging and validating data types.

**References:** For detailed documentation, refer to the MDN Web Docs on Typeof Operators:

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference

