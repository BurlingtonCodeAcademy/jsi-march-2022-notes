# Session-19

Tonight we learned more about **Event Listeners** and we were introduced to the final project: [Pixel Art Grid Editor Project](https://classroom.github.com/assignment-invitations/4ecfcd12b0b45dceb081b0d51ead9f69) (This is **due: Tuesday, 5/17 by 6pm**).

### Event Listeners

**The Structure of the Event Listener in Javascript**

```js
const element = document.getElementById('ID')
element.addEventListener('click', function(event))
```

- `document.getElementByID('ID')` is the DOM Query
- `element` is the HTML Element
- `addEventListener()` sets up an event listener
- `click` is the type of event to listen for
- `function()` is the callback function
- `(event)` note that by default, the even that triggers the callback is passed as the first argument to the function

#### More about the addEventListener

- Method on HTML elements
- Takes two arguments
  - The first argument is a string that represents the event you're listening for
  - The second is a callback function to execute the desired action
- The callback can be defined in-line, or elsewhere in the code.

#### Adding Fonts from Google Fonts

There are a couple ways to do this. See below for an example of one way that we practiced in class today:

1. Head on over to [google fonts](https://fonts.google.com/) and select a font you like
2. In the panel on the right side of the page, toggle to the **@import url** option
3. Copy the code that lives within the `style`. It starts with **@import** and should look like this:

```css
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@500&family=Share+Tech+Mono&display=swap");
```
4. Then, paste that into top of your CSS file.

4. Next, copy the **CSS rules to specify families** and paste them in the body tag of your CSS file (this will ensure that the font family extends to all of your text associated with that particular style sheet). Example below:

```css
body {
  font-family: "Roboto", sans-serif;
  font-family: "Share Tech Mono", monospace;
}
```

## Reading & Homework

- **We are collecting your questions!** Share your question with us in [this google form](https://docs.google.com/forms/d/e/1FAIpQLScJHv-nSaUk-gIoXXZQWRlUfHsCj6tGHinvLDS2e4Bq1pCbMg/viewform). We will be discuss responses in class on Thursday.

- [Pixel Art Grid Editor Project](https://classroom.github.com/assignment-invitations/4ecfcd12b0b45dceb081b0d51ead9f69) This is **due: Tuesday, 5/17 by 6pm**

### Labs 

**For more practice with event listeners**:
- [LAB: Pythagorus](https://replit.com/@Upright-JSI-Mar-2022/Pythag-1#.lesson/instructions.md)

- Here's GJ's code for the [Template lab](https://github.com/gjcritchlow21/newTemplate)
