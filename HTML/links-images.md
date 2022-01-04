# Links and Images

## Anchor Elements
To create a link in HTML, we use the anchor element. An anchor element is defined by wrapping the text or another HTML element we want to be a link with a `<a>` tag.

An anchor tag on its own won’t know where we want to link to. We have to tell it a destination to go to. We do this by using an HTML attribute.

An HTML attribute gives additional information to an HTML element and always goes in the element’s opening tag. An attribute is made up of two parts, a name, and a value. In our case, we need to add a href (hyperlink reference) attribute to the opening anchor tag. The value of the href attribute is the destination we want our link to go to.
```HTML
<a href="https://www.theodinproject.com/about">click me</a>
```
By default, any text wrapped with an anchor tag without a href attribute will look like plain text. If the href attribute is present, the browser will give the text a blue color and underline it to signify it is a link.

## Absolute and Relative Links
Generally, there are two kinds of links we will create:

1. Links to pages on other websites on the internet
2. Links to pages located on our own websites

### Absolute Links
Links to pages on other websites on the internet are called absolute links. A typical absolute link will be made up of the following parts: `protocol://domain/path`. An absolute link will always contain the protocol and domain of the destination.

### Relative Links
Links to other pages within our own website are called relative links. Relative links do not include the domain name, since it is another page on the same site, it assumes the domain name will be the same as the page we created the link on.

Relative links only include the file path to the other page, *relative* to the page you are creating the link on.
```HTML
<body>
  <h1>Homepage</h1>
	<a href="https://www.theodinproject.com/about">click me</a>

	<a href="pages/about.html">About</a>
</body>
```
Open the index file in a browser and click on the about link to make sure it is all wired together correctly. Clicking the link should go to the about page we just created.

This works because the index and about page are in the same directory. That means we can simply use the name of the about.html file about.html as the value of the href in the link.

In many cases, this will work just fine; however, you can still run into unexpected issues with this approach. Prepending ./ before the link will in most cases prevent such issues. By adding ./ you are specifying to your code that it should start looking for the file/directory relative to the current directory.

### Difference
 Relative links are directions from the room you are currently in (the bedroom) to another room (the kitchen). Absolute links, on the other hand, are directions to an entirely different house.

 ## Images
 To display an image in HTML we use the `<img>` element. Unlike the other elements we have encountered so far, the `<img>` element is empty. Which means it doesn’t have a closing tag.

Instead of wrapping content with an open and closing tag, it embeds an image into the page using a src attribute which tells the browser where the image file is located. The src attribute works much like the href attribute for anchor tags. It can embed an image using both absolute and relative paths.
```HTML
 <img src="https://www.theodinproject.com/mstile-310x310.png">
 ```

 ## Parent Directories

 What if we want to use the dog image in the about page? We would first have to go up one level out of the pages directory into its parent directory so we could then access the images directory.

 To go to the parent directory we need to use two dots in the relative filepath like this: `../`.
 ```HTML
 <img src="../images/dog.jpg">
 ```
 To break this down:

- First, we are going to the parent directory of the pages directory which is odin-links-and-images.
- Then, from the parent directory, we can go into the images directory.
- Finally, we can access the dog.jpg file.

## Alt Attribute
Besides the src attribute, every image element should also have an alt(alternative text) attribute.

The alt attribute is used to describe an image, it will be used in place of the image if it cannot be loaded. It is also used with screen readers to describe what the image is to visually impaired users
```HTML
 <img src="https://www.theodinproject.com/mstile-310x310.png" alt="The Odin Project Logo">
```
