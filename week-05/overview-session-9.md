# Session-09

Tonight we discussed **Arrays** and **Objects** and **Iteration Methods** oh my!

If you've already finished the "Guess The Number" project and want to take on an extra challenge, check out the Ice Box Challenges at the bottom of the notes doc.

## Arrays

- An array is a container for values
- It is an object that contains other objects
- It resembles an ordered list
- Square brackets around values indicates that it is an array

## Arrays are zero indexed

- Every "slot" in the array has an index
- You can retrieve any item in an array by its INDEX
- Square brackets after an array mean "get the N-th item in this array"

  - This method of accessing items is referred to as "square bracket notation" - The following code retrieves the fruit at index 1

  ```js
  let fruits = ["apple", "banana", "cherry"];
  fruits[1]; // => "banana"
  ```

**Creating an Array**

```js
let fruits = ["apple", "banana", "cherry"];
```

## Array Methods

[MDN: Array Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#instance_methods)
__Note__: You do NOT need to memorize these. Just skim them and remember how to get back to this documentation page later.

## Arrays and Loops

There are ways to loop through an array's items.

This means to go through the entire array, one item at a time, in order, and do something with each item.

JavaScript has had a **for loop** for quite some time. See an example below:

```js
let fruits = ["apples", "bananas", "cherries"];

for (let index = 0; index < fruits.length; index++) {
  console.log(fruits[index]);
}
```

Alternatively, you can use the **for..of loop**, which hides the messy details of incrementing an index counter and accessing each array item. See an example below:

```js
let fruits = ["apples", "bananas", "cherries"];
for (let fruit of fruits) {
  console.log("I like " + fruit + "!");
}
```

## Setting Items Within an Array

The `[]` operator works for assignment as well.

`fruits[0] = 'apricot'` will set the 0th item of the array to the string 'apricot'

## Helpful Links for Learning More About Arrays

- [JavaScript.info Arrays](https://javascript.info/array)
- [JavaScript.info Array Methods](https://javascript.info/array-methods)
- [MDN JavaScript Guide - Indexed Collections](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Indexed_collections)

## Software Models the World

- Data Structures allow for programmers to make models of the world in code.
- People naturally think of the world as made up of things.
- Programming languages have ways to represent things.
- JavaScript's primary way of representing a thing is an "Object".
- JavaScript objects let you describe things in any way you can imagine.

**Objects Contain Properties**

Objects enable us to encapsulate a bunch of data.
Here is an example of an object assigned to the variable **fido**:

```js
let fido = {
  species: "dog",
  color: "brown",
  spayed: true,
  weight: 40,
  favoriteActivities: ["sleeping", "chasing squirrels"],
};
```

- Object properties are KEY and VALUE pairs
- The key is on the left and the value on the right; the two together are called a _property_. In the example above, `species` is the `key` and `dog` is the `value`
- JavaScript object keys are always strings. If the key has no spaces you can omit surrounding quotes.
- `let fido = {...}` is an assignment, setting the variable fido to point to the object we just defined

**Getting Object Properties**

You can get the properties of an object using either _dots_ or _brackets_. Given the fido object declared in the example above:
`console.log(fido.species)` and `console.log(fido["species"])` will return the same result

**Dots vs Brackets**

Dots are prettier than square brackets, but less versatile. Some keys simply cannot be represented using dot notation, and trying to use them causes syntax errors.

The bracket [] syntax is less common but covers all uses (e.g., if the key contains spaces, or is a variable).

Brackets will recognize strings while dots will NOT recognize strings.

If you get an error when setting a property, revert to brackets, which are more reliable:

## Objects can be within objects

You can nest as many objects as you want.

## Reading & Homework

- Complete the "Guess The Number" project **(DUE: Thursday, 4/8)** If you want an extra challenge, take a look at the icebox challenges copied below.
- If you haven't already, finish reading [Eloquent JavaScript Chapter-4: Data Structures](https://eloquentjavascript.net/04_data.html)

## Guess The Number Ice Box Challenges

**Play it again!**

When the game finishes, instead of exiting, it should ask you if you want to play again. If you say "yes" it should restart the game from the beginning, otherwise it exits.

**How many tries?**

When the game finishes modify the victory message so it tells the user how many guesses it took for the computer to guess the correct number.

**Combine the games**

Modify the program in `index.js` so that the user can choose whether to play the normal game, or the reverse game when the program is started with `node index.js`
