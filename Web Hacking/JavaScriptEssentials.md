# JavaScript Essentials

- **Platform:** TryHackMe
- **Difficulty:** Easy
- **Status:** ✅ Completed
- **Topics:** JavaScript, HTML, Variables, Functions, Dialogs, Control Flow

## Introduction

In this room, I learned the basics of JavaScript and how it is used to make websites interactive. I also learned how JavaScript works with HTML and why understanding it is important for web application security.

## What is JavaScript?

JavaScript is a programming language that runs in the user's web browser. It allows websites to respond to user actions, update page content, validate forms, and communicate with web servers without reloading the page.

Some common uses of JavaScript include:

- Form validation
- Button click events
- Pop-up messages
- Dynamic page updates
- Fetching data from a server

## Basic JavaScript Concepts

The room introduced several important JavaScript concepts, including:

- Variables
- Functions
- Objects
- Arrays
- Events
- Conditions
- Loops

These concepts are the foundation of writing JavaScript code.

## Using JavaScript in HTML

JavaScript can be added to a webpage using the `<script>` tag.

It can either be written directly inside an HTML file or loaded from an external JavaScript file.

Example:

```html
<script src="script.js"></script>
```

Using external files keeps the code organized and easier to maintain.

## JavaScript Dialog Functions

JavaScript provides built-in dialog functions for interacting with users.

| Function | Description |
|----------|-------------|
| `alert()` | Displays a message box. |
| `confirm()` | Displays a message with **OK** and **Cancel** buttons. |
| `prompt()` | Asks the user to enter input. |

These functions are useful for learning JavaScript, but they are rarely used in modern websites because they interrupt the user experience.

## Control Flow Statements

Control flow statements allow a program to make decisions and repeat actions.

Common statements include:

- `if`
- `else`
- `else if`
- `switch`

JavaScript also provides loops for repeating code:

- `for`
- `while`
- `do...while`

These statements help control how the program executes.

## Minified JavaScript Files

Minified JavaScript files have unnecessary spaces, comments, and formatting removed to reduce file size and improve loading speed.

Although they are difficult to read, browser developer tools can format them to make analysis easier during security testing.

## Best Practices

Some good JavaScript practices include:

- Use meaningful variable names.
- Keep code clean and organized.
- Store JavaScript in external files when possible.
- Validate user input.
- Never store sensitive information in client-side JavaScript.
- Add comments when necessary to improve readability.

## Key Takeaways

- JavaScript makes websites interactive.
- It can be embedded in HTML or loaded from external files.
- Variables and functions are essential building blocks.
- Control flow statements allow programs to make decisions.
- Minified files improve performance but are harder to read.
- Sensitive information should never be stored in client-side JavaScript.

## References

- TryHackMe – JavaScript Essentials
- Mozilla Developer Network (MDN) – JavaScript Documentation
