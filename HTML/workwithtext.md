# Paragraphs
When the browser encounters new lines like this in your HTML, it will compress them down into one single space. The result of this compression is that all of the text is clumped together into one long line.

If we want to create paragraphs in HTML, we need to use the paragraph element, which will add a newline after each of our paragraphs. A paragraph element is defined by wrapping text content with a `<p>` tag.

# Headings
Headings are different from other HTML text elements: they are displayed larger and bolder than other text to signify that they are headings.

There are 6 different levels of headings starting from `<h1>` to `<h6>`. The number within a heading tag represents that heading’s level. `h1` is the most important and is larger than the other headings, and `h6` is the lowest level and therefore the smallest of the headings.
```HTML
 <head>
  </head>
  <body>
    <h1>This is a heading 1</h1>
    <h2>This is a heading 2</h2>
    <h3>This is a heading 3</h3>
    <h4>This is a heading 4</h4>
    <h5>This is a heading 5</h5>
    <h6>This is a heading 6</h6>
  </body>
 </html>
 ```
 Using the correct level of heading is important as levels provide a hierarchy to the content. An h1 heading should always be used for the heading of the overall page, and the lower level headings should be used as the headings for content in smaller sections of the page.

 # Strong Element
 The `<strong>` element makes text bold. It also semantically marks text as important; this affects tools, like screen readers, that users with visual impairments will rely on to use your website.

 `<strong>Lorem ipsum dolor</strong>` === <strong>Lorem ipsum dolor</strong>

 # Em Element
 The em element makes text italic. It also semantically places emphasis on the text, which again affects things like screen readers. To define an emphasised element we wrap text content in a `<em>` tag.

 `<em>Some emphasized text</em>` === <em>Some emphasized text</em>

# Nesting and Indentation
You may have noticed that in all the examples in this lesson we indent any elements that are within other elements. This is known as nesting elements.

When we nest elements within other elements, we create a parent and child relationship between them. The nested elements are the children and the element they are nested within is the parent.

Just as in human relationships, HTML parent elements can have many children. Elements at the same level of nesting are considered to be siblings.

We use indentation to make the level of nesting clear and readable for ourselves and other developers who will work with our HTML in the future. It is recommended to indent any child elements by two spaces.

# HMTL Comments
HTML comments are not visible to the browser; they allow us to comment on our code so that other developers or our future selves can read them and get some context about something that might not be clear in the code.

Writing an HTML comment is simple: we just put `<!--` and` -->` at either end of the comment.
