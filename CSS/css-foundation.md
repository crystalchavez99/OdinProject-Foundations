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
### Descendant Combinator
Combinators allow us to combine multiple selectors differently than grouping or chaining them, as they show a relationship between the selectors. There are four types of combinators in total, but for right now we’re going to only show you the descendant combinator, which is represented in CSS by a single space between selectors. A descendant combinator will only cause elements that match the last selector to be selected if they also have an ancestor (parent, grandparent, etc) that matches the previous selector.
```HTML
<!-- index.html -->

<div class="ancestor"> <!-- A -->
  <div class="contents"> <!-- B -->
    <div class="contents"> <!-- C -->
    </div>
  </div>
</div>

<div class="contents"></div> <!-- D -->
```
```CSS
/* styles.css */

.ancestor .contents {
  /* some declarations */
}
```
## Properties to start with
### color and background-color
The `color` property sets an element’s text color, while `background-color` sets, well, the background color of an element.
Both of these properties can accept one of several kinds of values.

### Typography Basics and text-align
- `font-family` can be a single value or a comma-separated list of values that determine what font an element uses. Each font will fall into one of two categories, either a “font family name” like "Times New Roman" (we use quotes due to the whitespace between words) or “generic family name” like sans-serif (generic family names never use quotes).

This is why it’s best practice to include a list of values for this property, starting with the font you want to be used most and ending with a generic font family as a fallback, e.g. `font-family: "Times New Roman", sans-serif`;

- `font-size` will, as the property name suggests, set the size of the font.
- `font-weight` affects the boldness of text, assuming the font supports the specified weight. This value can be a keyword, e.g. `font-weight: bold`, or a number between 1 and 1000, e.g. `font-weight: 700` (the equivalent of bold). Usually the numeric values will be in increments of 100 up to 900, though this will depend on the font.
- `text-align` will align text horizontally within an element, and you can use the common keywords you may have come across in word processors as the value for this property, e.g. `text-align: center`
### Image Height and Width
Images aren’t the only elements that we can adjust the height and width on, but we want to focus on them specifically in this case.
By default, an `<img>` element’s height and width values will be the same as the actual image file’s height and width. If you wanted to adjust the size of the image without causing it to lose its proportions, you would use a value of “auto” for the height property and adjust the width value:
```CSS
img {
  height: auto;
  width: 500px;
}
```
## Cascade of CSS
Sometimes we may have rules that conflict with one another, and we end up with some unexpected results.
### Specificty
A CSS declaration that is more specific will take precedence over ones that are less specific.

There are other selectors that contribute to specificity, but we’re focusing only on the ones mentioned in this lesson:
1. ID
2. Class
3. Type
Specificity will only be taken into account when an element has multiple, conflicting declarations targeting it, sort of like a tie-breaker. **An ID selector will always beat any number of class selectors, a class selector will always beat any number of type selectors, and a type selector will always beat any number of anything less specific than it.**
### Inheritance
Inheritance refers to certain CSS properties that, when applied to an element, are inherited by that element’s descendants, even if we don’t explicitly write a rule for those descendants.

The exception to this is when directly targeting an element, as this always beats inheritance:
```HTML
<!-- index.html -->

<div id="parent">
  <div class="child"></div>
</div>
```
```CSS
/* styles.css */

#parent {
  color: red;
}

.child {
  color: blue
}
```
Despite the `parent` element having a higher specificity with an ID, the `child `element would have the `color: blue` style applied since that declaration directly targets it, while `color: red` from the parent is only inherited.
### Rule Order
Really simply, actually. Whichever rule was last defined is the winner.
```CSS
/* styles.css */

.alert {
  color: red;
}

.warning {
  color: yellow;
}
```
For an element that has both the `alert` and `warning` classes, the cascade would run through every other factor, including inheritance (none here) and specificity (neither rule is more specific than the other). Since the `.warning` rule was the last one defined, and no other factor was able to determine which rule to apply, it’s the one that gets applied to the element.

## Adding CSS to HTML
There are three methods to do so.
### External CSS
External CSS is the most common method you will come across, and it involves creating a separate file for the CSS and linking it inside of an HTML’s opening and closing `<head>`tags with a self-closing `<link>` element:
```HTML
<!-- index.html -->
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```
```CSS
/* styles.css */

div {
  color: white;
  background-color: black;
}

p {
  color: red;
}
```
First, we add a self-closing `<link>` element inside of the opening and closing `<head>` tags of the HTML file. The href attribute is the location of the CSS file, either an absolute URL or, what you’ll be utilizing, a URL relative to the location of the HTML file.

**Pros:**
1. It keeps our HTML and CSS separated, which results in the HTML file being smaller and makes things look cleaner.
2. We only need to edit the CSS in one place, which is especially handy for websites with multiple pages that all share similar styles.

### Internal CSS
Internal CSS (or embedded CSS) involves adding the CSS within the HTML file itself instead of creating a completely separate file. With the internal method, you place all of the rules inside of a pair of opening and closing `<style>` tags, which are then placed inside of the opening and closing `<head>` tags of your HTML file. Since the styles are being placed directly inside of the `<head>` tags, we no longer need a `<link> `element that the external method requires.
```HTML
<head>
  <style>
    div {
      color: white;
      background-color: black;
    }

    p {
      color: red;
    }
  </style>
</head>
<body>...</body>
```

### Inline CSS
Inline CSS makes it possible to add styles directly to HTML elements, though this method isn’t as recommended:
```HTML
<body>
  <div style="color: white; background-color: black;">...</div>
</body>
```
 Generally, though, this isn’t exactly a recommended way for adding CSS to HTML for a few reasons:
 - It can get pretty messy pretty quickly once you start adding a lot of declarations to a single element, causing your HTML file to become unnecessarily bloated.
 - If you want multiple elements to have the same style, you would have to copy + paste the same style to each individual element, causing lots of unnecessary repetition and more bloat.
 - Any inline CSS will override the other two methods, which can cause unexpected results. (While we won’t dive into it here, this can actually be taken advantage of).
