# Axes Intro
The most confusing thing about flexbox is that it can work either horizontally or vertically, and the way some rules work changes a bit depending on which direction you are working with.

The default direction for a flex container is horizontal, or `row`, but you can change the direction to vertical, or `column`. The direction can be specified in CSS like so:
```CSS
.flex-container {
  flex-direction: column;
}
```

## Axes
No matter which direction you’re using, you need to think of your flex-containers as having 2 axes: the `main axis` and the `cross axis`. It is the direction of these axes that changes when the `flex-direction` is changed.

In most circumstances, `flex-direction: row` puts the main axis horizontal (left-to-right), and column puts the main axis vertical (top-to-bottom).

One thing to note is that in this example, `flex-direction: column` would not work as expected if we used the shorthand `flex: 1`

The reason for this is that the flex shorthand expands `flex-basis` to 0, which means that all `flex-growing` and `flex-shrinking` would begin their calculations from 0. Empty divs by default have 0 height, so for our flex items to fill up the height of their container, they don’t actually need to have any height at all.

Another detail to notice: when we changed the `flex-direction` to `column`, `flex-basis` referred to `height` instead of `width`.
