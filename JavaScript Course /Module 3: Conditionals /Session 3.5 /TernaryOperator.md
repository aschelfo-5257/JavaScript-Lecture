# Session 3.5 - Ternary Operator

In a session, time was dedicated to the use of `if...else` statements. Additionally, JavaScript's ternary operator is a well-known syntax. This operator accepts three operands and a condition, enabling the execution of one expression if the condition is `true` and another expression if the condition is `false`.

### Syntax:

The syntax for the ternary operator is as follows:

- `condition`: An expression that evaluates to a true or false (truthy or falsy) value.

- `?`: The question mark separates the condition from the true expression.

- `expressionIfTrue`: The value or expression returned if the `condition` is `true`.

- `:`: The colon separates the true and false expressions.

- `expressionIfFalse`: The value or expression returned if the `condition` is `false`.

      condition ? expressionIfTrue : expressionIfFalse;

Assigning a value to a variable based on a simple condition is the most common previous scenario.

    let age = 21;
    let message;
    
    if (age >= 18) {
      message = "You are an adult.";
    } else {
      message = "You are a minor.";
    }
    
    console.log(message);
    // Output: You are an adult.

At that point, the use case is a concise way of executing conditional expressions.

    let age = 21;
    
    const message = (age >= 18) ? "You are an adult." : "You are a minor.";
    
    console.log(message);
    // Output: You are an adult.

It allows quick assignment of values based on a condition without extra syntax overhead.

### Chaining Pattern:

To bond multiple ternary operators, use a pattern like an `?` and `:` structure. By arranging the chain vertically, you may preserve readability while keeping the code concise.

    const ChocolateBar = 225;
    const candy = ChocolateBar >= 250 ? "High" :
                  ChocolateBar >= 100 ? "Medium" :
                  ChocolateBar >= 50 ? "Low" :
                  "Not enough chocolate!";
    console.log(candy);

A ternary operator, as compared to a standard `if` statement, is a value-returning expression. This is ideal for direct variable assignments.

**Important:** Keep these things in mind while adding multiple ternary operators. Ternaries that are tightly nested are difficult to read and understand promptly.

:bulb: It clearly conveys the writing, the decisions, and the results in line with common scenarios. This operator facilitates the reading of values that indicate whether the condition expression is true or false. Only the expression that corresponds to the outcome of the condition is evaluated; all others are ignored.

**Key Concepts:**

- **Concise:** It reduces multiple lines of if/else into a single line, making the code shorter and easier to read.

- **Ternaries:** Use ternaries to assign a result to a variable or convey it as an argument.

- **Parentheses:** When using complex conditions with other operators (like `&&` or `||`), wrap the condition in parentheses to make the logic explicit.

- **Vertical Alignment:** If you must chain, place each new condition on a new line to mimic the structure of an `else if`.

- **Simple Expressions:** Only use this for basic value assignments. If you need to execute multiple lines of code per condition, a standard `if` statement is better.

The most common and widely recognized usage scenario is to assign a value to a variable based on a single condition, for example.

**If/Else:**

    let grade;
    if (score > 90) grade = 'A';
    else if (score > 80) grade = 'B';
    else if (score > 70) grade = 'C';
    else grade = 'F';

**Nested Ternary:**

    const score = 75;
    const grade = score > 90 ? 'A'
                : score > 80 ? 'B'
                : score > 70 ? 'C'
                : 'F';


**Comparison to Standard Logic:**

The most essential tactic is to understand that an if...else is a statement (it runs a block of code), while a ternary operator is an expression (it returns a result). This table structure is simplified into the chain shown above:

| `if...else` Structure                | Chained Ternary Expression |
|--------------------------------------|----------------------------|
| `if (condition1) { return A; }`      | `condition1 ? A :`         |
| `else if (condition2) { return B; }` | `condition1 ? B :`         |
| `else { return C; }`                 | `C;`                       |

### Summary:

The key strategies for using ternary operators in JavaScript involve balancing code conciseness with readability. While they can shorten logic effectively, misuse may lead to unreadable code that is hard to debug and understand. The ternary operator serves as a concise method for performing conditional expressions in JavaScript.
