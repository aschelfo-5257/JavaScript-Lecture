# Session 3.6 - The Switch Keyword

The `switch` statement is a control flow structure that is used to perform different actions based on different conditions. It is a control statement that evaluates an expression and executes code blocks associated with matching case labels. Use a switch statement to manage multiple conditional choices cleanly without relying on nested `if...else` blocks.

Here is the general syntax of a `switch` statement in JavaScript:

**Syntax:**

    switch (expression) {
      case value1:
        // Code to execute when expression === value1
        break;
      case value2:
        // Code to execute when expression === value2
        break;
      // ... more cases ...
      default:
        // Code to execute if none of the cases match
        break;
    }

- **`switch`:** Evaluates the given expression once and executes the matching case block.

- **`case`:** Defines a possible value to compare with the switch expression; if it matches, the following code block runs.

- **`break`:** Stops further execution of other cases inside the switch and exits the switch block. Without it, the computer will keep executing every case below it, even if they don't match.

- **`default`:** A fallback that runs if none of the case values match the expression.

Here is an example of `GroceryItem` when trying to buy a fruit in each case.

    let GroceryItem = 'Apple';
    
    switch(GroceryItem) {
      case 'Apple':
        console.log('I buy the Apple!');
        break;
      case 'Orange':
        console.log('I buy the Orange!');
        break;
      case 'Strawberry':
        console.log('I buy the Strawberry!');
        break;
      default:
        console.log('No fruit available');
        break;
    }

The most interesting and unique fact about the `switch` statement code is a behavior called "Fall-Through".

- If you omit the `break` keyword, the execution doesn't stop after the match.

- The computer executes the matching case, then executes every single case underneath it automatically.

- It ignores the conditions of those lower cases entirely.

### Switch of Comparison Operators:

If you want to use comparison operators (like `<`, `>`, `<=`, `>=`, or explicit strict equality `===`) inside your cases, you have to use a specific design pattern: passing true as the switch expression.

For example, if it evaluates the first case expression: `score >= 90`. Since `85 >= 90` is false, it moves on.

    let score = 85;
  
    switch (true) {
      case (score >= 90):
        console.log('You get an A!');
        break;
      case (score >= 80 === true): // Explicit strict equality check
        console.log('You get a B!');
        break;
      default:
        console.log('Keep trying!');
    }

It evaluates the next case: `(score >= 80 === true)`. This evaluates to true.

Thus, `true === true`, this case block runs and logs 'You get a B!'.

:bulb: In a switch statement, the expression inside the switch(expression) is evaluated only once. The expression compares a single value against various static constants. If a match is found, the code in that case block is executed until a break statement is encountered or the switch block ends.

**Key Concepts:**

- **Linear Search:** An engine sequentially processes every condition leading up to your match, increasing lookup time linearly.

- **Instant Lookup:** When a compiler processes a `switch` statement, it builds a Jump Table (a lookup array in memory). Instead of executing sequentially, it maps your variable directly to its correct memory location.

- **Speed Rate:** A switch statement is often faster than a long `if...else` chain because of how compilers and interpreters optimize the code behind the scenes.

Rather than a flaw, fall-through is an intentional feature used to map multiple inputs to a single output block.

    let response = 'yes';

    switch(response) {
      case 'yes':
      case 'y':
      case 'agree':
        console.log('User said yes!'); // Runs for all three cases
        break;
    }

Here, both 'yes' and 'y' cases execute the same code because there’s no `break` between them! This can be a neat shortcut, but forgetting `break` accidentally can cause bugs.

**Note:** The switch statement always uses strict equality (`===`) when matching expressions to cases.

### Summary:

A `switch` statement is cleaner and more readable than multiple `if...else` if statements when checking one variable against many values. It helps select one of many code blocks to execute, allowing for safe pre-optimization by the compiler, as all comparisons are made against the same variable.

For more information and interactive examples, refer to https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch


