# Session 1.8 - Built-in Objects

JavaScript incorporates a variety of built-in objects that form a fundamental component of the language. These objects include essential methods and properties that are integral to JavaScript's functionality and overall structure. Understanding these built-in objects is crucial for effectively utilizing the language's capabilities. The `Math` object provides a collection of mathematical constants and functions, including `Math.random()`, `Math.floor()`, and `Math.max()`, which are used for performing calculations and numerical manipulations. The primary goal is to provide standard mathematical operations and values without the need for manual implementation or external libraries.

- For example, we called the `Math.random()` method by appending the object name with the dot operator, the name of the method, and opening and closing parentheses. This method returns a random number between 0 (inclusive) and 1 (exclusive).

      console.log(Math.random()); // Prints a random number between 0 and 1

- To generate a random number. Let's say if I want to set a number between 0 and 100, we could multiply this result by `100`, like so:

      console.log(Math.random() * 100); // Prints a random number between 0 and 100

- As you run the code, it will evaluate to a random decimal.

- For another example, we can use a method called `Math.floor()`, which takes a decimal number and rounds it down to the nearest whole number. The result of this method should look like this:

      console.log(Math.floor(Math.random() * 100)); // Prints a random whole number between 0 and 100

- It will evaluate to a random whole number instead of a decimal.

- A `Math.max()` is a static method that returns the largest of zero or more numbers. It finds a maximum value among the provided numbers and returns the largest number from the arguments passed to it.

      console.log(Math.max(1, 5, 2, 8)); // Output: 8
      console.log(Math.max(10, 3, 7, 1)); // Output: 10
      console.log(Math.max(-5, -2, -10)); // Output: -2

Note that in case the method returns different values in certain scenarios:

      console.log(Math.max()); // Output: -Infinity
      
- If you run a code with no arguments provided, it returns `-Infinity`.

      console.log(Math.max("hello", 5, 10)); // Output: NaN
      
- If you run a code with any arguments that cannot be converted to a number, it returns `NaN` (Not a number).

:bulb: The primary purpose of `console.log()` is to assist developers in debugging their code by displaying messages and variable values in the browser's console or terminal. It functions as a mathematical tool that performs calculations or operations. The `Math.random()` function in JavaScript is a built-in method that generates a pseudo-random floating-point number within the range greater than or equal to 0 (inclusive) and less than 1 (exclusive). Consequently, the generated number may be 0, but it will never be 1. The `Math.floor()` method, when used within `console.log()`, outputs the largest integer less than or equal to the provided argument, effectively rounding numbers down to the nearest whole number. Additionally, the `Math.max()` function is employed to determine the maximum value among a set of zero or more numbers. When utilized with `console.log()`, it displays the result of this operation in the browser's developer console or Node.js terminal.

### Summary:

The text discusses how built-in objects, specifically the `Math` object, can be understood through demonstration of its methods and their return values. It highlights the benefit of testing these methods in isolation to observe their behavior without integration into a larger application.
