# Session 1.7 - Methods

In JavaScript, methods are crucial for the actions that we can perform. Remember, `data types` have access to specific methods that allow us to handle instances of the concepts. They are written in the same way as functions, but they are defined within the objects. And you will see furthermore the manipulated objects.

Suppose we can recall these methods by appending an instance with:

- a period (the dot operator)
- the name of the method
- opening and closing parentheses

Example: `'example string'.methodName()`

When we use `console.log(),` we're calling the `.log()` method on the `console` object. Here is something looks familiar syntax for real string methods in action:

    console.log('variable'.toUpperCase()); // Output: 'VARIABLE'
    console.log('variable'.toLowerCase()); // Output: 'variable'
    console.log('Data'.startsWith('D')); // Output: true 
    console.log('Example'.startsWith('F')); // Output: false

- On the <mark>first line</mark>, the `.toUpperCase()` method is called on the string instance `'variable'`. Then the result is logged to the console method for all capital letters: `'VARIABLE'`.
- On the <mark>second line</mark>, the `.toLowerCase()` method is called on the string instance `'variable'`. Then the result is logged to the console method for all lowercase letters: `'variable'`.
- On the <mark>third line</mark>, the `.startsWith('')` method is called on the string instance `'Data'`. This method is accepts the character `'D'` as an argument input in between the parenthesis. Since the string starts with the letter, then the method returns the boolean `true` output.
- On the <mark>fourth line</mark>, the `.startsWith('')` method is called on the string instance `'Example'`. This method does not accept the character `'F'` as an argument input in between the parentheses. Since the string starts with the letter, then the method returns the boolean `false` output.

:bulb: Methods are very useful that are associated with an object. They allow you to define actions or behaviors that an object can perform. Understanding the methods used to comprehend several key aspects of JavaScript, like modifying and processing the data stored within the object's properties. You can define your own methods for custom objects, enabling them to perform specific tasks relevent to your application, as long as it is a correctly named property.

### Summary

Understanding methods in JavaScript means how to make objects perform actions, how to interact with and manipulate object data, and how to utilize the rich set of functionalities provided by the language's built-in objects.
