### 1. Programming Basics questions

#### 1.1. Data Basics

- **What are the differences between objects, arrays, and primitives in JavaScript? How are they used in programming?**
  - Objects: collections of key-value pairs
  - Arrays: ordered collections of values
  - Primitives: basic data types in JavaScript, including numbers, strings, booleans, null, and undefined. Primitives usually store a single piece of information, while arrays and objects store groups of information

- **How would you access the value of a specific key in an object?**
  - With the name of the object and the key (`objectName.keyName` or `objectName[KeyName]`)

- **Explain the concept of key-value pairs in objects and how they differ from indexed elements in arrays.**
  - Key-value pairs are similar to variables, just grouped together. While you access a value of an array with it’s index, you use the key in an object (`objectName[keyName]` vs `arrayName[i]`)

- **Describe a scenario where you would choose to use an object instead of an array, or vice versa, and explain your reasoning.**
  - When for example I handle the data of various people, I would use an object to store a given person's details and an array to store the objects. Objects separate the data better and make it easier to handle differences while arrays are better for similar data.

- **How can you retrieve the first and last items of an array?**
  - `arrayName[0]` and `arrayName[arrayName.length-1]`

- **Identify the five most commonly used primitive types in JavaScript, and provide examples demonstrating when and how to use them?**
  - Number: storing numbers used in calculations
  - String: storing text or a middle step (`split()`, `html`, etc)
  - Boolean: true or false (for example for an if statement)
  - Null: intentionally missing data
  - Undefined: missing data

#### 1.2. Algorithm Basics

- **Provide examples of assignment operators in JavaScript.**
  - `let x = 5;` // assigns the value 5 to variable x
  - `let y = 10;` // assigns the value 10 to variable y
  - `x += 3;` // adds 3 to the current value of x
  - `y -= 5;` // subtracts 5 from the current value of y

- **Name some of the arithmetic operators in JavaScript.**
  - Addition (+): Adds two values.
  - Subtraction (-): Subtracts the right operand from the left operand.
  - Multiplication (*): Multiplies two values.
  - Division (/): Divides the left operand by the right operand.
  - Modulus (%): Returns the remainder of the division.
  - Increment (++): Increases the value of a variable by 1.
  - Decrement (--): Decreases the value of a variable by 1.

- **What are the different comparison operators in JavaScript?**
  - Equality (== or ===): Checks if two values are equal.
  - Inequality (!= or !==): Checks if two values are not equal.
  - Greater than (>), Less than (<), Greater than or equal to (>=), Less than or equal to (<=).

- **Name a few logical operators used in JavaScript.**
  - Logical AND (&&): Returns true if both operands are true.
  - Logical OR (||): Returns true if at least one operand is true.
  - Logical NOT (!): Returns true if the operand is false, and false if the operand is true.

- **Explain the differences between a for loop, for of loop, and for in loop in JavaScript.**
  - The for loop is the universal one, while the for-of and for-in loops are specifically for iterating through an array or object.

- **If you can't use any built-in functions or methods, how would you calculate the average of values in an array?**
  - By googling built-in functions and methods, then adding together every value of the array, then dividing by the number of values.
# 1.3. Function Basics

- **What is a function in JavaScript? Explain its purpose and how it is used in programming.**
  - A function in JavaScript is a reusable block of code that performs a specific task. Functions help modularize code, making it more organized, readable, and easier to maintain. They are used to encapsulate logic, promote code reusability, and enable the creation of more structured programs.

- **Describe the different syntax elements that make up a JavaScript function.**
  - Function keyword: Indicates the start of a function declaration.
  - Function name: A user-defined name for the function.
  - Parameters: Variables that act as placeholders for values passed to the function.
  - Function body: The block of code enclosed in curly braces {} that defines what the function does.
  - Return statement: Specifies the value the function should return (optional).

- **How do you pass arguments to a function? Explain the concept of parameter passing and provide an example.**
  - Arguments are values passed to a function when it is called. Parameters are variables used to receive these values inside the function.
    ```javascript
    function greet(name) {
      console.log("Hello, " + name + "!");
    }
    greet("Alice"); // Output: Hello, Alice!
    ```

- **What is the difference between function expressions and function declarations? Provide examples of each.**
  - The key difference is the way they are defined. Function declarations are hoisted (can be called before they are defined), while function expressions are not.

- **Explain what a callback function is in JavaScript.**
  - A callback function is a function that is passed as an argument to another function and is executed after the completion of some operation. Callbacks are commonly used in asynchronous operations, event handling, and to manage the flow of code.

- **What is the scope of variables in JavaScript functions? Explain the difference between local and global variables.**
  - Scope – where is the variable accessible
    - Local Variables: Variables declared within a function have local scope. They are only accessible within that function (within the {}).
    - Global Variables: Variables declared outside any function have global scope. They are accessible throughout the entire program.

# 1.4. Built-in Features

- **What are some commonly used built-in functions or methods in JavaScript for working with strings? Provide examples and explain their usage.**
  - `length`: Returns the length of a string.
    ```javascript
    const str = "Hello, World!";
    console.log(str.length) // Output: 13
    ```
  - `charAt(index)`: Returns the character at the specified index.
    ```javascript
    const str = "JavaScript";
    console.log(str.charAt(2)); // Output: v
    ```
  - `toUpperCase()`: Converts a string to uppercase.
    ```javascript
    const lowercase = "hello";
    const uppercase = lowercase.toUpperCase(); 
    console.log(uppercase); // Output: HELLO
    ```
  - `toLowerCase()`: Converts a string to lowercase.
    ```javascript
    const uppercase = "HELLO";
    const lowercase = uppercase.toLowerCase(); 
    console.log(lowercase); // Output: hello 
    ```
  - `indexOf(substring)`: Returns the index of the first occurrence of a substring, or -1 if not found.
    ```javascript
    const sentence = "This is a sample sentence.";
    console.log(sentence.indexOf("sample")); // Output: 10
    ```

- **Name at least five built-in functions or methods in JavaScript for manipulating arrays.**
  - `push()`, `slice()`, `reverse()`, `forEach()`, `filter()`

- **Describe how each function/method works and provide an example for each.**
  - `push()`: Adds one or more elements to the end of an array.
    ```javascript
    const fruits = ['apple', 'orange']; 
    fruits.push('banana', 'grape'); // fruits is now ['apple', 'orange', 'banana', 'grape']
    ```
  - `slice(start, end)`: Returns a shallow copy of a portion of an array between the specified start and end indices.
    ```javascript
    const numbers = [1, 2, 3, 4, 5];
    const slicedNumbers = numbers.slice(2, 4); // slicedNumbers is [3, 4], 
    ```
  - `reverse()`: Reverses the order of elements of an array in place.
    ```javascript
    const numbers = [1, 2, 3, 4, 5]; 
    numbers.reverse(); // numbers is now [5, 4, 3, 2, 1]
    ```
  - `forEach()`: Executes the argument function for each element of the array.
    ```javascript
    const numbers = [1, 2, 3, 4, 5]; 
    const biggerNumbers = numbers.forEach(x => x + 1);
    // biggerNumbers is now [2, 3, 4, 5, 6]
    ```

- **How can you use built-in functions or methods in JavaScript to perform mathematical operations? Give examples of commonly used functions or methods for mathematical calculations.**
  - `Math.sqrt(x)`: Returns the square root of a number.
  - `Math.round(x)`: Rounds a number to the nearest integer.
  - `Math.floor(x)`: Rounds a number down to the nearest integer.
  - `Math.ceil(x)`: Rounds a number up to the nearest integer.
  - `Math.random()`: Returns a random number between 0 (inclusive) and 1 (exclusive).
    ```javascript
    const num = 25.75;
    console.log(Math.sqrt(num)); // Output: 5.074
    console.log(Math.round(num)); // Output: 2
    console.log(Math.floor(num)); // Output: 25
    console.log(Math.ceil(num)); // Output: 26
    console.log(Math.random()); // Output: a random number between 0 and 1
    ```

- **What are some built-in functions or methods in JavaScript for manipulating numbers? Describe their functionality and give examples of how they can be used.**
  - `Math.round(x)`: Rounds a number to the nearest integer.
    ```javascript
    const num = 3.6; 
    const roundedNum = Math.round(num); // roundedNum is 4
    ```
  - `Math.floor(x)`: Rounds a number down to the nearest integer.
    ```javascript
    const num = 3.9; 
    const flooredNum = Math.floor(num); // flooredNum is 3
    ```
  - `Math.ceil(x)`: Rounds a number up to the nearest integer.
    ```javascript
    const num = 3.1; 
    const ceiledNum = Math.ceil(num); // ceiledNum is 4
    ```

- **Discuss the differences between for loops and the forEach method in JavaScript.**
  - Similar to for-of and for-in, forEach() is a specialized tool for iterating an array and calling a function with the current element as an argument. For its intended purpose, it’s way simpler and shorter, and the resulting code is
# 1.5. File Basics

- **What distinguishes JavaScript data structures from JSON data structures?**
  - JSON is a serialization format used for data interchange and storage, whereas JavaScript data structures refer to the in-memory organization of data during program execution.
  - JSON is a subset of JavaScript object literal notation. While JavaScript data structures can include functions and are more dynamic, JSON is a strict data format and does not support functions or other JavaScript-specific features.

- **How would you create a JavaScript data structure from the data in a JSON file?**
  - By reading and parsing it. (`fs.readFileSync` / `fs.readFile`; `JSON.parse`)
  - Also using `try…catch` helps catch parsing errors.

# 1.6. View Basics

- **Explain the difference between JavaScript object data structure and DOM data structure.**
  - **Scope and Context:**
    - JavaScript objects are used within the context of a JavaScript program to represent data and behavior.
    - DOM is specific to web development and provides a way for JavaScript to interact with and manipulate web documents.
  - **Representation:**
    - JavaScript objects are typically defined using literal notation or constructed with the `new Object()` syntax.
    - DOM is a standardized interface for representing the structure of HTML or XML documents in a hierarchical tree-like structure.
  - **Manipulation:**
    - JavaScript objects are manipulated using JavaScript methods and operations.
    - DOM manipulation involves using JavaScript to interact with and modify the elements, attributes, and content of an HTML or XML document.

- **What are the necessary steps to change the content of an HTML element using JavaScript?**
  - Selecting the HTML element (for example with `.getElementById`) and modifying it (for example with `insertAdjacentHTML`).

# 1.7. Event Basics

- **Define an event listener in JavaScript.**
  - An event listener in JavaScript is a function attached to a DOM element that listens for a specific event, triggering a defined set of instructions or code when that event occurs.

- **Outline the steps involved in changing the content of an HTML element when it is clicked.**
  - Select HTML element.
  - Write a function that changes the element.
  - Add Event Listener (`selectedElement.addEventListener("click", previousFunction);`).

- **Inside a click event listener, how can you access the element that was clicked?**
  - With the event object (`event.target`).
# 1.8. Design Basics

- **Differences between display: block, display: inline, and display: inline-block in CSS:**
  - **display: block;**
    - **Behavior:** Renders as a block-level element, starting on a new line, and takes up the full width available.
    - **Common Use Cases:** For structural elements like `<div>`, `<p>`, or headings, where a new line break before and after is desired.
  - **display: inline;**
    - **Behavior:** Renders as an inline element, flowing within the content and not starting on a new line. Only takes up as much width as necessary.
    - **Common Use Cases:** Suitable for elements like `<span>`, `<a>`, or other elements where you want them to flow within the text without creating line breaks.
  - **display: inline-block;**
    - **Behavior:** Combines aspects of both block and inline elements. Renders as an inline element but allows for setting width, height, margins, and padding.
    - **Common Use Cases:** Useful when you want elements to flow within the text but also have control over their dimensions, such as creating navigation items or grouping inline elements with specific dimensions.

- **Distinctions between position: relative and position: absolute CSS properties:**
  - **position: relative;**
    - **Behavior:** Positions an element relative to its normal position in the document flow.
    - **Reference Point:** Acts as the reference point for absolutely positioned child elements.
  - **position: absolute;**
    - **Behavior:** Positions an element relative to its nearest positioned ancestor (if any); otherwise, it positions it relative to the initial containing block (usually the `<html>` element).
    - **Taken out of Flow:** Does not contribute to the normal document flow, meaning other elements may overlap it.

- **Box Model:**
  - The box model in CSS consists of content, padding, border, and margin around each element.
  - **Associated Properties:**
    - `width` and `height`: Define the size of the content box.
    - `padding`: Clears an area around the content, inside the border.
    - `border`: A border surrounding the padding.
    - `margin`: Clears an area outside the border.

- **CSS properties that affect font and text appearance:**
  - **Font Properties:**
    - `font-family`: Specifies the font family for text.
    - `font-size`: Sets the size of the font.
     - `font-weight`: Sets the boldness of the font.
  - **Text Properties:**
    - `color`: Defines the color of the text.
    - `line-height`: Sets the height of a line of text.
    - `text-align`: Aligns the text within its container.

- **Steps for adding or removing a class name from an HTML element:**
  1. Select element
  2. `element.classList.add()` or `element.classList.remove()`

# 1.9. JavaScript - Language Specialties

- **Differences between value and reference data types in JavaScript:**
  - Primitives store values directly, making copies by duplicating those values. Reference types store references to memory addresses, allowing changes to their properties. When assigned or passed, reference types copy the reference, not the actual object. These differences impact assignment, equality comparison, and mutability, essential considerations for variable handling in JavaScript.

- **Concept of mutability and immutability in objects, arrays, and primitives:**
  - Objects and arrays in JavaScript can be changed after creation (mutable), while numbers and strings remain fixed once assigned (immutable).
  - Note: reassignment and change are different.
  - Understanding mutability is important for easier error correction and finding solutions.

- **Is null considered an object or a primitive in JavaScript?**
  - Primitive (despite what the `typeof` tells you)

- **What does undefined represent in JavaScript?**
  - The absence of a defined value (for example, a function without a return statement)

- **When would you use var, let, and const in JavaScript?**
  - `const`: when the variable value should not change.
  - `let`: when the variable needs to be reassigned.
  - `var`: when I want weird hoisting and a variable that can be redeclared

- **Explain the concept of hoisting in JavaScript:**
  - In JavaScript, hoisting is a behavior where variable and function declarations are moved to the top of their containing scope. This mainly comes into effect with function declarations (not function expressions), because they are fully hoisted.
  - Hoisting variables is less practical because only their declarations are hoisted; their initializations aren’t.
# 1.10. Git

- **Advantages of using a version control system:**
  - **History and Traceability:**
    - Version control systems maintain a complete history of changes made to a project. Developers can trace back to specific versions, identify when changes were made, and understand who made those changes.
  - **Collaboration:**
    - Version control facilitates collaboration among team members. Multiple developers can work on the same project concurrently, and the version control system helps merge their changes seamlessly.
  - **Branching and Parallel Development:**
    - Developers can create branches to work on features or bug fixes independently. This allows for parallel development without affecting the main codebase until changes are ready to be integrated.
  - **Revert Changes:**
    - If a mistake is made or an undesired change is introduced, version control allows developers to revert to a previous state, effectively undoing changes.
  - **Conflict Resolution:**
    - Version control systems provide mechanisms to handle conflicts that may arise when multiple developers modify the same piece of code simultaneously. Conflicts can be resolved before merging changes.
  - **Backup and Recovery:**
    - Projects stored in version control systems serve as a backup. In case of data loss or corruption, the entire project can be restored to a previous state.
  - **Code Reviews:**
    - Code reviews are facilitated by version control systems, allowing team members to review changes before they are merged into the main codebase.

- **Differences between Git and GitHub:**
  - Git is the version control system, and GitHub is a hosting platform.

- **Purpose of remote repositories in Git:**
  - Enables multiple developers working on a project, serves as a backup, and makes sharing the code easier. Also, open-source development wouldn't be practical without it.

- **When does a merge conflict occur in Git?**
  - A merge conflict in Git occurs when the changes made in two different branches cannot be automatically merged by Git.

# 1.11. Terminal

- **How to execute a JavaScript file in the terminal:**
  - `node fileName.js`

- **Keyboard shortcut to stop a running process in the terminal:**
  - `Ctrl + C`

- **How to retrieve the previous command executed in the terminal:**
  - By scrolling up or by using the arrow keys

- **How to navigate to the parent directory of the current directory in the terminal:**
  - `cd ..`
