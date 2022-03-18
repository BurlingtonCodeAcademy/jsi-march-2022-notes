# Playing With Strings

## Welcome

Strings are one of the most common data types you'll find in programming. The primary use for strings is to represent natural (spoken) language in a program. It's worth noting that almost all user input will come into your program as a string.

## What is a String?

A string is a collection of characters between quotes. Everything inside the quotations is a single string.

Every string also has a `length` property, that tells you how many characters are in that string.
e.g.

```js
"banana".length // returns the number 6
```

But do empty characters, such as spaces, count towards a string's length?

What's the length of this string: `"All dogs are good dogs"`?

## String Indexing

You can access specific characters inside a string by their index number.

## String Methods

There are many methods attached to all strings. Try the following in a Node environment, and see what happens:

```js
"titanic".toUpperCase()
"QUIETLY".toLowerCase()
"Java".repeat(10)
"berry".charAt(1)
"berry".charAt(0)
"banana".includes("nan")
"banana".endsWith("ana")
"blueberry".replace("blue", "black") //will replace the FIRST instance of the word you're trying to change 
"blueberry".replaceAll("blue", "black") //will replace ALL instances of the word you're trying to change
```

## Example Code (this is just one solution [not the only solution])

```js
// Assign the string to a variable
let string = "this is a fantastic string" 
// Method chaining allows us to make the string upper case and replace each empty string with a newline at the same time
string = string.toUpperCase().replaceAll(" ", "\n") 
// Print string to the console
console.log(string)
```

## Flavors of Quotes

In Javascript you can use any kind of quotation marks you want to designate a string, single quotes, double quotes, backticks, they all work! Try the following operations, and see if you can answer the questions below.

```js
"drive" + "way"
'Java' + "Script"

"Bert's pal Ernie" + ' sings "Rubber Duckie"'
```

- What happens when you put single quotes inside double quotes (and vice versa)?
- What happens when you add a single quoted string to a double quoted string
  - What if there are interior quotes inside those strings?

## String Concatenation

When you add two or more strings together they become a single string. This is known as concatenation. Strings will concatenate with pretty much any data type, and will always coerce that type into a string.

## Template Strings

If you use backticks as your quotations you have created a template string. One of the benefits of template strings is that you can use special characters `${}` to escape back to JavaScript so that you can insert expressions directly into your strings.

```js
`Two plus two is ${2 + 2}`
```

The above string would print out "Two plus two is 4"

## Characters

A string is composed of a sequence of characters.
A character is a Number, or _character code_, that stands for a symbol.

ASCII: American Standard Code for Information Interchange was invented in 1963
[Check out the ASCII Table](https://commons.wikimedia.org/wiki/File:ASCII-Table-wide.svg)

ASCII only goes from 0 to 127 which just isn't representative of all the characters that exist in the world!

Good thing there is Unicode, which currently has more than 130,000 characters, including symbols.
Note that ASCII and Unicode share the same first 0 to 127 characters; Unicode expands beyond after the 127th.

## Comparing Strings

Strings are compared one character at a time using the Unicode values of each character.

```js
'apple' > 'cherry' // The character code for 'a' is lower than the character code for 'c' so this comparison will return the boolean value false
false
'banana' < 'cherry'
true
```