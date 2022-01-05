# CSS-Foundation
The next step is to make that structure look good with some style, which is exactly what CSS is for.

## Basic Syntax
These rules are made up of a selector (more on these in a bit) and a semi-colon separated list of declarations, with each of those declarations being made up of a property:value pair.

Example:
```CSS
div.bold-text{ // <- selector
    font-weight: 700; <- (property: value);
}
```
A `<div>` is one of the basic HTML elements. It is simply an empty container.

## Selectors
Selectors simply refer to the HTML elements to which CSS rules apply; they’re what is actually being “selected” for each rule.
### Universal Selector
The universal selector will select elements of any type, hence the name “universal”, and the syntax for it is a simple asterisk.
```CSS
* {
  color: purple;
}
```
### Type Selectors
A type selector (or element selector) will select all elements of the given element type, and the syntax is just the name of the element.
```CSS
div {
  color: white;
}
```
### Class Selectors
Class selectors will select all elements with the given class, which is just an attribute you place on an HTML element. Here’s how you add a class to an HTML tag and select it in CSS:
```HTML
<!-- index.html -->

<div class="alert-text">
  Please agree to our terms of service.
</div>
```
```CSS
/* styles.css */

.alert-text {
  color: red;
}
```
Note the syntax for class selectors: a period immediately followed by the case-sensitive value of the class attribute. Classes aren’t required to be unique, so you can use the same class on as many elements as you want.
### ID Selectors
ID selectors are similar to class selectors. They select an element with the given ID, which is another attribute you place on an HTML element:
```HTML
<div id="title">My Awesome 90's Page</div>
```
```CSS

#title {
  background-color: red;
}
```
Instead of a period, we use a hashtag immediately followed by the case-sensitive value of the ID attribute.

The major difference between classes and IDs is that an element can only have one ID. An ID cannot be repeated on a single page, and the ID attribute should not contain any whitespace at all.
### Grouping Selector
To cut down on the repetition, we can group these two selectors together as a comma-separated list:
```CSS
.read,
.unread {
  color: white;
  background-color: black;
}

.read {
  /* several unique declarations */
}

.unread {
  /* several unique declarations */
}
```
Reduces repetition of declarations and makes it easier to edit either the color or background-color for both classes at once.
### Chaining Selectors
Another way to use selectors is to chain them as a list without any separation.
```HTML
<div>
  <div class="subsection header">Latest Posts</div>
  <p class="subsection preview">This is where a preview for a post might go.</p>
</div>
```
We have two elements with the `subsection` class that have some sort of unique styles, but what if we only want to apply a separate rule to the element that also has header as a second class? Well, we could chain the two class selectors together in our CSS like so:
```CSS
.subsection.header {
  color: red;
}
```
