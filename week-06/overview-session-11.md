# Session-11

Tonight we discussed `Objects, Methods, and Classes` as well as `Array Properties and Methods`

We reviewed what a `class` is and how we can create new instances of a particular `class`. Remember the "cookie analogy":

- A class = cookie cutter
- An instance = cookie
- An instance's data = icing and sprinkles

## Factory Functions

A `Factory Function`constructs objects for you, based on your specifications. See example below:

```js
class Circle {
  constructor(radius) {
    if (radius <= 0) {
      throw "Error must be positive.";
    }
    this.radius = radius;
  }
}

let someDiameter = 20;

function circleFromDiameter(diameter) {
  return new Circle(diameter / 2);
}

let myCircle = circleFromDiameter(20);
console.log(myCircle.radius); // 10;
```

## Factory Methods

Factory Methods are for your convenience.
The factory method works exactly the same way as the factory function, but...

- the `factory function` is in the global namespace
- the `factory method` is in the class namespace so it's more clear that it is meant to create one of this class of objects

**Remember**: A `method` is just a `function` attached to an `object`.

## Array Properties and Methods

Every JavaScript Array is also a JavaScript Object.

That means that arrays have properties and methods like other objects.

Examples:

```js
let myArray = ["apple", "cherry", "pineapple"];
```

- `myArray.length` is a property that is the number of elements in the array
- `myArray.reverse()` is a method that reverses the ordering of all elements in the array

[MDN: Array Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#instance_methods)

**Iterators are Callback Functions**

A callback function is _any function_ passed to another function as an argument. Callback functions are then called by the outer function in order to do some work.

```js
function printDate(value) {
  console.log("The date is: " + value);
}

function currentDate(callback) {
  let now = Date().toLocaleString();
  // calling the inner callback
  callback(now);
  // back in the outer function
  console.log("All Done!");
}

currentDate(printDate);
```

[MDN: Callback Function](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function)

**The `forEach()` Method**
- `forEach` works a lot like `for..of`, but passes each value to a callback function as an argument, one after another.

**The `find()` Method**
- `.find()` will find the first instance that matches the condition.

**The `filter()` Method**
- `.filter()` returns all matching values, in a _new array_.

**The `map()` Method**
- `.map()` returns a _new array_ whose elements correspond to the elements of the original array. See example below:

```js
let names = ["Alice", "Bob", "Charlie", "Carol", "David"];
function upperCase(word) {
  return word.toUpperCase();
}
// Creating a variable to hold the new array that is created with the .map() method
let loudNames = names.map(upperCase);

console.log(loudNames);
//=> [ 'ALICE', 'BOB', 'CHARLIE', 'CAROL', 'DAVID' ]
```

## Reading & Homework

Complete the following labs on replit:

- [reverse array](https://replit.com/team/Upright-JSI-Mar-2022/reverse-array)
- [shopping list arrays](https://replit.com/team/Upright-JSI-Mar-2022/shopping-list-arrays)
- [array includes](https://replit.com/team/Upright-JSI-Mar-2022/array-includes)
- [person object](https://replit.com/team/Upright-JSI-Mar-2022/person-object)
- [gpa calculator](https://replit.com/team/Upright-JSI-Mar-2022/gpa-calculator)
- [menu order](https://replit.com/team/Upright-JSI-Mar-2022/menu-order)

### Labs

Tonight we worked on the following labs in class:

- [cake constructor](https://replit.com/team/Upright-JSI-Mar-2022/templates/cake-factory)
- [ends with berry](https://replit.com/team/Upright-JSI-Mar-2022/templates/ends-with-berry)
- [find all berries](https://replit.com/team/Upright-JSI-Mar-2022/templates/find-all-berries)
- [titlelize string with map](https://replit.com/team/Upright-JSI-Mar-2022/templates/titleize-string-with-map)
