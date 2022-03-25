# Session-06

Today we started the class by reviewing the "Titlelize" challenge (thank you Dominic for sharing your code!!) See below for a solution that we talked through in class.

We also discussed Loops and Logic!

**Example of a Solution for Titleize Challenge**

```js
function titleize(someString) {
  let stringSplit = someString.split(" ");
  let count = 0;
  let finalString = " ";

  console.log(stringSplit); // => ["all", "dogs", "are", "good", "dogs"]

  while (count < stringSplit.length) {
    let upperCased =
      stringSplit[count][0].toUpperCase() +
      stringSplit[count].slice(1).toLowerCase();
    finalString = finalString + " " + upperCased;
    count += 1;
  }
  return finalString;
}
console.log(titleize("all dogs are good dogs"));
// should print "All Dogs Are Good Dogs"
```

## Loops

A _LOOP_ is when a program does something repeatedly, until some CONDITION is met. Two commonly used include:

- **While Loops**
- **For Loops**

As you'll see, these two types of loops achieve the same result. As you practice with loops pay attention to what syntax you like more.

**The While Loop**
The simplest kind of loop is the _while loop_.

A while statement checks the condition every cycle
IF condition evaluates to true, THEN loop again
IF condition evaluates to false, THEN stop looping and proceed to the code after the loop.

The loop below counts from one to five, followed by Ha ha ha! each time.

```js
let count = 1;
while (count <= 5) {
  // the code below runs once per loop cycle
  console.log("" + count + ", Ha ha ha!");
  count = count + 1;
}
```

You can use a boolean value as a conditional for your while loop, but it's not recommended. See below for an example of how a boolean value used as a conditional creates an _infinite loop_:

```js
while (true) {
  // will loop forever
  // because true is always true
  console.log("Hello");
}
```
_Note_: To escape from an infinite loop type: CONTROL+C keys

If the program encounters the keyword `break` the loops stops.
Alternative code counting from 1 to 100 using break is below:

```js
let count = 0;
while (true) {
  if (count > 100) {
    break;
  }

  console.log(count);
  count = count + 1;
}
```

**For Loops**
A while loop is simple, but requires a variable in the condition or the break keyword.

There is another kind of loop called a _for loop_.

```js
for (let count = 1; count <= 100; count++) {
  console.log(count);
}
```

## Logic

In order to make a DECISION, a program needs to use LOGIC expressions and CONDITIONAL statements.

**Conditional Statements**
The key word `if` is used to create a CONDITIONAL

The EXPRESSION following the `if` is the TEST

When the TEST evaluates to TRUE the code in the body runs

```js
let age = 17;
if (age < 18) {
  console.log("Sorry, you cannot vote yet.");
}
```

[MDN: Conditional Statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)

**What is True**
Any VALUE or EXPRESSION that EVALUATES to a non-false value is EQUIVALENT to TRUE
[MDN: Truthy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy)

**What is False**
The only VALUES considered EQUIVALENT to FALSE are listed below:

```js
false;
null;
undefined;
("");
0 - 0;
NaN;
```

[MDN: Falsy](https://developer.mozilla.org/en-US/docs/Glossary/Falsy)

**If..Else**
The keyword `else` allows for a CONDITIONAL to BRANCH.

```js
let age = 17;

if (age >= 18) {
  console.log("You are allowed to vote.");
} else {
  console.log("Sorry, you cannot vote yet.");
}
```

**If..Else Nesting**
It is possible to nest CONDITIONAL statements, _but_ it can become confusing and can make it more difficult to debug. So, nest with caution.

```js
let age = 17;

if (age >= 18 /* first test */) {
  if (hasPermission /* second test */) {
    console.log("You have special permission.");
  } /* first else */ else {
    console.log("You are allowed to vote.");
  }
} /* second else */ else {
  console.log("Sorry, you cannot vote yet.");
}
```

**If..Else..If**
The keywords else if allow for the chaining of CONDITIONALs, which can be easier to understand.

```js
if (x > 50) {
  /* do something */
} else if (x > 5) {
  /* do something */
} else {
  /* do something */
}
```

[MDN: if else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else#using_else_if)

## Reading & Homework

- [Count to One Hundred](https://replit.com/@Upright-JSI-Mar-2022/count-to-one-hundred#index.js)
- [One Potato](https://replit.com/@Upright-JSI-Mar-2022/one-potato#index.js)
- [Good Friend, Bad Friend](https://replit.com/@Upright-JSI-Mar-2022/good-friend-bad-friend#index.js)
- [Enemy List](https://replit.com/@Upright-JSI-Mar-2022/enemy-list#index.js)


