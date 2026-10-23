
# JavaScript Fundamentals — Complete Beginner's Guide

Welcome to JavaScript! JavaScript makes websites interactive and dynamic. In this guide, you'll learn the fundamentals step by step, practice each concept, and build small projects along the way.

**Goal:** Understand core JavaScript concepts and build interactive web pages without blindly copying code.

**Prerequisites:** Complete [Getting Started](00-getting-started.md), [HTML Fundamentals](01-html-fundamentals.md), and [CSS Fundamentals](02-css-fundamentals.md).

---

## How to Use This Guide

For each step:

1. Watch the recommended lecture or search for a suitable lesson.
2. Write the examples yourself instead of only watching.
3. Complete the practice tasks.
4. Move forward when you can explain the concept in your own words.

**Video-link note:** The links below open YouTube searches for the relevant topic, not a specific verified video. Choose a clear, up-to-date lecture that covers the listed concepts. Prefer one comprehensive lecture per section when it covers everything you need.

---

## Step 1: Understand What JavaScript Does

### Learn

- What JavaScript is and why websites use it
- The difference between HTML, CSS, and JavaScript
- How JavaScript runs in a browser
- The browser console and developer tools
- How to connect an external JavaScript file to HTML

### Watch

- [JavaScript for Beginners — Introduction and Basics](https://www.youtube.com/results?search_query=javascript+for+beginners+full+course+introduction)
- [How to Connect JavaScript to HTML](https://www.youtube.com/results?search_query=how+to+link+javascript+file+to+html)

### Practice

1. Create `index.html` and `script.js`.
2. Connect `script.js` to your HTML using a `<script>` element.
3. Use `console.log()` to print a message.
4. Open your browser's developer tools and find the message in the Console.

**Example:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript Practice</title>
  <script src="script.js" defer></script>
</head>
<body>
  <h1>Learning JavaScript</h1>
</body>
</html>
```

```javascript
console.log("Hello, JavaScript!");
```

**Checkpoint:** You can explain what JavaScript does and run a JavaScript file in your browser.

---

## Step 2: Variables and Data Types

### Learn

- `let` and `const`
- Variable naming rules
- Strings and numbers
- Booleans
- `undefined` and `null`
- Basic type conversion
- The difference between `==` and `===`

Prefer `const` by default and use `let` when you need to reassign a variable. Avoid `var` while learning modern JavaScript.

### Watch

- [JavaScript Variables and Data Types](https://www.youtube.com/results?search_query=javascript+variables+data+types+let+const+beginner)

### Practice

1. Store your name, age, and favorite technology in variables.
2. Create a variable for a product price and another for its quantity.
3. Calculate the total price.
4. Print the values and their types using `typeof`.
5. Experiment with converting a string to a number.

**Checkpoint:** You can create variables, identify common data types, and explain when to use `let` or `const`.

---

## Step 3: Operators and Expressions

### Learn

- Arithmetic operators: `+`, `-`, `*`, `/`, `%`, `**`
- Assignment operators
- Comparison operators
- Logical operators: `&&`, `||`, `!`
- Increment and decrement
- Operator precedence

### Watch

- [JavaScript Operators Explained](https://www.youtube.com/results?search_query=javascript+operators+arithmetic+comparison+logical+beginner)

### Practice

1. Build a simple calculator using two numbers.
2. Calculate the remainder after division.
3. Check whether someone meets a minimum age requirement.
4. Combine two conditions using logical operators.

**Checkpoint:** You can use operators to perform calculations and evaluate conditions.

---

## Step 4: Conditional Statements

### Learn

- `if`, `else if`, and `else`
- Nested conditions
- `switch`
- The ternary operator
- Truthy and falsy values

### Watch

- [JavaScript If Else, Switch, and Ternary Operators](https://www.youtube.com/results?search_query=javascript+if+else+switch+ternary+operator+tutorial)

### Practice

1. Check whether a number is positive, negative, or zero.
2. Check whether a number is even or odd.
3. Convert a score into a grade.
4. Build a simple login-condition demonstration.
5. Use `switch` to display a message for a selected day.

**Checkpoint:** You can choose different actions based on conditions.

---

## Step 5: Loops

### Learn

- `for` loops
- `while` and `do...while`
- `break` and `continue`
- Loop counters
- Nested loops
- Iterating over arrays

### Watch

- [JavaScript Loops for Beginners](https://www.youtube.com/results?search_query=javascript+for+while+do+while+loops+beginner)

### Practice

1. Print numbers from 1 to 100.
2. Print the multiplication table of a number.
3. Calculate the sum of numbers from 1 to 100.
4. Print only even numbers in a range.
5. Iterate through a list of names.

**Checkpoint:** You can repeat a task using an appropriate loop and avoid accidental infinite loops.

---

## Step 6: Functions

### Learn

- Function declarations
- Function expressions
- Arrow functions
- Parameters and arguments
- Return values
- Default parameters
- Local and global scope
- Why reusable functions matter

### Watch

- [JavaScript Functions and Arrow Functions](https://www.youtube.com/results?search_query=javascript+functions+arrow+functions+parameters+return+beginner)

### Practice

1. Create a function that adds two numbers.
2. Create a function that converts Celsius to Fahrenheit.
3. Write a function that checks whether a number is even.
4. Rewrite a simple function as an arrow function.
5. Create a function that accepts a name and returns a greeting.

**Checkpoint:** You can write reusable functions and explain the difference between parameters and return values.

---

## Step 7: Arrays and Array Methods

### Learn

- Creating and accessing arrays
- Array indexes and `length`
- Adding and removing items with `push`, `pop`, `shift`, and `unshift`
- `slice()` and `splice()`
- `forEach()`
- `map()`
- `filter()`
- `find()`
- `includes()`
- Basic sorting and common array pitfalls

### Watch

- [JavaScript Arrays and Array Methods](https://www.youtube.com/results?search_query=javascript+arrays+map+filter+forEach+find+beginner)

### Practice

1. Create an array of five favorite technologies.
2. Add and remove an item.
3. Use `map()` to double an array of numbers.
4. Use `filter()` to select numbers greater than 10.
5. Use `find()` to locate a specific item.

**Checkpoint:** You can store collections of data and transform or search them using array methods.

---

## Step 8: Objects

### Learn

- Object literals
- Properties and methods
- Dot notation and bracket notation
- Adding, updating, and deleting properties
- Nested objects
- The `this` keyword at a basic level
- `Object.keys()`, `Object.values()`, and `Object.entries()`

### Watch

- [JavaScript Objects for Beginners](https://www.youtube.com/results?search_query=javascript+objects+properties+methods+beginner)

### Practice

1. Create an object describing a student.
2. Add properties for name, course, and skills.
3. Update one of its properties.
4. Add a method that returns a short introduction.
5. Create an array of objects representing products.

**Checkpoint:** You can model related information using objects and access their properties.

---

## Step 9: DOM Manipulation

The Document Object Model (DOM) lets JavaScript interact with HTML elements on a page.

### Learn

- What the DOM is
- `document.querySelector()` and `querySelectorAll()`
- `textContent` and `innerHTML`
- Changing styles and classes
- `classList.add()`, `remove()`, and `toggle()`
- Creating, inserting, and removing elements
- Why inserting untrusted input with `innerHTML` can be unsafe

### Watch

- [JavaScript DOM Manipulation Full Tutorial](https://www.youtube.com/results?search_query=javascript+dom+manipulation+querySelector+classList+createElement+beginner)

### Practice

1. Change a heading when a button is clicked.
2. Change a page's background color.
3. Add a new list item to a list.
4. Toggle a CSS class on an element.
5. Remove an element from the page.

**Checkpoint:** You can select HTML elements and update page content using JavaScript.

---

## Step 10: Events and Forms

### Learn

- `addEventListener()`
- Click, input, submit, and change events
- The event object
- `preventDefault()`
- Reading form input values
- Basic form validation
- Event bubbling at an introductory level

### Watch

- [JavaScript Events and Form Handling](https://www.youtube.com/results?search_query=javascript+addEventListener+form+handling+preventDefault+beginner)

### Practice

1. Make a button increase a counter.
2. Display text as a user types.
3. Build a form that accepts a name and email.
4. Prevent the form's default submission and validate the inputs.
5. Display a friendly error message when required fields are missing.

**Checkpoint:** You can respond to user interactions and handle form input.

---

## Step 11: Modern JavaScript (ES6+)

### Learn

- Template literals
- Destructuring arrays and objects
- Spread and rest syntax
- Optional chaining
- Nullish coalescing (`??`)
- Modules: `export` and `import`
- Useful modern syntax without overusing shortcuts

### Watch

- [Modern JavaScript ES6+ Features](https://www.youtube.com/results?search_query=modern+javascript+ES6+features+destructuring+spread+modules)

### Practice

1. Use template literals to generate a greeting.
2. Destructure a person's name from an object.
3. Copy an array using spread syntax.
4. Use optional chaining with a nested object.
5. Split a small program into two JavaScript modules.

**Checkpoint:** You can read and write common modern JavaScript syntax.

---

## Step 12: Error Handling and Debugging

### Learn

- Syntax errors and runtime errors
- Reading browser console messages
- `try`, `catch`, and `finally`
- Throwing errors with `throw`
- Using breakpoints and the Sources panel
- Debugging one step at a time

### Watch

- [JavaScript Error Handling and Debugging](https://www.youtube.com/results?search_query=javascript+debugging+try+catch+browser+devtools+beginner)

### Practice

1. Intentionally introduce a syntax error and fix it.
2. Debug a function that returns the wrong result.
3. Use `try...catch` to handle an expected error.
4. Set a breakpoint and inspect variable values.

**Checkpoint:** You can investigate an error instead of randomly changing code until it works.

---

## Step 13: Asynchronous JavaScript

Asynchronous JavaScript helps your program handle work that takes time, such as network requests.

### Learn

- Synchronous vs. asynchronous execution
- Callbacks at a basic level
- Promises
- `.then()` and `.catch()`
- `async` and `await`
- `fetch()`
- JSON parsing
- Handling failed network requests
- Loading and error states

### Watch

- [JavaScript Promises, Async Await, and Fetch](https://www.youtube.com/results?search_query=javascript+promises+async+await+fetch+API+beginner)

### Practice

1. Use `fetch()` to request data from a public test API.
2. Display the returned data on a page.
3. Show a loading message while waiting.
4. Display an error message if the request fails.
5. Use `async` and `await` with `try...catch`.

**Checkpoint:** You can explain promises and retrieve remote data without freezing the page.

---

## Step 14: JSON and Browser Storage

### Learn

- What JSON is
- `JSON.stringify()` and `JSON.parse()`
- `localStorage` and `sessionStorage`
- Saving and loading simple data
- Storage limitations
- Why sensitive information should not be stored carelessly in browser storage

### Watch

- [JavaScript JSON and Local Storage](https://www.youtube.com/results?search_query=javascript+JSON+localStorage+sessionStorage+beginner)

### Practice

1. Save a theme preference in `localStorage`.
2. Restore the preference when the page reloads.
3. Save a small list of tasks as JSON.
4. Load the saved list when the application starts.

**Checkpoint:** You can persist simple application preferences and data in the browser.

---

## Step 15: Build a JavaScript Project

Build a **Task Tracker** that combines the concepts from this guide.

### Required features

- Add a task using a form
- Display all tasks on the page
- Mark tasks as completed
- Delete tasks
- Filter all, completed, and pending tasks
- Save tasks to `localStorage`
- Restore saved tasks after refreshing
- Validate empty input
- Show a helpful message when no tasks exist
- Use separate HTML, CSS, and JavaScript files

### Build it in stages

1. Create the HTML layout.
2. Style the page using CSS.
3. Create an array to hold tasks.
4. Write functions for adding, rendering, completing, and deleting tasks.
5. Connect buttons and forms with event listeners.
6. Save and load tasks using `localStorage`.
7. Test empty inputs and unusual cases.
8. Update the README with features and screenshots.

### Optional challenges

- Add due dates.
- Add task priorities.
- Add a search box.
- Add dark mode.
- Make the layout responsive.
- Add a task counter.

**Project completion:** You can explain how your app works, fix bugs, and add a feature without following a tutorial line by line.

---

## Recommended Learning Resources

Use these free resources alongside the video lessons.

- [MDN JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide) — a detailed reference for JavaScript concepts.
- [JavaScript.info](https://javascript.info/) — structured lessons from fundamentals to advanced topics.
- [MDN DOM Introduction](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) — understand the DOM.
- [MDN Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) — learn how to request data.
- [freeCodeCamp JavaScript Courses](https://www.freecodecamp.org/learn/) — interactive practice and projects.

---

## Final Completion Checklist

Mark each item when you can do it without copying a complete solution.

- [ ] Run JavaScript in the browser.
- [ ] Use variables, data types, and operators.
- [ ] Write conditional statements and loops.
- [ ] Create reusable functions.
- [ ] Work with arrays and objects.
- [ ] Manipulate HTML through the DOM.
- [ ] Handle events and forms.
- [ ] Use modern JavaScript syntax.
- [ ] Debug errors and handle exceptions.
- [ ] Fetch data asynchronously from an API.
- [ ] Save and restore simple data using browser storage.
- [ ] Build and explain the Task Tracker project.
- [ ] Write a README documenting the project.

## What's Next?

Continue to [Git and GitHub](04-git-and-github.md) to learn how to track your code, collaborate with others, and share your projects.

---

**Remember:** Consistent practice matters more than watching lots of tutorials. Write code every day, make mistakes, debug them, and keep building.
