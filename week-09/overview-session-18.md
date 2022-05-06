# Session-18

Tonight we practiced **DOM scripting**

#### Finding many elements

In addition to getting a single element by its `id` or a CSS selector, you can also ask the document to give all elements that match a certain criterion.

**by CSS Class name**:

```js
let elements = document.getElementsByClassName("profile-picture");
```

**by Element name**:

```js
let elements = document.getElementsByTagName("h2");
```

**by CSS Selector expression**:

```js
let elements = document.querySelectorAll("h2.preview > p");
```


#### Event Handler Functions

In JavaScript, **event handlers** are **callback functions**.
- [MDN:EventTarget.addEventListener()](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)

#### Event Parameters

**An event handler function can optionally accept a parameter**

- This parameter is typically called `event` (or `evt` or even just `e`).
  - This `event` parameter holds **lots of information about the thing that just happened.**

An event object has many properties but **the most important one is** `event.target`, which points to the element where the action took place.

For instance, for a click event, `event.target` contains a pointer to the element that was clicked.

### Event Bubbling & Capture

- Events are created by their elements
- After creation they move up the chain by default
- This behavior can be changed by using `event.stopPropagation()` in the listener
- As Josh Burke mentioned in class, event bubbling can be a behavior that you want to enact for a particular reason, but often times you WON'T want it to bubble. Knowing how to prevent this default behavior is super useful!

#### Event Listeners

**Event Listeners** are a special type of function in JavaScript that **waits for a specified event**, and then **calls a callback function** after that event has been triggered.

#### Different Types of Events

There are many different types. You can check them out here:

- [MDN: Event Listeners](https://developer.mozilla.org/en-US/docs/Web/Events)

**What is a CSS Selector?**

- _A CSS Selector is the first part of a CSS rule._
- [MDN: What is a selector](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors#what_is_a_selector)

```css
h1 {
  background-color: purple;
}
h3 {
  background-color: yellow;
}
```

## Homework 

- [click-counter](https://replit.com/@Upright-JSI-Mar-2022/click-counter#index.html)
- [mission-countdown](https://replit.com/@Upright-JSI-Mar-2022/mission-countdown-timer#index.html)
- [hello-frenemy](https://replit.com/@Upright-JSI-Mar-2022/hello-frenemy-www)
- [Passing-data](https://replit.com/@Upright-JSI-Mar-2022/passing-data#index.html)
- [to-do-list](https://replit.com/@Upright-JSI-Mar-2022/dom-todo-list)
- [ticket-taker](https://replit.com/@Upright-JSI-Mar-2022/ticket-taker)
