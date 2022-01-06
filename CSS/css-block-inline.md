# Block and Inline
The MDN box model article linked in the previous lesson mentions that different display types have subtly different box models, and that you can change how a box is calculated by changing the display property.

## Block vs Inline
Most of the elements that you have learned about so far are block elements.

By default, block elements will appear on the page stacked atop each other, each new element starting on a new line.

Inline elements, however, do not start on a new line. They appear in line with whatever elements they are placed beside.

Inline-block elements behave like inline elements, but with block-style padding and margin.

Inline-block is a useful tool to know about, but in practice you’ll probably end up reaching for flexbox more often if you’re trying to line up a bunch of boxes. Flexbox will be covered in depth in the next lesson.

## Divs and Spans
Div’s and spans, on the other hand, give no particular meaning to their content. They are just generic boxes that can contain anything.

Another use case we will face regularly is grouping related elements under one parent element to position them on the page correctly. Divs and spans provide us with the ability to do this.

Div is a block-level element by default. It is commonly used as a container element to group other elements. Divs allows us to divide the page into different blocks and apply styling to those blocks.

Span is an inline-level element by default. It is commonly used to group text content and inline HTML elements so we can apply styling to them.

### Resources
- [W3](https://www.w3schools.com/html/html_blocks.asp)
- [MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow)
- [DO](https://www.digitalocean.com/community/tutorials/css-display-inline-vs-inline-block)
