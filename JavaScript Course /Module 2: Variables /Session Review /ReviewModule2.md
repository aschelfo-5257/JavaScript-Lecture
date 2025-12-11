# Module 2 Review:

### **Variable Rules:**
- `let` allows reassignment of new values in a new block.
- `const` acquire to initialization because variables cannot be reassigned.
- `var` is accessible throughout the entire outside of the block function and can be redeclared and reassigned.
- Both `let` and `const` are safer choices in modern JavaScript to prevent redeclaration.

### **Mathematical Assignment Operators:**
- Mathematical assignment operators provide a shorthand for commonly used variables to calculate the operand. We recall assignment operators:
- Addition assignment: `+=`
- Subtraction assignment: `-=`
- Multiplication assignment: `*=`
- Division assignment: `/=`
- Remainder assignment: `%=`
- Exponentiation assignment: `**=`
- Remember, writing out the definition of `variable = variable op value`.

### **The Increment and Decrement Operator:**
- The increment increases (`++`) of a numeric `variable++` is equivalent to `+= x`. Prefix is (`++variable` or `--variable`).
- The decrement decreases (`--`) of a numeric `variable--` is equivalent to `-= x`. Postfix is (`variable++` or `variable--`).
- An `i++` (post-increment) and `i--` (post-decrement) are easier to read expressions.

### **String Concatenation with Variables:**
- A plus sign (`+`) operator is a concatenation of common methods

      let greeting = "Hello";
      let name = "World";
      let message = greeting + " " + name;

- Template literals (`` ` ``) are more efficient than single or double quotes

      let greeting = "Hello";
      let name = "World";
      let message = `${greeting} ${name}`;

- An `concat()` method is a function that acquires two or more strings

      let greeting = "Hello";
      let name = "World";
      let message = greeting.concat(" ", name);

### **String Interpolation:**
- Similar to string concatenation is a fundamental method that is fully supported and more readable.

      let name = "Smith";
      let age = 25;
      let greetingConcat = "Hello, " + name + "! You are " + age + " years old.";
      console.log(name);
      console.log(age);

- A template literal is a cleaner and more expressive syntax by using backticks (`` ` ``) and `${}` with a string construction.

      let name = "Smith";
      let age = 25;
      let greetingInterpolation = `Hello, ${name}! You are ${age} years old.`;
      console.log(greetingInterpolation);

- Multiline Strings acquire the use of template literals, respecting line breaks and indentation in the source code, but must be escaped with a dollar sign and curly braces for characters from `\n`.

      let multiLineString = `
      This is a string
      that spans multiple
      lines.
      `;
      console.log(multiLineString);

### **Typeof Operators:**

- The `typeof` operator is a unary operator that may determine the environment data type of its argument. You can apply syntax with or without parentheses. There are eight `typeof` operator returns the strings.
- Undefined is `"undefined"`
- Null is `"object"`
- Boolean is `"boolean"`
- Number is `"number"`
- BigInt is `"bigint"`
- String is `"string"`
- Symbol is `"symbol"`
- Function is `"function"`
- Common quirks include any definition of the values, functions, or objects that make up a data type's operands.
