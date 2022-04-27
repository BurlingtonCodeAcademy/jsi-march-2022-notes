# Session-15

Tonight we learned more about styling with CSS.

### CSS

#### Linking to CSS

There are two ways to link your CSS file to your HTML

1. Linking them through the Link tag (See example below):

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Cat</title>
    <link href="styles/style.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <h1>My Cat Bob</h1>
    <p>My cat is named Bob. He is a lazy cat.</p>
  </body>
</html>
```

2.  Using `@import` 
- [MDN: @import](https://developer.mozilla.org/en-US/docs/Web/CSS/%40import) 
- The example below assumes that the .css file is at the same level directory as your index.html file

```html
<style type="text/css" media="screen">
  @import "my_special_css_file.css";
</style>
```

#### The Element Box Model

- Imagine every HTML element as a 'box'
- Every box consists of four different 'layers': Margin, Border, Padding, and Content
- Margins and padding help to position and align content inside an HTML element
- Padding and margins are transparent. Think of it as empty space
- Borders can be colored, or image-based. They can also be 'styled' (dashes, dots, etc.)

[MDN: Introduction to the CSS basic box model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)

#### The !Important Declaration

Using `!important` in a declaration **overrides all other declarations**

#### Style Override Precedence

The more specific selectors will override the less specific selectors.
See below for the order of specificity (**Note: the list below orders the selectors from most specific to less specific**):

1. !important
2. Inline CSS
3. ID Selectors
4. Class Selectors
5. Element Selectors

**If your CSS is doing something unexpected**, take a another look at your HTML and CSS to make sure you're using the hierarchy in the way you are intending.

#### CSS Layout: Inline vs. Block Level Elements

There are **two main display rules (or "levels") for HTML elements.**

- **Block level**
  - New line, full width
  - Block level elements can contain both block and inline elements.
- **Inline level**
  - Same line, width of content
  - Inline elements should only contain data, or other inline elements.

#### CSS Display Property

Elements are given a default display value based on their type - this is a CSS property that determines an element's layout, and how it interacts with other elements.

- `display: block;`
  - The element will take up the full width of the page
- `display: inline;`
  - The element will only take up the width of the content within the element.
- `display: inline-block;`
  - Acts as an inline element, but can be given a specific width and height.
- `display: none;`
  - The element will disappear, as will all its children, and its neighbors will be rendered as if it was never there.

[MDN: Display values](https://developer.mozilla.org/en-US/docs/Web/CSS/display)

#### Example of Block vs. Inline Elements

Inherent display properties of commonly-used HTML elements:

**Block Level Elements**
- div
- p
- table
- form
- ul, ol
- nav

**Inline Elements**
- span
- a
- i, em
- b, strong
- img
- button

#### Positioning

**Four commonly-used position properties in CSS**. These further help to position elements on a page.

1. **Relative**: Elements are relative to the flow of the HTML document.

    - Elements moved around with the properties top, left, right, bottom. top:20px; will move a relatively positioned element 20 pixels from its natural postioning.
    - "my children are positioned relative to me"

2. **Absolute**: This is positioned relative to its parent or ancestor (closest ancestor that is relatively positioned).

    - Any element that is positioned absolutely, will be placed (using the top/left/right/bottom CSS properties) specifically within the parent, irrespective of other sibling elements.
    - "I am positioned relative to my parent"

3. **Fixed**: Position an element is relation to its viewport (browser window).

4. **Static**: Same as relative, but cannot be moved with top/left/right/bottom. It is relative to the flow of the HTML document.

#### Wrapper DIVs

In order to make content layout work in CSS, you often need to introduce **wrapper divs**.
This helps us to organize our code _AND_ enables us to more effectively style components of our site in relation to each other.

#### Floats

Floats used to be the only way to achieve specific layouts using CSS, especially:

- stacking left-to-right or right-to-left
- forcing an element to be as wide as its contents, not as wide as its parent
- Float properties
  - `float: left;`
  - `float: right;`

Nowadays, the `float` property **should only be used for wrapping text around images**, which was its original purpose - gone are the days of CSS layout using floats.

[Float Explanation video](https://youtu.be/xara4Z1b18I)

When applying styles to your website, think about your site in a 3D manner. It might help you consider how you want to display and hide particular components.

#### Flexbox

Flexbox is a flexible tool that helps us create responsive and compelling layouts! Flexbox helps to accomplish the following:

- Horizontal or vertical alignment of elements
- Arrangement (order) of elements
- Space distribution between elements
- Space distribution around elements

**Here's an example of how to create a flexbox with `flex-direction: row` in CSS:**

```css
.container {
  display: flex;
  flex-direction: row;
}
```

**Here's an example of how to create a flexbox with `flex-direction: column` in CSS:**

```css
.container {
  display: flex;
  flex-direction: column;
}
```

**Here's an example of how to reverse the content in a flexbox:**

```css
#container {
  display: flex;
  flex-direction: column-reverse;
}
```

**Note:** If a flex-direction is not identified, the flexbox will default to `row`.

**Here's an example of the `order` property, which enables you to change the order in which items are displayed**:

```css
.firstItem {
  display: flex;
  order: 1;
}

.secondItem {
  display: flex;
  order: 2;
}
```

**Learn more flexbox properties here:** [CSS Tricks: A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## Homework

**Replit Labs**

- [Hello HTML](https://replit.com/@Upright-JSI-Mar-2022/hello-html#index.html)
- [Markup Recipe](https://replit.com/@Upright-JSI-Mar-2022/markup-recipe#index.html)
- [Hello Styles](https://replit.com/@Upright-JSI-Mar-2022/hello-styles#index.html)

**Interactive Games**

- [Flexbox Froggy](https://flexboxfroggy.com/)
- [CSS Diner](https://flukeout.github.io/)

### More practice with flexbox(if you have time)

- [Codepen: Flexbox Display](https://codepen.io/burlingtoncodeacademy/pen/NWaqYmE)
- [Codepen: Simple Flex Grid](https://codepen.io/burlingtoncodeacademy/pen/vYeOjdz)
- [Codepen: Flexbox Playground](https://codepen.io/burlingtoncodeacademy/pen/wvKRojY)
