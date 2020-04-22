# Forms and validations

* Let's understand how to structure HTML forms and give them semantics so they are usable and accessible.
* Websites are designed and developed in such a way that people with disabilities can use them. More specifically, people can: perceive, understand, navigate, contribute and navigate.

![image](https://user-images.githubusercontent.com/36536646/79612762-e7408f00-80c2-11ea-9515-895551579124.png)

## How to structure a web form

* The `<form>` element formally defines a form and attributes that determine the form's behavior.
* The URL that processes the form submission. This value can be overridden by a formaction attribute on a `<button>`, `<input type="submit">`, or `<input type="image">` element.
  
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

There are two different types of client-side validation that you'll encounter on the web:

* Built-in form validation: uses HTML5 form validation features. Built-in form validation has better performance than JavaScript, but it is not as customizable as JavaScript validation.

```html
<form>
    <label for="number">How old are you?</label>
    <input type="number" id="number" name="amount" value="1" min="1" max="100">

    <label for="t2">What's your favorite sport<abbr title="This field is mandatory" aria-label="required">*</abbr></label>
        <input type="text" id="t2" name="sport" list="l2" required pattern="[Ss]occer|[Bb]asketball|[Hh]ockey|[Tt]ennis|[Vv]olleyball">
        <datalist id="l1">
          <option>Soccer</option>
          <option>Basketball</option>
          <option>Hockey</option>
          <option>Tennis</option>
          <option>Volleyball</option>
        </datalist>

       <p>
          <label for="t3">Leave your personal description</label>
          <textarea id="t3" name="msg" maxlength="100" rows="5"></textarea>
       </p>
</form>
```
Other validations:

* __required__: Specifies whether a form field needs to be filled in before the form can be submitted.
* __minlength and maxlength__: Specifies the minimum and maximum length of textual data (strings)
* __min and max__: Specifies the minimum and maximum values of numerical input types
* __type__: Specifies whether the data needs to be a number, an email address, or some other specific preset type. 
* __pattern__: Specifies a regular expression that defines a pattern the entered data needs to follow.
* JavaScript validation: is coded using JavaScript. This validation is completely customizable, but you need to create it all (or use a library).

Let's see the difference: [Form validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)

## Submit - Reset buttons
* A click on a submit button (the default value) sends the form's data to the web page defined by the action attribute of the <form> element.
* The `<button>` element also accepts a type attribute — this accepts one of three values: submit, reset, or button.
* A click on a reset button resets all the form widgets to their default value immediately. This is considered bad practice, so you should avoid using this type of button unless you really have a good reason to include one.
  
```html
  <button type="submit">Validate the payment</button>

  <button type="reset">Reset</button>
```
## Should I specify the button type?

![image](https://user-images.githubusercontent.com/36536646/79809380-e82d2700-8335-11ea-80a7-b0d6e29b1be5.png)

* If you include a button in a form element without specifying the type, by default it's a  `submit` button. Semantics usually become important, so it's a good idea to make a habit of specifying the type.

```html
<form>
    <button>I will submit the form when clicked!</button>
</form>

//vs

<form>
    <button type='button'>I won't!</button>
</form>
```
## Exercise

1. Inside your `4-forms-validations` folder create a file named `form.html`.
2. Build in HTML a simple form with semantic structure. The form must have the following elements:

* First name
* Last name
* Email-Address (using email type)
* Date of birth (using date type)
* Gender (using select)
* Socioeconomic status (using radiobutton)
* Hobbies (using checkbox)
* IMG (searching file)

3. These fields must be required.
4. Push the changes to your local copy of the repo (Pull request).
 
## Source

* [How to structure a web form](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form)
* [Client-side form validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)
* [Accessibility For Beginners with HTML and CSS](https://dev.to/mxl/accessibility-for-beginners-with-html-and-css-16j7)
