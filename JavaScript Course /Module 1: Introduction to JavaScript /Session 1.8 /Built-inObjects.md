# Session 1.8 - Built-in Objects

There are other objects built into JavaScript. At this standard serves as the fundamental part of the language includes their methods and properties. The `Math` object provides a collection of mathematical constants and functions for a following `Math.random()`, `Math.floor()`, and `Math.max()` for performing calculations and numerical manipulations. The primary goal is to provide standard mathematical operations and values without need for manual implementation or external libararies.

- For example, we called the `Math.random()` method by appending the object name with the dot operator, the name of the method, and opening and closing parenthesis. This method returns a random number between 0 (inclusive) and 1 (exclusive).

      console.log(Math.random()); // Prints a random number between 0 and 1

- To generate a random number. Let's say if I want to set a number between 0 and 100, we could multiply this result by `100`, like so:

      console.log(Math.random() * 100); // Prints a random number between 0 and 100

- As you run the code, it will evaluate to a random decimal.

- For another example, we can take a method called `Math.floor()`, which takes a decimal number and rounds it down to the nearest a `whole number`. This method whole number should look like this.

      console.log(Math.floor(Math.random() * 100)); // Prints a random whole number between 0 and 100

- It will evaluate to a random whole number instead of decimal.

- A `Math.max()` is a static method that returns the largest of zero or more numbers. It finds a maximum value among the provided numbers and returns the largest number from the arguments passed to it.

      console.log(Math.max(1, 5, 2, 8)); // Output: 8
      console.log(Math.max(10, 3, 7, 1)); // Output: 10
      console.log(Math.max(-5, -2, -10)); // Output: -2

Note that in case the method returns a different values in certain scenerios:

      console.log(Math.max()); // Output: -Infinity
      
- If you run a code with no arguments provided, it returns `-Infinity`.

      console.log(Math.max("hello", 5, 10)); // Output: NaN
      
- If you run a code with any arguments and cannot be converted to the number, it returns `NaN` (Not a number).

:bulb: The primary purpose of `console.log()` is to help developers debug their code and displaying messages and variable values in the browser's console or terminal. It is a mathematical tool that allows to perform a calculation works a operation. A `Math.random()` is a built-in JavaScript function that generates a pseudo-random floating-point number. The range number generated will always be greater than or equal to 0 (inclusive) and strictly less than 1 (exclusive). This means you could get 0, but you will never get 1. The `Math.floor()` method in JavaScript, when used within console.log(), will output the largest integer less than or equal to the number provided as its argument. It effectively rounds a number down to the nearest `whole number`. The `Math.max()` is used to find the largest value among a set of zero or more numbers. When used with `console.log()`, it will print the result of this operation to the browser's developer console or Node.js terminal.

### Summary:

This usually helps built-in objects by demonstrated how the `Math` object methods work and what values they return. It provides a quick way to test and observe behavior of methods without needing to integrate them into a larger application.
