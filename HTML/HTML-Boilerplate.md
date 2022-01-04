# HTML Boilerplate
All HTML documents have the same basic structure or boilerplate that needs to be in place before anything useful can be done.

## Creating a HTML Files
Let's demonstrate.

Create a new folder on your computer and name it `html-boilerplate`. Within that folder create a new file and name it `index.html`.

To let the computer know we want to create an *HTML* file, we need to append the filename with the `.html` extension as we have done when creating the `index.html` file. It is worth noting that we named our *HTML* file index. We should always name the *HTML* file that will contain the homepage of our websites `index.html`. This is because web servers will by default look for an `index.html` page when users land on our websites - and not having one will cause big problems.

## The DOCTYPE
Every HTML page starts with a doctype declaration. The doctype’s purpose is to tell the browser what version of HTML it should use to render the document. The latest version of HTML is HTML5, and the doctype for that version is simply `<!DOCTYPE html>`.

Open the `index.html` file created earlier in your text editor and add `<!DOCTYPE html> `to the very first line.

## HTML Element

After we declare the doctype, we need to provide an `<html>` element. This is what’s known as the root element of the document, meaning that every other element in the document will be a descendant of it.

This becomes more important later on when we learn about manipulating *HTML* with JavaScript. For now, just know that the *HTML* element should be included on every *HTML* document.

Back in the `index.html` lets add the `<html>` element by typing out its opening and closing tag
```HTML
<!DOCTYPE html>
<html>
</html>
```
## Head Element
The <head> element is where we put important meta-information about our webpages, and stuff required for our webpages to render correctly in the browser. Inside the <head>, we should not use any element that displays content on the webpage.

### Title Element
The title element is used to give webpages a human-readable title which is displayed in our webpage’s browser tab.
```HTML
<title>My First Webpage</title>
```

### The Charset Meta Element
Another important element we should always have in the head element is the meta tag for the charset encoding of the webpage:
```HTML
<meta charset="utf-8">.
```
Setting the encoding is very important because it ensures that the webpage will display special symbols and characters from different languages correctly in the browser.

## Body Element
The final element needed to complete the HTML boilerplate is the <body> element. This is where all the content that will be displayed to users will go - the text, images, lists, links, and so on.

## Viewing HTML Files in the Browser
There are a couple of different options:
- You can drag and drop an HTML file from your text editor into the address bar of your favorite browser.
- You can find the HTML file in your file system and then double click it. This will open up the file in the default browser your system uses.
- You can use the terminal to open the file in your browser.
  - **Ubuntu** - Navigate to the directory containing the file and use firefox `index.html` or google-chrome index.html

## VSCODE Shortcut
VSCode has a built-in shortcut you can use for generating all the boilerplate in one go. Please note that this shortcut only works while editing a file with the’.html’ extension or a text file with the HTML language already selected. To trigger the shortcut, delete everything in the index.html file and just enter ! on the first line. This will bring up a couple of options. Press the enter key to choose the first one, and voila, you should have all the boilerplate populated for you.
