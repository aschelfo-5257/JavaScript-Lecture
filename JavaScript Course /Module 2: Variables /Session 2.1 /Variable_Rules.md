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

- **Important Note:** Using `var` is generally considered a bad practice in modern JavaScript development. The introduction of `let` and `const` in ECMAScript 6 (ES6) provided better, more predictable alternatives that address the confusing and error-prone behaviors of `var`.


Best practices:

Prefer const by default; use let when you need to reassign. Avoid var in modern code.
Declare variables close to where they’re used.
Use clear, descriptive names.
Avoid relying on hoisting — declare before use to improve readability and prevent TDZ errors
