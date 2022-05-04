# Session-17

Tonight we learned about the **DOM** and how we can manipulate the DOM with **DOM Scripting**.

#### Intro to the DOM

- stands for Document Object Model
  - "Document" = HTML page
    - also works for XML
  - "Object Model" = way of describing page elements
    - tags, attributes, styles, text, etc.
- Mostly standard
  - but there are some browser differences
- Core DOM objects

  - Node, Element, Text, Comment, Attr

  #### The BOM (Browser Object Model)

- Global window variable with helpful properties:
  - window.location
  - window.navigator
  - window.history
  - window.screen
  - window.frames
  - window.document -- _hey, look! it's the DOM_
  - methods too
  - open(), close()
  - moveTo(), sizeTo()
  - alert(), prompt(), confirm()
  - setTimeout(), setInterval()

#### window vs. document

- The **document** is the page and the content on it.
- The **window** is the stuff around the page (the things associated with the browser(e.g. cookies, url, etc.))

#### Locating HTML Elements

- **the hard way**

  - traverse the document tree using DOM Node methods

- **the somewhat easier way**

  - `document.getElementsByTagName('p')[0]`

- **the easy way**
  - `document.getElementById('article')`

#### Adding HTML in a programmatic way with JavaScript

```js
let target = document.getElementById("someElement");

let paragraph = document.createElement("p");
paragraph.textContent =
  "I’ve seen things you people wouldn’t believe. Attack ships on fire off the shoulder of Orion. I watched C-beams glitter in the dark near the Tannhauser gate. All those moments will be lost in time, like tears in rain.";

target.appendChild(paragraph);
```

**By assigning values to variables** we are able to further manipulate them in dynamic ways.

#### Events

When a user does something (e.g. click on a button), it generates an _event_

- **the target** is the element that was affected
- **the event** is an object describing the details
- **the listener** is a function you wrote
  - **"listener"** is just another name for **"callback"** (for events)
    also called "handler"

#### Many Event Types

- **Mouse**

  - mousedown, mouseup, click
  - mouseover, dblclick
  - and many more. There are a ton of mouse events. A ridiculous number really.

- **Keyboard**

  - keydown, keypress, keyup

- **Window**

  - load, unload, beforeunload
  - ready (jQuery only)
  - abort, error
  - resize, scroll, contextmenu

- **Form**

  - focus, blur
  - change, select
  - submit, reset

#### DOM Scripting

**"Scripting"** is a term used when you're writing programs that don't do much on their own; instead scripts usually use other, more advanced programs, or are embedded within them.

**"DOM Scripting"** means using JavaScript to manipulate the DOM (page elements and contents) inside a web page, either during page load, or in response to user events, like clicking a button or selecting text.

#### Scripts as Attributes

Below is an example of the _simplest_, but certainly **NOT the best**

```js
<button name="button" onclick="alert('here in the Dom')">
  tinker
</button>
```

#### A Script Tag (without src)

**Without a src attribute**, a script tag defines a script and _immediately executes_ its code. Take a look at this example below.

```js
<script>let message = "Shazam!" alert(message)</script>
```

#### A Script Tag with src

**With a src attribute**, it loads code from a separate file, and immediately executes it:

```js
<script src="tictactoe.js"></script>
```

- This code expects a file named `tictactoe.js` to exist on the server in the same directory as the HTML file.

- The script tag may appear in the head or in the body. **Scripts are executed in top-to-bottom order.**

HINT: **to be sure that your code executes after the page has been fully loaded**, put your `<script>` tags at the bottom of the `<body>` section.

### The document

- In a DOM script, **the current page is always available via the global variable named `document`.**

- When we refer to `document` we are referring to the current page that you are on. For example:

`document.URL` => URL of the current page, as a string

**document** - (with lowercase d) global instance accessible anywhere. It's an object!

**Document** - (with uppercase D) creates a brand new instance of the document

#### Finding an Element by ID

If an element has an id attribute, you can get a pointer to that element with a single line of code:

```js
let element = document.getElementById(id);
```

Once you have a pointer to that element, you can manipulate it further. You can also log it to the console for further inspection using:

```js
console.log(element);
```

[MDN: Document.getElementById()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById)

#### Finding an Element by CSS Selector

```js
let element = document.querySelector("main div.preview > p");
```

This returns the first Element within the document that matches the specified selector (in this case, the first `<p>` that is a direct child of any `<div class='preview'>` that is in the `main` section).

#### Using an Element

Once you find an element, you can start using it.

```js
let header = document.getElementById("header");
let text = header.textContent;
```

When you are targeting an element, use a variable name that's either the same or very similar.

#### Event Listeners

[MDN: Event Listeners](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)

## Reading & Homework

- [click-counter](https://replit.com/@Upright-JSI-Mar-2022/click-counter)
- [dom-manipulation](https://replit.com/@Upright-JSI-Mar-2022/dom-manipulation-practice#index.html)
- [mission-countdown](https://replit.com/@Upright-JSI-Mar-2022/mission-countdown-timer#index.html)
- [hello-frenemy](https://replit.com/@Upright-JSI-Mar-2022/hello-frenemy-www)
- [Passing-data](https://replit.com/@Upright-JSI-Mar-2022/passing-data#index.html)
