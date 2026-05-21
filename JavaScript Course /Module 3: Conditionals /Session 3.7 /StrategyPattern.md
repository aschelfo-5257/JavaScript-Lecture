# Session 3.7 - Strategy Pattern

We often explored the built-in capabilities of JavaScript. A conditional strategy refers to the design or pattern you use to run different blocks of code based on different inputs or truthy/falsy values. Selecting the appropriate strategy ensures that the code remains clear, efficient, and scalable. :star2:

- **`if...else`:** The most standard approach for checking specific, sequential conditions. It is best suited for boolean evaluations or range checking (e.g., `if (score >= 90)`).

- **`switch` statement:** Best suited for evaluating a single variable against multiple strict matching values (e.g., matching strings or integers). It offers better readability than massive `if...else` chains.

- **Ternary Operator (`? :`):** An expression-based shorthand ideal for inline, single-line variable assignments or quick binary decisions.

- **Short-Circuit Evaluation (`&&` and `||`):** Leverages logical operators to execute expressions conditionally. For example, `isLoggedIn && showDashboard()` quickly checks a state before running a function.

As applications grow, nested `if else` chains often turn into a "code smell" known as arrow anti-patterns or deeply nested loops.

Its primary purpose is to allow a client to choose which "<mark>strategy</mark>" algorithm or behavior to use without changing the code that consumes it.

### Example #1 - The Lookup Table:

Instead of matching a string through a series of `if/else` or `switch` blocks, map keys to functions or values within a standard JavaScript object literal.

    const userRole = 'admin';

    const roleActions = {
          admin: () => console.log("Granted All Access"),
          editor: () => console.log("Granted Write Access"),
          guest: () => console.log("Granted Read Access")
      };
          
      // Execution is highly readable and runs in O(1) time
      const currentAction = roleActions[userRole] || roleActions.guest;
      currentAction();

It’s easier to add new roles or strategies by adding new functions in roleActions.

### Example #2 - The Strategy Design Pattern:

A software design strategy where you encapsulate interchangeable blocks of logic (strategies) inside independent functions or classes. The correct behavior is selected dynamically at runtime without relying on rigid control flows.

    const shippingStrategies = {
      FedEx: (weight) => weight * 2.5,
      UPS: (weight) => weight * 2.0,
      LocalPost: (weight) => weight * 1.2,
    };
    
    const selectedStrategy = 'FedEx';
    const weight = 10; // 10 kg
    const cost = shippingStrategies[selectedStrategy](weight);
    
    console.log(`Cost for ${selectedStrategy} shipping: $${cost}`); 
    // Output: Cost for FedEx shipping: $25
    // Output: Cost for UPS shipping: $20
    // Output: Cost for LocalPost shipping: $12

FedEx, UPS, and LocalPost have different strategies for calculating shipping costs based on weight.

### Example #3 - Guard Clauses:

This strategy prioritizes checking for invalid states or exceptional conditions at the very top of a function. If a condition is met, the function exits immediately, eliminating the need to wrap the rest of the function in an expansive, nested else block.

    function calculateDiscount(userType, price) {
      if (userType === 'VIP') return price * 0.8;
      if (userType === 'Premium') return price * 0.9;
      if (userType === 'Regular') return price * 0.95;
    
      return price; // default case
    }
    
    console.log(calculateDiscount('VIP', 200));
    console.log(calculateDiscount('Premium', 200));
    console.log(calculateDiscount('Regular', 200));

This makes the function cleaner and easier to understand at a glance. If none of the conditions match, the function falls back to returning the original price.

If you check multiple dependent conditions before executing code logic. This will end up finding or creating nested code through a phenomenon known as "The Arrow Anti-Pattern" or "Pyramid of Doom."

:bulb: Think of it as a way to create a family of interchangeable behaviors that a program can swap out at runtime. It helps to avoid messy `if...else` or `switch` blocks when you have multiple ways to perform the same task.

**Key Concepts:**

- **Strategy Interface**: A common blueprint (often just a shared method name in JS) that all concrete strategies must follow.

- **Concrete Strategies**: The interchangeable algorithms or behaviors.

- **Context**: The object that uses a strategy. It doesn't know how the strategy works; it just calls the strategy's method.

**Why do we use a strategy?**

- You can add new behaviors (new strategies) without changing the existing code that uses them. :heavy_check_mark:
- You can switch between different logics (like sorting algorithms or payment methods) dynamically based on user input or environment. :heavy_check_mark:
- It eliminates "conditional-infested" code by encapsulating logic into separate objects or functions. :heavy_check_mark:

Picking the appropriate condition method in JavaScript directly impacts your application's maintainability, performance, and scalability. JavaScript offers several ways to handle logic branchings (if/else, switch statements, guard clauses, object lookups, and ternary operators), and choosing the wrong one creates a "code smell" that slows down development.

### Summary:

The Strategy Design Pattern is a behavioral blueprint that extracts a family of algorithms into separate, interchangeable modules. It allows your application to dynamically swap business logic at runtime without modifying the core system.

For more information and interactive examples, refer to https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference
