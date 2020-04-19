# SEO basics

SEO stands for "Search Engine Optimization", basically optimize your website to it can be indexed by Google and more users can access to it.

## Steps in HTML to have a good SEO:

1. Meaningful title.
2. Good meta tags.
3. Include OG/Twitter meta tags.
4. Specify how other pages are related
5. Correct use of headings.
6. Put good quality links in your page.
7. Put alt and title attributes to your images.
8. Use Emphasizing where required.
9. Use tables and lists where required for exposing your content into Google's answers.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <!-- 1. Title tag -->
    <title>1</title>
    <!-- 2. Meta tags -->
    <meta name="robots" content="2">
    <meta name="description" content="3">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- 3. Open graph meta tags -->
    <meta name="og:title" property="og:title" content="The Title of Your Article">
    <meta name="twitter:card" content="summary">
    <!-- 4. Link tag to specify how pages are related -->
    <link rel="alternate" hreflang="es" href="https://seranking.com/es/">
  </head>
  <body>

    <!-- 5. Heading tags -->
    Headings:

    <h1></h1> – usually reserved for webpage titles.
    <h2></h2> – highlights the topic of the title.
    <h3></h3> – reflects points in regards to the topic.
    <h4></h4> – supports points from <h3>.
    <h5></h5> – not often used, but great for supporting points of <h4>.

   <!-- 6. Anchor/links tags -->
   Links:

   <a href="URL" title="this is the title" rel="nofollow">The link is here</a>

   <!-- 7. Images alt + title attributes -->
   Images:

   <img src="image.jpg" alt="labrador in sunglasses" title="dog">

   <!-- 8. Emphasizing tags -->
   Styling tags but with important meaning:

   <i>Italicized text</i>
   <b>Emboldened text</b>
   <strong>Strong text</strong>
   <q>Quote</q>

   <!-- 9. Table, ul and ol are used in Google's answers -->

   <table>
     <tr>
        <th>FIFA rankings</th>
        <td>Colombia</td>
      </tr>
   </table>

   <ul>
     <li>Unordered list item</li>
     <li>One more list item</li>
   </ul>

   <ol>
      <li>Ordered list item</li>
      <li>One more list item</li>
   </ol>
  </body>
</html>
```

## More about SEO

* [SEO Basics: Beginner’s Guide to SEO Success](https://ahrefs.com/blog/seo-basics/)
* [SEO Basics: Complete Beginner’s Guide to Search Engine Optimization](https://www.wordstream.com/blog/ws/2015/04/30/seo-basics)
* [The Beginner's Guide to SEO](https://moz.com/beginners-guide-to-seo)
