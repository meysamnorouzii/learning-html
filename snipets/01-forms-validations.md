# HTML Form & Validations

# Table Of Contents

1. <a href="#html-form">HTML Form</a>
2. <a href="#form-element">Form Element</a>
3. <a href="#input-types">Input Types</a>
4. <a href="#input-form-attributes">Input form\* Attributes</a>
5. <a href="#pattern-regex">Pattern Regex</a>

# HTML Form

```html
<!-- On submit, send form data to "action_page.php -->
<form action="/action_page.php">
  ...
  <input type="submit" value="Submit" />
</form>

<!-- 
target value :
    _blank, _self, _top, _parent,
    framename: The response is displayed in a named iframe
-->
<form action="/action_page.php" target="_blank">...</form>

<!-- method: GET, POST -->
<form action="/action_page.php" method="get">...</form>

<!-- autocomplete -->
<form action="/action_page.php" autocomplete="on">...</form>

<!-- novalidate -->
<form action="/action_page.php" novalidate>...</form>
```

# Form Element

```html
<form>
  <!-- input, label -->
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname" />

  <!-- select, option -->
  <label for="cars">Choose a car:</label>
  <select id="cars" name="cars" size="3" multiple>
    <option value="volvo" selected>Volvo</option>
    <option value="saab">Saab</option>
    <option value="fiat">Fiat</option>
    <option value="audi">Audi</option>
  </select>

  <!-- textarea -->
  <textarea name="message" rows="10" cols="30">...</textarea>

  <!-- button -->
  <button type="button" onclick="alert('Hello World!')">Click Me!</button>

  <!-- fieldset, legend -->
  <fieldset>
    <legend>Personalia:</legend>
    <label for="fname">First name:</label><br />
    <input type="text" id="fname" name="fname" value="John" />
  </fieldset>

  <!-- datalist : Specifies a list of pre-defined options for input controls -->
  <input list="browsers" name="browser" />
  <datalist id="browsers">
    <option value="Internet Explorer"></option>
    <option value="Firefox"></option>
    <option value="Chrome"></option>
    <option value="Opera"></option>
    <option value="Safari"></option>
  </datalist>

  <!-- output: Defines the result of a calculation -->
  <form
    action="/action_page.php"
    oninput="x.value=parseInt(a.value)+parseInt(b.value)"
  >
    0
    <input type="range" id="a" name="a" value="50" />
    100 +
    <input type="number" id="b" name="b" value="50" />
    =
    <output name="x" for="a b"></output>
    <br /><br />
    <input type="submit" />
  </form>
</form>
```

# Input Types

```html
<input type="button" />
<input type="checkbox" />
<input type="color" />
<input type="date" />
<input type="datetime-local" />
<input type="email" />
<input type="file" />
<input type="hidden" />
<input type="image" />
<input type="month" />
<input type="number" />
<input type="password" />
<input type="radio" />
<input type="range" />
<input type="reset" />
<input type="search" />
<input type="submit" />
<input type="tel" />
<input type="text" />
<input type="time" />
<input type="url" />
<input type="week" />
```

# Input Attrebutes

<ul>
    <li>checked</li>
    <li>disabled</li>
    <li>max</li>
    <li>maxlength</li>
    <li>min</li>
    <li>pattern</li>
    <li>readonly</li>
    <li>required</li>
    <li>size</li>
    <li>step</li>
    <li>value</li>
    <li>multiple</li>
    <li>placeholder</li>
    <li>autofocus</li>
    <li>height</li>
    <li>width</li>
    <li>list</li>
</ul>

# Input form\* Attributes

```html
<!-- An input field located outside of the HTML form (but still a part of the form) -->
<form action="/action_page.php" id="form1">
  ...
  <input type="submit" value="Submit" />
</form>

<label for="lname">Last name:</label>
<input type="text" id="lname" name="lname" form="form1" />

<!-- The formaction Attribute -->
<form action="/action_page.php">
  ...
  <input type="submit" value="Submit" />
  <input type="submit" formaction="/action_page2.php" value="Submit as Admin" />
</form>

<!-- The formenctype Attribute -->
<form action="/action_page_binary.asp" method="post">
  ...
  <input type="submit" value="Submit" />
  <input
    type="submit"
    formenctype="multipart/form-data"
    value="Submit as Multipart/form-data"
  />
</form>

<!-- The formmethod Attribute -->
<form action="/action_page.php" method="get">
  ...
  <input type="submit" value="Submit using GET" />
  <input type="submit" formmethod="post" value="Submit using POST" />
</form>

<!-- The formtarget Attribute -->
<form action="/action_page.php">
  ...
  <input type="submit" value="Submit" />
  <input type="submit" formtarget="_blank" value="Submit to a new window/tab" />
</form>

<!-- The formnovalidate Attribute -->
<form action="/action_page.php">
  ...
  <input type="submit" value="Submit" />
  <input
    type="submit"
    formnovalidate="formnovalidate"
    value="Submit without validation"
  />
</form>

<!-- The novalidate Attribute -->
<form action="/action_page.php" novalidate>
  ...
  <input type="submit" value="Submit" />
</form>
```

# Pattern Regex

```html
<!-- Specifies a regular expression -->
<input pattern="regexp" />

<!-- contain numbers and special characters -->
<input type="text" pattern="[A-Za-z0-9]{3}" />

<!-- contain 8 or more characters -->
<input type="password" pattern=".{8,}" />

<!-- contain 8 or more characters that are of at least one number, and one uppercase and lowercase letter -->
<input type="password" pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}" />

<!-- ex: characters@characters.domain -->
<input type="email" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$" />

<!-- CANNOT contain the following characters: ' or " -->
<input type="search" pattern="[^'\x22]+" />

<!-- start with http:// or https:// -->
<input type="url" pattern="https?://.+" />
```
