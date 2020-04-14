# Writing semantic HTML

## Semantic

Refers to the meaning or additional information granted by the elements or labels of the language, information that defines or describes the content, function or section it contains.

![image](https://user-images.githubusercontent.com/36536646/79190140-1fa54c00-7de9-11ea-8d00-dd487cc1b330.png)

* Search engine optimization (html code analysis)
* Accessibility
* Practicality
* Reusability

![image](https://user-images.githubusercontent.com/36536646/79189977-bb828800-7de8-11ea-9147-53cf0ca4909d.png)

## Why we should care about semantics?

* Provides additional information about that document, which aids in communication.
* Semantic tags make it clear to the browser what the meaning of a page and its content is. 
* That clarity is also communicated with search engines, ensuring that the right pages are delivered for the right queries.

## Ambiguous vs Semantic

![image](https://user-images.githubusercontent.com/36536646/79190057-ee2c8080-7de8-11ea-95e4-cee11d2c820b.png)

* Let's see more examples: [Semantic structure](https://www.internetingishard.com/html-and-css/semantic-html/)

## Do vs Don't

```html
   <!-- Don't -->
   <div id="header"/>
   <div id="nav"/>
   <div id="footer"/>

    <!-- Do -->
   <header>
    <!-- header content -->
      <nav>
      <!-- nav content -->
      </nav>
   </header>
   
  <footer>
     <!-- footer content -->
    <p> PushDev 2020 </p>
  </footer>
```

## Homework

Build in HTML a simple form with semantic structure. The form must have the following elements:

1. First name
2. Last name
3. Email-Address
4. Date of birth
5. Gender (Using select)
6. Socioeconomic status (Using radiobutton)
7. IMG (Searching file

## Source

* [Semantic structure](https://www.internetingishard.com/html-and-css/semantic-html/)
* [Why use semantic HTML](https://www.lifewire.com/why-use-semantic-html-3468271)
* [Element list](https://developer.mozilla.org/es/docs/HTML/HTML5/HTML5_lista_elementos)
