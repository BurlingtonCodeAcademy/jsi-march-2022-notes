# Session-07

Tonight we learned about Input and Output and scope.

We started off the class by going over the Frenemy Lab. A couple **array methods** highlighted in the solutions discussed include:

- `.indexOf()`

- `.includes()`

## Input and Output

- Performing calculations and using memory is fast
- Reading Input and writing Output is slow
  - CPU operations = nanoseconds, 1/1,000,000,000 second
  - I/O operations = milliseconds to seconds
- During an I/O operation, the program is paused, or waits.
  - CPU does other things during that time.

## Using Readline

`readline` is a library, which is code you can use, but someone else wrote. Readline is a **node standard library**, meaning that it is already built into JavaScript. In order to use it, you just need to include the boilerplate code at the top of your file.

Use Readline as demonstrated in the following example:

```js
// include the library
const readline = require("readline");
// create an "interface", using STDIN and STDOUT
const readlineInterface = readline.createInterface(
  process.stdin,
  process.stdout
);
// create a function called "ask" that
// OUTPUTs a question, and waits for INPUT
function ask(questionText) {
  // use a "Promise", which stands in for a future answer
  return new Promise((resolve, reject) => {
    readlineInterface.question(questionText, resolve);
  });
}
```

## Async and Await

A **PROMISE** is something that stands in for a finished result, while a task is still processing. 

- [MDN: Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

- [MDN: Using Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)



Promises can be **awaited**, within a function marked as **async**.

1. await means "wait for the following to finish"
2. To use await inside a function, you must use mark it as async

**WARNING**: async functions and for loops do not mix well, use while instead

## Scope
The **SCOPE** is a context, including all the variables accessible from a given code location

There are different kinds of SCOPE:

- **Global**: can be accessed from anywhere
- **Local**: can only be accessed within where it is defined
    - Includes functions, loops, or code blocks
- **Private**: cannot be accessed beyond a specific place

**Remember**: Scope is like a one-way mirror, inner scopes can see out, but outer scopes cannot see in.


## Reading & Homework

Homework challenges within Replit

Note: The first four challenges are covered in class today, the last challenge is new.

- [Full Name](https://replit.com/team/Upright-JSI-Mar-2022/full-name-input-output)
- [Quest](https://replit.com/team/Upright-JSI-Mar-2022/quest-input-output)
- [Name Length](https://replit.com/team/Upright-JSI-Mar-2022/name-length-input-output-1)
- [Length of Each Name](https://replit.com/team/Upright-JSI-Mar-2022/length-of-each-name-input-output)
- [Frenemy](https://replit.com/team/Upright-JSI-Mar-2022/hello-frenemy-input-output)

### Labs

Labs covered in class include:
- Echo
- First and Last Name
- What is your Quest?
- Name Length
