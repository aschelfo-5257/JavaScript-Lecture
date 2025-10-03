# Lesson 1.4 - Arithmetic Operators

Arithmetic operators can be utilized to perform data. The fundamental takes numerical operands (literals or variables) and returns a single numerical value. These include the following operators and their corresponding symbols: :telescope:

**Addition (+):**
- Adds two numbers together.

      console.log(5 + 3); // Output: 8

**Subtraction (-):**
- Subtracts the second number from the first.

      console.log(10 - 4); // Output: 6

**Multiplication (*):**
- Multiplies two numbers.

      console.log(2 * 6); // Output: 12

**Division (/):**
- Divides the first number by the second.

      console.log(15 / 3); // Output: 5

**Remainder (%):**
- Returns the remainder of a division operation.

      console.log(10 % 3); // Output: 1 (10 divided by 3 is 3 with a remainder of 1)

**Exponentiation (': ')**
- Raises the first number to the power of the second number.

      console.log(2 ** 3); // Output: 8 (2 * 2 * 2)

:bulb: Note that when we `console.log()`, the computer evaluates the expression inside the parentheses and prints the result to the console. Let's say if we want to print characters such as `14 + 6 / 6` we could wrap them a quotes and print as a string.

The remainder operator, sometimes called modulo, returns the number that remains after the right-hand number is divided by the left-hand as many times as it can evenly: 
- `10 % 5`: 10 divided by 5 is 2 with a remainder of 0. So, 10 mod 5 = 0.
- `7 % 5`: 7 divided by 5 is 1 with a remainder of 2. So, 7 mod 5 = 2.

**Assignment operators:**

Assignment operators provide a shortcut for performing an operation and assigning the result to a variable. Here are the tables to follow:

|  Operator   |  Equivalent expression  |  console.log()       |
|-------------|-------------------------|----------------------|
|     +=      |        a = a + b        | console.log(a + b);  |
|     -=      |        a = a - b        | console.log(a - b);  |
|     *=      |        a = a * b        | console.log(a * b);  |
|     /=      |        a = a / b        | console.log(a / b);  |
|     %=      |        a = a % b        | console.log(a % b);  |
|     **=     |        a = a ** b       | console.log(a ** b); |

### Summary:

To perform and display arithmetic operations in JavaScript using `console.log();`. It highlights that these operations depend on the data type of operands and suggests testing them in a browser's developer console or a Node.js environment.
