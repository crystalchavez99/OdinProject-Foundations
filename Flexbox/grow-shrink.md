# Growing and Shrinking
Let’s look a little closer at what actually happened when you put flex: 1 on those flex items in the last lesson.

## Flex shorthand
The flex declaration is actually a shorthand for 3 properties that you can set on a flex item. These properties affect how flex items size themselves within their container.

In this case, `flex` is actually a shorthand for `flex-grow`, `flex-shrink` and `flex-basis`.
```CSS
div{
    flex: 0 1 0%;
}
```
The default value of the `flex` property is shown in the above screenshot: `flex-grow: 0`, `flex-shrink: 1`, `flex-basis: 0%`.

### flex-grow
Expects a single number as its value, and that number is used as the flex-item’s “growth factor”.

 When we applied `flex: 1` to every div inside our container, we were telling every div to grow the same amount. If we instead add `flex: 2` to just one of the divs, then that div would grow to 2x the size of the others.

 ### flex-shrink
 `flex-shrink` is similar to `flex-grow`, but sets the “shrink factor” of a flex item. `flex-shrink` only ends up being applied if the size of all flex items is larger than their parent container.

The default shrink factor is `flex-shrink: 1`, which means all items will shrink evenly. If you do not want an item to shrink then you can specify `flex-shrink: 0`;. You can also specify higher numbers to make certain items shrink at a higher rate than normal.

### flex-basis
`flex-basis` simply sets the initial size of a flex item, so any sort of `flex-growing` or `flex-shrinking` starts from that baseline size.

Using auto as a `flex-basis` tells the item to check for a width declaration (`width: 250px`).
