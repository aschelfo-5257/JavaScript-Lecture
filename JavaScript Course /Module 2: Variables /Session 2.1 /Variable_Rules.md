# Session 2.1 - Variable Rules

The variables in JavaScript are used to declare variables. Introduced in ES6 are `let` and `const` offer more predictable variable handling in the modern standard. While `var` is the original and older way of declaring variables. To master variables in JavaScript, you need to understand the different ways to declare them, how their accessibility changes based on where they are created, and the various types of data they can hold. There are a few general variable rules to follow: :writing_hand:

### `let`:

- **Scope:** `let` declarations are block-scoped, meaning they are only accessible within the nearest set of curly braces.
- **Reassignment:** Variables declared with `let` can be reassigned to new values.
- **Re-declaration:** Variables declared with `let` cannot be redeclared within the same block scope. Attempting to do so will result in a `SyntaxError`.
- **Hoisting:** `let` declarations are hoisted to the top of their block, but they are not initialized. They exist in a "Temporal Dead Zone" until their declaration is encountered, and attempting to access them before this point will result in a `ReferenceError`.

  Let's say if I want to assigned `let` <mark>meal</mark> and run the console <mark>pizza</mark>.

      let meal = 'Pizza';
      console.log(meal); // Output: Pizza

  If I want to add a new value, then I add to the new console <mark>hamburger</mark>.

      meal = 'Hamburger';
      console.log(meal); // Output: Hamburger

  It allows to reassign the new value.
  
### `const`:

- **Scope:** `const` is block-scoped, similar to `let`.
- **Reassignment:** `const` variables cannot be reassigned after their initial assignment. They must be initialized at the time of declaration. Attempting to reassign a `const` variable will result in a `TypeError`.
- **Re-declaration:** `const` variables cannot be re-declared within the same scope.
- **Hoisting:** `const` declarations are hoisted to the top of their block scope but are in a "temporal dead zone" until the declaration is processed, similar to `let`.
- **Initialization:** A `const` declaration is required to have an initializer because it's impossible to assign a value to it later. The keyword const establishes a "constant" or "read-only" binding to a value.

  Let's say if I want to assigned `const` <mark>bookName</mark> and run the console <mark>The MockingBird 1948</mark>.

      const bookName = 'The MockingBird 1948';
      console.log(bookName); // Output: The MockingBird 1948
      // (This variable is only to run at once.)

  If I tried to add a new value, then the console <mark>William Snakespeare 1978</mark> is constant variable to run.

      bookName = 'William Snakespeare 1978'
      console.log(bookName); // Output: William Snakespeare 1978
      // (This would cause a TypeError: Assignment to constant variable.)

  It does not allow to reassign the new value.

### `var`:

- **Scope:** `var` is function-scoped. This means a variable declared with `var` is accessible throughout the entire function in which it is declared, regardless of block-level structures like `if` statements or loops. If declared outside of any function, it becomes a global variable.
- **Reassignment:** `var` variables can be reassigned to new values.
- **Re-declaration:** `var` variables can be re-declared within the same scope without error.
- **Hoisting:** `var` declarations are hoisted to the top of their function or global scope and initialized with undefined. This allows them to be accessed before their declaration in the code, though their value will be `undefined` until the actual declaration is processed.

Let's say if I assigned `var`. <mark>globalVar</mark> and run the console <mark>Global</mark>.

    var globalVar = 'Global';
    console.log(globalVar); // Output: Global

It allows for redeclared and reassign anytime with a new value.

- **Important Note:** Using `var` is generally considered a bad practice in modern JavaScript development. The introduction of `let` and `const` in ECMAScript 6 (ES6) provided better, more predictable alternatives that address the confusing and error-prone behaviors of `var`.

:bulb: In JavaScript, `var`, `let`, and `const` all declare variables, but they differ in their scope, hoisting behavior, and rules for reassignment and redeclaration. For modern JavaScript development, `let` and `const` are preferred over `var`. Here are the best practices:

- Prefer `const` by default; use `let` when you need to reassign. Avoid `var` in modern code. :heavy_check_mark:
- Declare variables close to where they’re used. :heavy_check_mark:
- Use clear, descriptive names. :heavy_check_mark:
- Avoid relying on hoisting — declare before use to improve readability and prevent TDZ errors. :heavy_check_mark:

**Why should you use `let` and `const`?**

- Both `let` and `const` are block-scoped, meaning they are confined to the block of code (the nearest {} curly braces) where they are declared. This makes code more predictable and easier to reason about, as variables won't "leak" out of the block they are used in.
- Using `const` for variables that should not change signals your intent to other developers and prevents accidental reassignment.
- Many modern JavaScript tools and linters, like ESLint, can be configured to disallow the use of `var` and enforce the use of `let` and `const`, aligning your codebase with modern conventions.

Here are the summary differences in a table: :mag:

Feature            |              `let`                |              `const`              |                `var`                   |
-------------------|-----------------------------------|-----------------------------------|----------------------------------------|
**Scope**          |              Block                |               Block               |            Function/Global             |
**Hoisting**       | Hoisted but not initialized (TDZ) | Hoisted but not initialized (TDZ) | Hoisted and initialized to `undefined` |
**Reassignment**   |               Yes                 |                No                 |                 Yes                    |
**Redeclaration**  |               No                  |                No                 |                 Yes                    |
**Initialization** |           Not required            |              Required             |             Not required               |

### Summary:

Any performance difference is so small that it is likely to be imperceptible in most applications and is not a valid reason to choose one over the other. `let` Common cases include loop counters or variables whose values are calculated incrementally. `const` This communicates intent and makes your code safer and more readable. `var` Its function-level scoping and permissive reassignment can lead to bugs that `let` and `const` prevent.
