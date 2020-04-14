# Other important HTML Tags

Here you will find examples of how to write these important and common HTML tags.

## Images

```html
<img src="images/your-image.png" alt="Test image">
```
Attributes:

* `src` url of your image
* `alt` alternative text for accesibility or a description for when the image can't be loaded

## Headings

Some texts can be specified as section headings. There are different sizes and importance for each one. They're from 1-6.

```html
<h1>My main title</h1>
<h2>My top level heading</h2>
<h3>My subheading</h3>
<h4>My sub-subheading</h4>
<h5>My sub-sub-subheading</h5>
<h6>My sub-sub-sub-subheading</h6>
```

## Paragraphs

They're good to group text and for regular content text.

```html
<p>This is a single paragraph</p>
```

## Lists

Grouping items are very common in internet, like menu items, text options, and to specify multiple topics. They're good for concise explanations.

There are unsorted lists:

```html
<ul>
  <li>technologists</li>
  <li>thinkers</li>
  <li>builders</li>
</ul>
```

Ordered lists in which the numbers are important.

```html
<ol>
  <li>this goes first</li>
  <li>the second one goes here</li>
  <li>and the third option appears here</li>
</ol>
```

## Links

Links are very important — they are what makes the web a web! To add a link, we need to use the "anchor" tag `<a>`.

```html
<a href="https://pushdev.co">Push Dev website</a>
```

Attributes:
* `href`: hypertext reference, it means the url we want to go to.
* `target`: tells the browser where the linked document should be loaded. By default uses `_self`
which means, the same window. `_blank` loads the page in a new window. Other options are `_parent` and `_top`.

## Exercise

1. Inside your fork `html-tutorial` repo, under the `2-other-html-tags` folder, create a file named `tags.html` Don't forget to include the `.html` extension
2. Inside of it, create a web page for your Curriculum it must include images (your photo), headings (your name, main cv sections), paragraphs (your resume), lists (skills) and anchors(websites you like the most).
3. commit your changes
4. Push the changes to your local copy of the repo.
