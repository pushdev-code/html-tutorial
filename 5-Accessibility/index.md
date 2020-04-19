# Accessibility

Websites should be designed and developed in such a way that people with disabilities can use them. More specifically, people can: perceive, understand, contribute and navigate in your website without too much problem. Have you ever tried to a text-to-speech app, close your eyes and try to navigate your website or webapp?

One way to ensure accessibility is to use the correct Hypertext Markup Language elements for the correct purpose at all times, so semantic is not just for SEO and indexing purposes, but for make your content accessible.

__Don't__

```html
<div>Play video</div>
```

__Do__

```html
<button>Play video</button>
```

Here if you use the `<button>` tag, users will be able to navigate to your button using the `Tab` key and if your button is a form submit, they will be able to complete the action using the `Enter` key.

## Benefits of semantic markup

* __Easier to develop with__: you get some functionality for free, plus it is arguably easier to understand.
* __Better on mobile__: semantic HTML is arguably lighter in file size than non-semantic spaghetti code, and easier to make responsive.
* __Good for SEO__: search engines give more importance to keywords inside headings, links, etc., than keywords included in non-semantic <div>s, etc., so your documents will be more findable by customers.

## Accessibility in language

The HTML lang attribute is used to identify the language of text content on the web. This information helps search engines return language specific results, and it is also used by screen readers that switch language profiles to provide the correct accent and pronunciation.

__Don't__

```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <meta charset="utf-8">
    <title>Language page</title>
  </head>
  <body>
    <p>This page is written in English.</p>
    <p>Sauf pour ce qui est écrit en mauvais français.</p>
  </body>
</html>
```

__Do__

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <meta charset="utf-8">
    <title>Language page</title>
  </head>
  <body>
    <p>This page is written in English.</p>
    <p lang="fr">Sauf pour ce qui est écrit en mauvais français.</p>
  </body>
</html>
```

## Accessibility in text content

One of the best accessibility aids a screenreader user can have is a good content structure with headings, paragraphs, lists, etc.

__Don't__

```html
<font size="7">My heading</font>
<br><br>
This is the first section of my document.
<br><br>
I'll add another paragraph here too.
<br><br>
1. Here is
<br><br>
2. a list for
<br><br>
3. you to read
<br><br>
<font size="5">My subheading</font>
<br><br>
This is the first subsection of my document. I'd love people to be able to find this content!
<br><br>
<font size="5">My 2nd subheading</font>
<br><br>
This is the second subsection of my content. I think is more interesting than the last one.
```

__Do__:

```html
<h1>My heading</h1>

<p>This is the first section of my document.</p>

<p>I'll add another paragraph here too.</p>

<ol>
  <li>Here is</li>
  <li>a list for</li>
  <li>you to read</li>
</ol>

<h2>My subheading</h2>

<p>This is the first subsection of my document. I'd love people to be able to find this content!</p>

<h2>My 2nd subheading</h2>

<p>This is the second subsection of my content. I think is more interesting than the last one.</p>
```

## Accessibility in language

You should use clear language that is not overly complex, and doesn't use unnecessary jargon or slang terms. This not only benefits people with cognitive or other disabilities; it benefits readers for whom the text is not written in their first language, younger people ... everyone in fact! Apart from this, you should try to avoid using language and characters that don't get read out clearly by the screenreader. For example:

* Don't use dashes if you can avoid it. Instead of writing 5–7, write 5 to 7.
* Expand abbreviations — instead of writing Jan, write January.
* Expand acronyms, at least once or twice. Instead of writing HTML in the first instance, write Hypertext Markup Language

## Accessibility in page layouts

Page layouts can also be made accessible if you use the right HTML elements. Can you imagine a layout created with nested tables? This is an old practice, but if you're not aware of semantic elements, you will be making hard for screen readers to understand your content if your layout is complex.

__Don't__

```html
<table width="1200">
      <!-- main heading row -->
      <tr id="heading">
        <td colspan="6">

          <h1 align="center">Header</h1>

        </td>
      </tr>
      <!-- nav menu row  -->
      <tr id="nav" bgcolor="#ffffff">
        <td width="200">
          <a href="#" align="center">Home</a>
        </td>
        <td width="200">
          <a href="#" align="center">Our team</a>
        </td>
        <td width="200">
          <a href="#" align="center">Projects</a>
        </td>
        <td width="200">
          <a href="#" align="center">Contact</a>
        </td>
        <td width="300">
          <form width="300">
            <input type="search" name="q" placeholder="Search query" width="300">
          </form>
        </td>
        <td width="100">
          <button width="100">Go!</button>
        </td>
      </tr>
      <!-- spacer row -->
      <tr id="spacer" height="10">
        <td>

        </td>
      </tr>
      <!-- main content and aside row -->
      <tr id="main">
        <td id="content" colspan="4" bgcolor="#ffffff">

          <!-- main content goes here -->
        </td>
        <td id="aside" colspan="2" bgcolor="#ff80ff" valign="top">
          <h2>Related</h2>

          <!-- aside content goes here -->

        </td>
      </tr>
      <!-- spacer row -->
      <tr id="spacer" height="10">
        <td>

        </td>
      </tr>
      <!-- footer row -->
      <tr id="footer" bgcolor="#ffffff">
        <td colspan="6">
          <p>©Copyright 2050 by nobody. All rights reversed.</p>
        </td>
      </tr>
    </table>
```

__Do__

```html
<header>
  <h1>Header</h1>
</header>

<nav>
  <!-- main navigation in here -->
  <ul>
    <li>
      <a href="#">Home</a>
    </li>
    <li>
      <a href="#">Our team</a>
    </li>
    <li>
      <a href="#">Projects</a>
    </li>
    <li>
      <a href="#">Contact</a>
    </li>
    <li>
      <form role="search">
        <input type="search" name="q" placeholder="Search query">
        <button type="submit">Search</button>
      </form>
    </li>
  </ul>
</nav>

<!-- Here is our page's main content -->
<main>

  <!-- It contains an article -->
  <article>
    <h2>Article heading</h2>

    <!-- article content in here -->
  </article>

  <aside>
    <h2>Related</h2>

    <!-- aside content in here -->
  </aside>

</main>

<!-- And here is our main footer that is used across all the pages of our website -->

<footer>
  <!-- footer content in here -->
  <p>©Copyright 2050 by nobody. All rights reversed.</p>
</footer>
```

If you try the more modern structure example with a screenreader, you'll notice that the layout markup it's easier to understand and follow.

See [content sectioning reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#Content_sectioning) for choosing the right elements when creating pages so the document content is organized into logical pieces.

## HTML elements supported by screen readers

### Sections and grouping

* `<article>`
* `<section>`
* `<nav>`
* `<aside>`
* `<header>`
* `<footer>`
* `<figure>`
* `<figcaption>`
* `<main>`

### Text-level

* `<time>`
* `<mark>`


### Graphics and media

* `<canvas>`
* `<audio>`
* `<video>`
* `<track>`

### Controls

* search input
* tel input
* url input
* email input
* details
* summary

### Properties

* hidden
* required
* placeholder

More on [HTML5 Accessibility](https://www.html5accessibility.com/).

## Accessibility in UI Controls

__Don't__

```html
<p class="heading1">Links</p>

<div>This is a link to <button href="https://www.mozilla.org">Mozilla</button>.</div>

<div>Another link, to the <button href="https://developer.mozilla.org">Mozilla Developer Network</button>.</div>

<div class="heading2">Buttons</div>

<div>
  <div data-message="This is from the first button">Click me!</div>
<div data-message="This is from the second button">Click me too!</div>
<div data-message="This is from the third button">And me!</div>
</div>

<p class="heading2">Form</p>

<form>
  <div>
    <span>Fill in your name:</span>
    <input type="text" name="name">
  </div>
  <div>
    <span>Enter your age:</span>
    <input type="text" name="age">
  </div>
  <div>
    <span>Choose your mood:</span>
    <select name="mood">
      <option>Happy</option>
      <option>Sad</option>
      <option>Angry</option>
      <option>Worried</option>
    </select>
  </div>
</form>
```

__Do__

```html
<h1>Links</h1>

<p>This is a link to <a href="https://www.mozilla.org">Mozilla</a>.</p>

<p>Another link, to the <a href="https://developer.mozilla.org">Mozilla Developer Network</a>.</p>

<h2>Buttons</h2>

<p>
  <button data-message="This is from the first button">Click me!</button>
  <button data-message="This is from the second button">Click me too!</button>
  <button data-message="This is from the third button">And me!</button>
</p>

<h2>Form</h2>

<form>
  <div>
    <label for="name">Fill in your name:</label>
    <input type="text" id="name" name="name">
  </div>
  <div>
    <label for="age">Enter your age:</label>
    <input type="text" id="age" name="age">
  </div>
  <div>
    <label for="mood">Choose your mood:</label>
    <select id="mood" name="mood">
      <option>Happy</option>
      <option>Sad</option>
      <option>Angry</option>
      <option>Worried</option>
    </select>
  </div>
</form>
```

### Good text and link labels

You should make sure that your button and link text labels are understandable and distinctive. Don't just use "Click here" for your labels, as screenreader users sometimes get up a list of buttons and form controls.

__Don't__

```html
<p>Whales are really awesome creatures. To find more out about whales, <a href="whales.html">click here</a>.</p>
```

__Do__

```html
<p>Whales are really awesome creatures. <a href="whales.html">Find out more about whales</a>.</p>
```

Form labels are also important, for giving you a clue what you need to enter into each form input. The following seems like a reasonable enough example:

__Don't__

```html
Fill in your name: <input type="text" id="name" name="name">
```

__Do__

```html
<div>
  <label for="name">Fill in your name:</label>
  <input type="text" id="name" name="name">
</div>
```

## Alternative texts

Whereas textual content is inherently accessible, the same cannot necessarily be said for multimedia content — image/video content cannot be seen by visually-impaired people, and audio content cannot be heard by hearing-impaired people.

Some examples with `<img>` element:

| Example        | Screen reader           |
| ------------- |:-------------:|
| `<img src="dinosaur.png">`      | "/dinosaur.png, image" |
| `<img src="dinosaur.png" alt="A red Tyrannosaurus Rex: A two legged dinosaur standing upright like a human, with small arms, and a large head with lots of sharp teeth.">`      | alt text      |
| `<img src="dinosaur.png" alt="A red Tyrannosaurus Rex: A two legged dinosaur standing upright like a human, with small arms, and a large head with lots of sharp teeth." title="The Mozilla red dinosaur">` | alt text, the title attribute, and the filename
| `<img src="dinosaur.png" aria-labelledby="dino-label"><p id="dino-label">The Mozilla red Tyrannosaurus Rex: A two legged dinosaur standing upright like a human, with small arms, and a large head with lots of sharp teeth.</p>`| paragraph content, defined in `aria-labelledby` attribute

The last example in the table is useful, because you can reuse the same description text for multiple images.

## Decoration images

If you have images for visual decoration, it is better to keep them away from screen readers by leaving the `alt` attribute empty, or by setting the `role="presentation"` attribute, or if you're good at CSS, configuring your styles so the image appears as the background of an element.

```html
<img src="background-image.png" alt="">
```

```html
<img src="background-image.png" role="presentation">
```

## Links

Links ( the `<a>` element with an href attribute ), depending on how they are used, can help or harm accessibility. By default links are accessible in appearance. They can improve accessibility by enabling a user to quickly navigate sections of a document. They can also harm accessibilty if their accessible styling is removed or if JavaScript causes them to behave in unexpected ways.

### onclick events

Anchor tags are often abused with the onclick event to create pseudo-buttons by setting href to "#" or "javascript:void(0)" to prevent the page from refreshing, it is suggested to use an anchor for navigation using a proper URL and buttons for other actions.

__Don't__

```html
<a href="#">Send email</a>
```

__Do__

```html
<button>Send email</button>
```

### External links

__Don't__

```html
<a target="_blank" href="https://www.wikipedia.org/">Wikipedia</a>
```

__Do__

```html
<a target="_blank" href="https://www.wikipedia.org/">Wikipedia (opens in a new window)</a>
```

## Links to non-HTML resources

__Don't__

```html
<a target="_blank" href="2017-annual-report.ppt">2017 Annual Report</a>
```

__Do__

```html
<a target="_blank" href="2017-annual-report.ppt">2017 Annual Report (PowerPoint 1MB)</a>
```

## Links/Buttons Proximity

Large amounts of interactive content—including anchors—placed in close visual proximity to each other should have space inserted to separate them. This spacing is beneficial for people who suffer from fine motor control issues, and may accidentally activate the wrong interactive content while navigating.

![Form buttons bad proximity example](https://user-images.githubusercontent.com/61557537/79697733-f736ab00-8249-11ea-9748-bb227fbe2d17.png)

## Exercise

Creating an accessible HTML form.

1. Inside your fork `html-tutorial` repo, under the `5-accessibility` folder, create a file named `accessible-form.html` Don't forget to include the `.html` extension.
2. Create a new branch with the name `feature/accessible-form`.
3. Inside of it, create the form from the image:

![Accessible form exercise](https://user-images.githubusercontent.com/61557537/79698080-1fbfa480-824c-11ea-8e18-a95450513f8a.png)

  * Make sure the form is accessible by navigating the inputs with the keyboard.
  * Include descriptions for those elements that express they're required.
  * Use labels for input elements.
  * Use fieldsets and legends.
  * Use aria-attributes to indicate the inputs that are required.

4. Commit your changes
5. Push the changes to your local copy of the repo.
6. Create a pull request and please assign the reviewers.

## Sources

* [HTMLDog - Accessible forms](https://htmldog.com/guides/html/advanced/forms/)
* [HTML: A good basis for accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML)
* [Using the HTML lang attribute](https://developer.paciellogroup.com/blog/2016/06/using-the-html-lang-attribute/)
