# Forms and validations

* Let's understand how to structure HTML forms and give them semantics so they are usable and accessible.
* Websites are designed and developed in such a way that people with disabilities can use them. More specifically, people can: perceive, understand, navigate, contribute and navigate.

![image](https://user-images.githubusercontent.com/36536646/79612762-e7408f00-80c2-11ea-9515-895551579124.png)

## How to structure a web form

* The `<form>` element formally defines a form and attributes that determine the form's behavior.
* The URL that processes the form submission. This value can be overridden by a formaction attribute on a <button>, <input type="submit">, or <input type="image"> element.
  
```html
    <form action="">
        <!--form content-->
    </form>
```

* It's strictly forbidden to nest a form inside another form
* Don't forget *accessibility*.

Some tips:

* The `<label>` element is the formal way to define a label for an HTML form widget.
* *Accessibility*: screen readers will speak a form element label along with any related instructions. 

```html
<label for="name">
        Name: <input type="text" id="name" name="user_name">
        <abbr title="required" aria-label="required">*</abbr>
 </label>
```

* *type* attribute in the `<input>` tag [types](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input).
* *required* attribute in the `<input>` tag.

* Nest the `<input>` tag to the `<label>` tag.
```html
  <label for="name">
    Name: <input type="text" id="name" name="user_name">
  </label>
```

* The `<fieldset>` element is a convenient way to create groups of widgets that share the same purpose (styling and semantic). 
* You can label a `<fieldset>` by including a `<legend>` element.
* Select (5 or more options...)

```html
<fieldset>
        <legend>Choose your city:</legend>
        <select id="city">
            <option value="Tunja">Tunja</option>
            <option value="Bogota">Bogota</option>
            <option value="Cali">Cali</option>
            <option value="Bucaramanga">Bucaramanga</option>
            <option value="Medellin">Medellin</option>
            <option value="Pasto">Pasto</option>
        </select>
 </fieldset>
```

* Group radio buttons in fieldsets

```html
  <fieldset>
        <legend>Choose your bootcamp:</legend>
        <input id="basic" type="radio" name="bootcamp" value="basic">
        <label for="basic">Basic web development</label>
        <input id="advanced" type="radio" name="bootcamp" value="advanced">
        <label for="advanced">Advanced web development</label>
    </fieldset>
```

* Rule of thumb: If it's a long list or the alternatives aren't that important, use a select.

## Validation


## Exercise

1. Inside your `4-forms-validations` folder create a file named `form.html`.
2. Build in HTML a simple form with semantic structure. The form must have the following elements:

* First name
* Last name
* Email-Address
* Date of birth (using)
* Gender (using select)
* Socioeconomic status (using radiobutton)
* Hobbies (using checkbox)
* IMG (uearching file)

3. Push the changes to your local copy of the repo (Pull request).
 
## Source

* [How to structure a web form](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form)
* [Client-side form validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)
