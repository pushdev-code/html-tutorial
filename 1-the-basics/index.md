# HTML basics

*HTML* (HyperText Markup Language) is the language in which most websites are written. It defines the meaning and structure of web content. It is used to describe the content of a document so it can be read by browsers in the internet or offline.

* `Hypertext`: How web pages are connected to one another, either within a single website or between websites? By using links. These are a fundamental aspect of the Web. Content linking is the building block of Internet's purpose: sharing information.
* `Markup`: to annotate text, images, and other content for display in a Web browser. HTML markup includes special "elements" called `tags`, such as ```<head>, <title>, <body>```, and many others.
* `Tags`: HTML element surrounded by "`<`" and "`>`".

## is HTML a programming language?

HTML is a way of adding context and structure to text, therefore some people don't consider it a programming language, because _"a programming language is a notation for writing programs, which are specifications of a computation or algorithm"_ When you code HTML, you're denoting a piece of data, You haven’t “instructed” the browser to execute a task.

## How to write HTML Tags

![HTML Tag Structure](https://mdn.mozillademos.org/files/9347/grumpy-cat-small.png)

The main parts of our element are as follows:

* `The opening tag`: This consists of the name of the element (in this case, p), wrapped in opening and closing angle brackets. This states where the element begins or starts to take effect — in this case where the paragraph begins.
* `The closing tag`: This is the same as the opening tag, except that it includes a forward slash before the element name. This states where the element ends — in this case where the paragraph ends. Failing to add a closing tag is one of the standard beginner errors and can lead to strange results.
* `The content`: This is the content of the element, which in this case, is just text.
* `The element`: The opening tag, the closing tag and the content together comprise the element.

Besides from the previous parts, Tags can have `attributes` that contain more information about the content, they usually won't be visible in the document:

![HTML Tag attributes](https://mdn.mozillademos.org/files/9345/grumpy-cat-attribute-small.png)

An `attribute` should always have the following:

* A space between it and the element name (or the previous attribute, if the element already has one or more attributes).
* The attribute name followed by an equal sign.
* The attribute value wrapped by opening and closing quotation marks.

HTML tag can contain other tags and this called Nesting.

```html
<p>My cat is <strong>very</strong> grumpy.</p>
```

Some HTML tags like `<img>` can be empty and not contain other tags. They usually are self enclosed (They don't need the closing tag) as well:

```html
<img src="images/firefox-icon.png" alt="My test image">
```

Source: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics


## Basic HTML file structure

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My HTML page</title>
  </head>
  <body>
    <p>This is my HTML page</p>
  </body>
</html>
```

* It should always start with `<!DOCTYPE html>`
* Like Human body it should have a `<head>` and `<body>`. What's in the `<head>` it won't be visible to the user, but it will what's inside the `<body>`.
* `<meta>` is used to define the character encoding for the HTML document.
* Without a `<title>`, users will never know what's your page about.
* `<p>` is used to display paragraphs.
* Most of content tags should be closed with a backslash `</head>`,`</body>`,`</html>`.

## Exercise

Create an HTML document and see it live in your browser.

1. Inside your fork `html-tutorial` repo, under the `1-the-basics` folder, create a file named `basic.html` Don't forget to include the `.html` extension
2. Copy the contents of the HTML file structure from above into the html file
3. Put your name inside the `<title>` and in the `<p>` tags
4. Save your changes and double click your file
5. Your file should be visible in the browser and look similar to this image:
6. Push the changes to your local copy of the repo.

![HTML structure exercise](https://user-images.githubusercontent.com/61557537/79169746-d89c6400-7db2-11ea-80b4-940f70d8d235.png)
