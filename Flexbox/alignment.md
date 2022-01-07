# Alignment
Adding `flex: 1` to .item makes each of the items grow to fill the available space, but what if we wanted them to stay the same width, but distribute themselves differently inside the container? We can do this!

Remove `flex: 1` from .item and add `justify-content: space-between` to .container.

`justify-content` aligns items across the main axis.

To change the placement of items along the cross axis use `align-items`

Because `justify-content` and `align-items` are based on the main and cross axis of your container, their behavior changes when you change the `flex-direction` of a `flex-container`.

## Gap
One more very useful feature of flex is the `gap` property. Setting `gap` on a flex container simply adds a specified space between flex items, very similar to adding a margin to the items themselves.
