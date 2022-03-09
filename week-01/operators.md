
# Operators

Values can be combined using **operators**, such as:

* PLUS (`+`)
* TIMES (`*`)
* POWER (`**`)
* DOT (`.`)
* ASSIGNMENT (`=`)
* COMPARISON (`===`)

An operator *sends a message* to the value

* e.g. `1 + 2` sends the number `1` the message `please add 2 to yourself`.

The Dot `.` is a special operator that *sends arbitrary messages*; we will learn more about that later.

## Types of Operators

Like data there are several different *types* of operators

* Assignment
* Comparison
* Arithmetic
* Logical
* Conditional
* [And many more exist too](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)

## Comments

When reading JavaScript code, if you ever see two slashes in a row, that means "everything after these slashes is a comment".

```js
// this is a comment

2 + 2 // results in four
```

A comment is a message for humans. JavaScript ignores everything to the right of the slashes, so you can explain what the nearby code does, or why it does it.

In these lessons, we often use comments to explain the *result* of executing the nearby code. In this case, we sometimes add an arrow to the comment:  

```js
2 + 2  // => 4
3 + 5  // => 8
```

## Multi Line Comments

JavaScript also has multi-line comments via `/* ... */` but those are less common. They can also be used to comment out a section within a line:  

```js
/* This is
 * a multiline
 * comment! */

console.log(x /*some variable from earlier*/);
```

## Expression Evaluation

A snippet of JavaScript code is called an *expression*.

Whenever JavaScript encounters an expression, it tries to *evaluate* it, which means to convert it into a *value*.

A simple expression (like a plain number or a string) evaluates to just that value.

A more complicated expression with operators keeps applying those operators until it gets down to a single value.

When an expression is evaluated, it gives you back a value. The act of giving back the value is *returning*.

> You can think of evaluation as *asking and answering* a question.

## Expression Examples

```js
2 + 2    // Question: What is 2 + 2?
4        // Answer: 4

// Q: What is the all-caps version of the string "apple"?
"apple".toUpperCase()  
// A: the string "APPLE"
"APPLE"
```

We say that a statement **evaluates to** a value, as in
"2 plus 2 *evaluates to* 4". You can also say "the value of 2 + 2 is 4" or "the return value of 2 + 2 is 4".

## Return Values

When code expressions are run (evaluated), they result in a new value.

This value is called a `return` value.

Sometimes the return value is the same as the original value.

```js
4 * 1    // return value: 4
```

Sometimes the return value is a different value.

```js
2 + 3    // return value: 5
```

Sometimes the return value is a different value *and* a different type.

```js
"banana".length  // return value: 6
```

## Special Values

Sometimes the return value is a special value!

```js
(5).length     // return value: undefined
5 / 0          // return value: Infinity
"cookie" * 10  // return value: NaN
```

## Expressions vs. Statements

JavaScript (like most languages derived from C) makes a distinction between *expressions* and *statements*.

*expression* means "code that can be evaluated" or "code that has a value", e.g.:

```js
1 + 1
```

*statement* means "code that does something", e.g.

```js
console.log("hello")
```

## Values

Some statements have values, so `node` will *evaluate* them and *print* those values...

```js
1 + 1
// evaluates to 2
```

...but *some statements have no value* (even though they contain expressions that *do* have value), and this can cause some surprising effects, e.g.:

```js
x = 10
// evaluates to 10
let x = 20
// evaluates to undefined
```

# Expression vs Statements

|             Expression   | Statement                    |
|--------------------------|------------------------------|
| has a value              | does something               |
| can be assigned to a var | has a semicolon (optionally) |
|                          | contains expressions         |

[Expressions vs. Statements - 2ality.com](https://2ality.com/2012/09/expressions-vs-statements.html)
