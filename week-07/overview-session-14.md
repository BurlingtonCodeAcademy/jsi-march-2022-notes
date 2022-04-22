# Session-14

Tonight we learned more about **HTML** and **CSS**!

### HTML

#### Attributes 
Attributes further define HTML elements and their purpose. For example, an image tag may have the following attributes:

```js
<img src="/images/cat-pic.jpg" title="Cat Picture" alt="Picture of a fuzzy cat">
```

- `src` defines where the image file is located.
- `alt` is alternative text to be displayed if the image cannot be.
- Attributes are not always required. However in the example above, a source is needed for the image to be displayed.
- Others include `style` (for inline CSS), `title` (for hover-over tooltips), `href` (hyperlink reference)
- Attribute names should always be lowercase

#### Tables

- Tables are a way of structuring data into rows and columns.
- Tables are comprised 4 elements:
  - `<table>` => defines an HTML table
  - `<tr>` => table row
  - `<th>` => table height
  - `<td>` => table data

#### Lists

- Two main types of HTML lists: **ordered** and **unordered**.

- `<ul>` describes a **unordered list**. Each item in the list will be bulleted.

```js
<ul>
  <li>Pizza</li>
  <li>Pasta</li>
  <li>Bread</li>
</ul>
```

- `<ol>` describes an **ordered list**. Each item in the list will be numbered (top to bottom)

```js
<ol>
  <li>Pizza</li>
  <li>Pasta</li>
  <li>Bread</li>
</ol>
```

#### Comments are our friend in HTML!

- Commenting is important in any form of coding.
- Comments help both you and others to better understand the intent of the code.
- Especially helpful when reviewing large amounts of code.
- Comments in HTML are not read by browsers. They use the following syntax:
<!-- This is a comment! -->

#### Resources: Web Accessability

- [Quick wins for web accessibility](https://a11y.coffee/quick-wins/#2-missing-alt-text-for-images)
- [Web Accessibility in Mind](https://webaim.org/techniques/alttext/)
- [Web.dev: What is accessibility?](https://web.dev/what-is-accessibility/)

### CSS (Cascading Style Sheets)

- CSS, by itself, does nothing.
- Responsible for determining how your HTML looks
- CSS formats your webpage. Without it, there is only content, and no structure or styles.

#### Writing CSS

- _Can_ be written within HTML, but it's **best practice** to write CSS in an external style sheet

- Creating external style sheets prevents you from having to write code multiple times, and makes it easy to modify.

#### Styling with CSS

- Using CSS properties, you can modify the appearance of your HTML.
- This can done by targeting HTML elements.

**Example:**
Let's say we have the following HTML:

```js
<!DOCTYPE html>
<html>
  <head>
    <title>My Cat</title>
  </head>
  <body>
    <h1>My Cat Bob</h1>
    <p>My cat is named Bob. He is a lazy cat.</p>
  </body>
</html>

```

Below is an example of **CSS targeting the HTML elements** from the example above:

```css
h1 {
  color: red;
  font-size: 24px;
}

p {
  color: blue;
  font-size: 12px;
}
```

#### Adding styles to an HTML page
Common use-cases to add style to an HTML page include:

- `<h1 style="color: red; font-size: 32px;">` Inline
- `<link>` Tag to a CSS file
- `<style>` Tags with `@import` of a CSS file

#### Selectors and Properties

- CSS is constructed of selectors and properties.
- Selectors determine where the styles are applied.
- Properties determine what those styles are.
- CSS begins with a selector, followed by curly braces.
- Declare your styles inside the curly braces.

```css
p {
  color: white;  
  background-color: navy; 
  text-align: center; 
  font-size: 24px;
  border: 5px grey solid; 
}
```

^ In the above example, `p` is the selector with the styles declared within the curly braces.

#### Compound Selectors - Example #1
Selectors can target elements nested within other elements:

```css
p img {
  max-width: 320px;
  height: auto;
}
```

#### Compound Selectors - Example #2
Selectors can target specific elements with a class:

```css
h1 .title {
  display: block;
  margin: 0, auto;
  padding-top: 1em;
}
```

^ In the example above, we are applying the styling to any element with the `class="title"`

[CSS Tricks: The Difference between ID and Class](https://css-tricks.com/the-difference-between-id-and-class/#:~:text=ID's%20have%20special%20browser%20functionality,hash%20value%E2%80%9D%20in%20the%20URL.)

#### Compound Selectors - Example #3
Selectors can target specific elements with several layers of nesting

```css
main .introduction > p {
  background-color: lightgray;
  margin: 10px auto;
}
```

_The above example says:_ "apply these styles to all `p`s that are direct children of a `div` of class `introduction` inside the `main` section"

#### Psuedo-Class Selectors
You can target the state of an element using psuedo-class selectors

```css
a:hover {
  background-color: red;
}

a:active {
  background-color: green;
}
```

[Full List on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

[MDN Psuedo-Class Tutorial](https://developer.mozilla.org/en-US/docs/learn/css/building_blocks/selectors/pseudo-classes_and_pseudo-elements)

## Reading & Homework

Continue working on **Zorkington! Due: Tuesday, 4/26**
