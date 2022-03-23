# Session-05

Today we started class by sharing our code samples from the homework (so many great solutions, everyone!) and then moved on to cover Variables and Functions.

# Variables

## Let vs Var vs Const

- `let` declares a variable in JavaScript
- `const` declares a variable that cannot be reassigned
- `var` is like let but is no longer recommended

_Note_: You can only declare a variable with `let` keyword once.
The code snippet below will return a SyntaxError because the `let` keyword is used to declare the variable `name` more than once:

```js
let name = "Grace";
let name = "Hopper";
// Identifier 'name' has already been declared
```

## Terminology

_Legacy code_: Code that was created awhile ago that needs to be updated.

## Variables as Documentation

Variables provide helpful context! They give meaning and context to values in our code. 
By assigning variables to our values we can then more easily manipulate our values in other parts in our code.

*Which is clearer?:*
```js
60 * 60 * 24;
```
or 
```js
let secondsPerMinute = 60;
let minutesPerHour = 60;
let hoursPerDay = 24;
let secondsPerDay = secondsPerMinute * minutesPerHour * hoursPerDay;
```

## Lab: Play in the Console

Here is *a* solution for the poem challenge that we worked on in a node environment:

```js
let poem = "roses are red, violets are blue";
let formatted = poem.replace(",", "\n");
console.log(formatted);
```

## Changing Variables

You can assign and reassign variables at will.
_Remember_: You can only declare a variable with the `let` keyword once.

- Reassignment changes the name of an object. It does not change the data inside the object
- This is analogous to removing a label from one box and placing it on a different box

```js
let color = "blue"; // assign 'blue' to color
let fruit = "berry"; // assign 'berry' to fruit
color + fruit; // 'blueberry'

color = "black"; // 'black'
color + fruit; // 'blackberry'
```

Three different variable names that point to _three distinct instances_ of "Apple":
```js
let snack = "Apple";
let fruit = "Apple";
let tree = "Apple";
```

Three different variables that point to the _one instance_ of "Apple":
```js
let snack = "Apple";
let fruit = snack;
let tree = fruit;
```

## Summary: Variables

- Variables are names for memory locations, which hold values
- declaring a variable says what its scope is
- assigning a variable changes which location it points to
- you can have many names for the same location
- sometimes values can change on the inside of a location
  (which is useful but could cause bugs)

## Functions

A FUNCTION is just a NAME for a piece of code. Names of functions should be _concise_ and _descriptive_.
If your going to use a piece of code more than once, you can make your life a lot easier by making it a function

## Function example

Here's an example function:
```js
function add(firstNum, secondNum) {
  let sum = firstNum + secondNum;
  return sum;
}

add (3, 2) //=> 5
add (12, 30) //=> 42

```
- `function` means, define a function
- `add` is the name of the function
- `firstNum`, secondNum are the parameters to the function, also called arguments
- `sum` is a local variable of the function
- `sum` is also the return value of the function
- `add (3, 2)` is an example of *calling* the `add` function

*Note*: In order to get the above function example to work, we need to call/execute the function. 

## Passing Variables as Parameters

You can pass values as parameters *and* you can pass variables as parameters (this makes sense because variables are just names that have been assigned to values).

When you pass a variable to a function, that variable value is assigned to a parameter.
```js
let nameToShout = 'Grace Hopper';
shouter(nameToShout);
// 'GRACE HOPPER!!!'
```

## Reading & Homework
Below are the links to challenges for the homework, some of them were already introduced earlier tonight.

Note: The last lab, "Titleize", is challenging! If you don't find a solution before Thursday, don't worry! 

- [Divisible](https://replit.com/team/Upright-JSI-Mar-2022/divisible)
- [Capitalize](https://replit.com/team/Upright-JSI-Mar-2022/capitalize)
- [Age Calculator](https://replit.com/team/Upright-JSI-Mar-2022/age-calculator)
- [Age-In-Years](https://replit.com/team/Upright-JSI-Mar-2022/age-in-years)
- [Supply Calculator](https://replit.com/team/Upright-JSI-Mar-2022/supply-calculator)
- [Titleize String](https://replit.com/team/Upright-JSI-Mar-2022/titleize-string)
   

- And if you haven't already, please finish reading the chapter on Functions in Eloquent JavaScript 



