# Session 1.5 - String Concatenation

String concatenation serves a fundamental purpose in combining two or more strings into a single or larger string. This enables the process of various tasks by creating an append that learns from the operator's quotes `+`.

It appends to the right string and to the left string, for example:

    console.log("A" + " " + "B"); // Output: A B

This process is ensured to include a space at the end of the first string. The computer will join the strings exactly, so we must include the space between the two proper strings `' ' + ' '`. Here is, for example:

- **Front space:**

      console.log('front ' + 'space'); // Prints: 'front space'
- **Backspace:**

      console.log('back' + ' space'); // Prints: 'back space'
- **No space:**

      console.log('no' + 'space'); // Prints: 'nospace'
- **Middle space:**

      console.log('middle' + ' ' + 'space'); // Prints: 'middle space'

Just as with the arithmetic operator math, we can combine or chain our operations to obtain a final result.

:bulb: When joining strings in JavaScript, it's important to pay attention to where you place spaces, as the concatenation process won't add them automatically.

**Note:**

When using the `-` operators with strings, It does not work for string concatenation because it is exclusively defined for performing arithmetic subtraction on numerical values.

    console.log("A" - " " - "B"); // Output: NaN

It is not overloaded for string manipulation. Its sole purpose is to subtract one number from another. Strings cannot successfully convert them to numbers first, resulting in `NaN` (Not a Number).

### Summary:

This is the most straightforward method. You simply include a space character (enclosed in a single or double quotes) between the strings you are concatenating. `-` only works for arithmetic operations.
