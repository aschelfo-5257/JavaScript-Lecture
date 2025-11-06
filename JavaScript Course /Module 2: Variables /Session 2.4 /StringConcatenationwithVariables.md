# Session 2.4 - String Concatenation with Variables

String concatenation with variables entails merging string literals and variable values to form a new, singular string. In JavaScript, there are several methods for accomplishing this. The purpose of concatenation is to join two or more strings into a variable.

- **Using the `+` Operator:**

The `+` operator is the most common and straightforward method. The plus sign (+) operator, when used with strings, acts as a concatenation operator instead of an addition operator [1, 2].

    let name = "Alice";
    let age = 30;
    let message = "Hello, my name is " + name + " and I am " + age + " years old.";
    console.log(message); // Output: Hello, my name is Alice and I am 30 years old.

- **Using Template Literals (Template Strings):**

Template literals, enclosed in backticks (`` ``), offer a more readable and convenient way to embed expressions (including variables) directly within a string using the `${}` syntax.

    let name = "Bob";
    let city = "London";
    let greeting = `Welcome, ${name}! You live in ${city}.`;
    console.log(greeting); // Output: Welcome, Bob! You live in London.

- **Using the `+=` Operator:**

The `+=` operator is a shorthand for concatenating a string or variable to an existing string variable. It's equivalent to `variable = variable + value;`.

    let sentence = "This is the first part.";
    let secondPart = " And this is the second part.";
    sentence += secondPart;
    console.log(sentence); // Output: This is the first part. And this is the second part.

- Using the `concat()` method

The `concat()` method is a function of the String object that joins two or more strings.

    let greeting = "Hello";
    let name = "World";

    // Using the concat() method
    let message = greeting.concat(" ", name);

    console.log(message); // Output: "Hello World"
