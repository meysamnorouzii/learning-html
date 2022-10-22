# HTML Basics

# Table Of Contents

1. <a href="#html-structure">HTML Structure</a>
2. <a href="#typography">Typography</a>
3. <a href="#link">Link</a>
4. <a href="#image">Image</a>
5. <a href="#favicon">Favicon</a>
6. <a href="#tables">Tables</a>
7. <a href="#list">List</a>
8. <a href="#block-and-inline">Block and Inline</a>
9. <a href="#iframe ">Iframe</a>
10. <a href="#html-javascript">HTML JavaScript</a>
11. <a href="#head">Head</a>
12. <a href="#computer-code">Computer Code</a>
13. <a href="#semantic">Semantic</a>
14. <a href="#html-uniform-resource-locators">HTML Uniform Resource Locators</a>
15. <a href="#graphics">Graphics</a>
16. <a href="#media">Media</a>

# HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width,initial-scale=1.0" />
    <title>page title</title>
  </head>

  <body>
    <h1>Hello world!</h1>
  </body>
</html>
```

# Typography

## Headings

```html
<!-- HTML Heading Page -->
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

## Paragraph

```html
<!-- Paragraph -->
<p>This is a paragraph.</p>
<!-- Pre-formatted Text -->
<pre>
        My Bonnie lies over the ocean.
      
        My Bonnie lies over the sea.
      
        My Bonnie lies over the ocean.
      
        Oh, bring back my Bonnie to me.
</pre>
<!-- line break -->
<br />
<!-- Horizontal Rules -->
<hr />
```

## Formatting

```html
<!-- HTML Bold Text -->
<b>This text is bold</b>

<!-- Important text -->
<strong>This text is important!</strong>

<!-- Italic text -->
<i>This text is italic</i>

<!-- Emphasized text -->
<em>This text is emphasized</em>

<!-- Smaller text -->
<small>This is some smaller text.</small>

<!-- Marked text -->
<mark>mark text</mark>

<!-- Deleted text -->
<del>delete text</del>

<!--  Inserted text -->
<ins>Inserted text</ins>

<!-- Subscript text -->
<p>This is <sub>subscripted</sub> text.</p>

<!-- Superscript text -->
<p>This is <sup>superscripted</sup> text.</p>
```

## Quotations

```html
<!-- Quotations -->
<blockquote cite="http://www.worldwildlife.org/who/index.html">
  For 50 years, WWF has been protecting the future of nature. The world's
  leading conservation organization, WWF works in 100 countries and is supported
  by 1.2 million members in the United States and close to 5 million globally.
</blockquote>

<!-- Short Quotations -->
<q>Build a future where people live in harmony with nature.</q>

<!-- Abbreviations -->
<abbr title="World Health Organization">WHO</abbr>

<!-- Contact Information -->
<address>
  Written by John Doe.<br />
  Visit us at:<br />
  Example.com<br />
  Box 564, Disneyland<br />
  USA
</address>

<!-- Work Title -->
<p><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</p>

<!-- Bi-Directional Override -->
<bdo dir="rtl">This text will be written from right to left</bdo>
```

# Link

```html
<a href="url">...</a>
<!-- sample url -->

<!-- Absolute URLs -->
<a href="https://www.google.com/">...</a>

<!-- Relative URLs -->
<a href="/css/default.asp">...</a>

<!-- Link to an Email Address -->
<a href="mailto:someone@example.com">...</a>

<!-- Linking to an element on the same page -->
<a href="#id_element">...</a>

<!-- Linking to telephone numbers -->
<a href="tel:+49.157.0156">...</a>

<!-- title Atribute -->
<a href="url" title="additional information about the link">...</a>

<!-- target Atribute -->
<a href="url" target="_self">...</a>
<a href="url" target="_blank">...</a>
<a href="url" target="_parent">...</a>
<a href="url" target="_top">...</a>

<!-- download Atribute -->
<a href="url" target="_top" download>...</a>
<a href="url" target="_top" download="filename">...</a>
```

# Image

```html
<img src="url" alt="alternatetext" />
<!-- map -->
<img src="url" alt="alternatetext" usemap="#mapp" />

<map name="mapp">
  <area shape="rect" coords="34,44,270,350" alt="" href="" />

  <area shape="rect" coords="left,top" alt="" href="" />
  <area shape="circle" coords="center[left,top], radius" alt="" href="" />
  <area shape="poly" coords="left,top" alt="" href="" />
  <area shape="default" coords="" alt="" href="" />
</map>

<!-- picture -->

<!-- There are two main purposes for the <picture> element: -->
<!-- 1. Bandwidth -->
<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg" />
  <source media="(min-width: 465px)" srcset="img_car.jpg" />
  <img src="img_girl.jpg" />
</picture>

<!-- 2. Format Support -->
<picture>
  <source srcset="img_avatar.png" />
  <source srcset="img_girl.jpg" />
  <img src="img_beatles.gif" alt="Beatles" style="width:auto;" />
</picture>
```

# Favicon

```html
<head>
  <link rel="icon" type="image/x-icon" href="/img/favicon.ico" />
</head>
```

# Tables

## Table Structure

```html
<table>
  <caption>
    caption text
  </caption>
  <colgroup>
    <col span="1" style="visibility: collapse" />
    <col span="1" style="background-color: gray" />
    <col span="1" />
    <col span="1" style="background-color: blue" />
  </colgroup>
  <!-- Groups the header content in a table -->
  <thead>
    <!-- tr stands for table row. -->
    <tr>
      <!-- th stands for table header. -->
      <th>header 1</th>
      <th colspan="2">header 2</th>
      <th>header 3</th>
    </tr>
  </thead>
  <!-- Groups the body content in a table -->
  <tbody>
    <tr>
      <!-- td stands for table data. -->
      <td rowspan="2">th 1- col 1</td>
      <td rowspan="2">col 2</td>
      <td rowspan="2">col 3</td>
      <td>col 4 - row 1</td>
    </tr>
    <tr>
      <td>col 4 - row 2</td>
    </tr>
    <tr>
      <!-- td stands for table data. -->
      <td>th 2- col 1</td>
      <td>col 2</td>
      <td>col 3</td>
      <td>col 4</td>
    </tr>
  </tbody>
  <!-- Groups the footer content in a table -->
  <tfoot>
    <tr>
      <td>footer</td>
      <td>footer</td>
      <td>footer</td>
      <td>footer</td>
    </tr>
  </tfoot>
</table>
```

<table style="width:500px;">
  <caption>
    caption text
  </caption>
  <colgroup>
    <col span="1" style="visibility: collapse">
    <col span="1" style="background-color: gray">
    <col span="1">
    <col span="1" style="background-color: blue">
  </colgroup>
  <!-- Groups the header content in a table -->
  <thead>
    <!-- tr stands for table row. -->
    <tr>
      <!-- th stands for table header. -->
      <th>header 1</th>
      <th colspan="2">header 2</th>
      <th>header 3</th>
      <th>header 4</th>
    </tr>
  </thead>
  <!-- Groups the body content in a table -->
  <tbody>
    <tr>
      <!-- td stands for table data. -->
      <td rowspan="2">th 1- col 1</td>
      <td rowspan="2">col 2</td>
      <td rowspan="2">col 3</td>
      <td>col 4 - row 1</td>
      <td>col 5</td>
    </tr>
    <tr>
      <td>col 4 - row 2</td>
    </tr>
    <tr>
      <!-- td stands for table data. -->
      <td>th 2- col 1</td>
      <td>col 2</td>
      <td>col 3</td>
      <td>col 4</td>
      <td>col 5</td>
    </tr>
  </tbody>
  <!-- Groups the footer content in a table -->
  <tfoot>
    <tr>
      <td>footer</td>
      <td>footer</td>
      <td>footer</td>
      <td>footer</td>
    </tr>
  </tfoot>
</table>

# List

```html
<!-- An unordered HTML list: -->
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>

<!-- An ordered HTML list: -->
<!-- type 1-A-a-i-I -->
<ol type="1">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
<!-- A description list -->
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```

# Block and Inline

Here are the block-level elements in HTML:

```html
<h1></h1>
<h2></h2>
<h3></h3>
<h4></h4>
<h5></h5>
<h6></h6>
<hr />
<p></p>
<pre></pre>
<blockquote></blockquote>
<address></address>

<ul></ul>
<li></li>
<ol></ol>
<dl></dl>
<dt></dt>
<dd></dd>

<table></table>
<tfoot></tfoot>

<div></div>

<header></header>
<footer></footer>
<main></main>
<nav></nav>
<aside></aside>
<article></article>
<section></section>

<canvas></canvas>
<fieldset></fieldset>
<figcaption></figcaption>
<figure></figure>

<form></form>

<noscript></noscript>

<video></video>
```

Here are the inline elements in HTML:

```html
<!-- <acronym></acronym> Not Supported in HTML5. -->
<!-- <big></big> Not Supported in HTML5. -->
<!-- <tt></tt> Not Supported in HTML5. -->

<br />
<b></b>
<strong></strong>
<i></i>
<em></em>
<small></small>
<sub></sub>
<sup></sup>
<abbr></abbr>
<q></q>
<bdo></bdo>
<cite></cite>

<a></a>
<img />
<map></map>
<button></button>
<input />
<label></label>
<code></code>
<dfn></dfn>
<kbd></kbd>
<object></object>
<output></output>
<samp></samp>
<script></script>
<select></select>
<span></span>
<textarea></textarea>
<time></time>
<var></var>
```

# Iframe

```html
<iframe src="url" title="description"></iframe>
<!-- Target for a Link -->
<iframe src="url" title="description" name="iframe_a"></iframe>
<a href="https://www.w3schools.com" target="iframe_a">...</a>
```

# HTML JavaScript

```html
<html>
  <head>
    <title>title</title>
  </head>
  <body>
    <h1 id="demo"></h1>

    <script>
      var el = document.getElementById("demo");
      el.innerHTML = "Hello JavaScript!";
    </script>

    <noscript> Sorry, your browser does not support JavaScript! </noscript>
  </body>
</html>
```

# Head

```html
<html>
  <head>
    <!-- Define the character set used: -->
    <meta charset="UTF-8" />

    <!-- Refresh document every 30 seconds: -->
    <meta http-equiv="refresh" content="30" />

    <!-- Setting the viewport to make your website look good on all devices: -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!-- The <base> element specifies the base URL and/or target for all relative URLs in a page -->
    <base href="https://www.w3schools.com/" target="_blank" />
  </head>
</html>
```

# Computer Code

```html
<!-- defines a piece of computer code -->
<code> x = 5; y = 6; z = x + y; </code>

<!-- defines keyboard input -->
<p>Save by pressing <kbd>Ctrl + S</kbd></p>

<!-- defines sample output from a computer program -->
<p>
  <samp>File not found.<br />Press F1 to continue</samp>
</p>

<!-- defines a variable in programming or in a mathematical expression -->
<p>
  The area of a triangle is: 1/2 x <var>b</var> x <var>h</var>, where
  <var>b</var> is the base, and <var>h</var> is the vertical height.
</p>
```

# Semantic

Examples of non-semantic elements:

```html
<!-- non-semantic : Tells nothing about its content. -->
<div></div>
<span></span>
<!-- semantic : Clearly defines its content. -->

<!-- Defines a section in a document -->
<section></section>

<!-- Defines independent, self-contained content -->
<article></article>

<!-- Specifies a header for a document or section -->
<header></header>

<!-- Defines a footer for a document or section -->
<footer></footer>

<!--  Defines navigation links -->
<nav></nav>

<!-- Defines content aside from the page content -->
<aside></aside>

<!-- Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc. -->
<figure></figure>

<!-- Defines a caption for a <figure> element -->
<figcaption></figcaption>

<!-- Specifies the main content of a document -->
<main></main>

<!-- 	Defines marked/highlighted text -->
<mark></mark>

<!-- Defines additional details that the user can view or hide -->
<details></details>

<!-- Defines a visible heading for a <details> element -->
<summary></summary>

<!-- Defines a date/time -->
<time></time>
```

## &lt;section&gt; can be used:

 <ul>
    <li>Chapters</li>
    <li>Introduction</li>
    <li>News items</li>
    <li>Contact information</li>
  </ul>

## &lt;article&gt; can be used:

<ul>
  <li>Forum posts</li>
  <li>Blog posts</li>
  <li>User comments</li>
  <li>Product cards</li>
  <li>Newspaper articles</li>
</ul>

## &lt;header&gt; typically contains:

<ul>
 <li>one or more heading elements (&lt;h1&gt; - &lt;h6&gt;)</li>
  <li>logo or icon</li>
  <li>authorship information</li>
</ul>

## &lt;footer&gt; typically contains:

<ul>
  <li>authorship information</li>
  <li>copyright information</li>
  <li>contact information</li>
  <li>sitemap</li>
  <li>back to top links</li>
  <li>related documents</li>
</ul>

# HTML Uniform Resource Locators

### URL - Uniform Resource Locator

    scheme://prefix.domain:port/path/filename

Explanation:

<ul>
  <li><b>scheme</b> - defines the type of Internet service (most common is <b>http</b> or <b>https</b>)</li>

  <li><b>prefix</b> - defines a domain <b>prefix</b> (default for http is <b>www</b>)</li>

  <li><b>domain</b> - defines the Internet <b>domain name</b> (like w3schools.com)</li>

  <li><b>port</b> - defines the <b>port number</b> at the host (default for http is <b>80</b>)</li>

  <li><b>path</b> - defines a <b>path</b> at the server (If omitted: the root directory of the site)</li>

  <li><b>filename</b> - defines the name of a document or resource</li>
</ul>

<table>
  <tr>
    <th>Scheme</th>
    <th>Short for</th>
    <th>Used for</th>
  </tr>
  <tr>
    <td>http</td>
    <td>HyperText Transfer Protocol</td>
    <td>Common web pages. Not encrypted</td>
  </tr>
  <tr>
    <td>https</td>
    <td>Secure HyperText Transfer Protocol</td>
    <td>Secure web pages. Encrypted</td>
  </tr>
  <tr>
    <td>ftp</td>
    <td>File Transfer Protocol</td>
    <td>Downloading or uploading files</td>
  </tr>
  <tr>
    <td>file</td>
    <td></td>
    <td>A file on your computer</td>
  </tr>
</table>

# Graphics

```html
<!-- Canvas -->
<canvas id="myCanvas" width="200" height="100"></canvas>

<!-- SVG -->
<svg width="100" height="100">
  <circle
    cx="50"
    cy="50"
    r="40"
    stroke="green"
    stroke-width="4"
    fill="yellow"
  />
</svg>

<svg width="400" height="100">
  <rect
    width="400"
    height="100"
    style="fill:rgb(0,0,255);stroke-width:10;stroke:rgb(0,0,0)"
  />
</svg>
```

# Media

```html
<!-- video -->
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4" />
  <source src="movie.ogg" type="video/ogg" />
  Your browser does not support the video tag.
</video>

<video width="320" height="240" autoplay muted>...</video>

<!-- audio -->
<audio controls>
  <source src="horse.ogg" type="audio/ogg" />
  <source src="horse.mp3" type="audio/mpeg" />
  Your browser does not support the audio element.
</audio>

<audio controls autoplay muted>...</audio>

<!-- plug-ins -->
<object width="100%" height="500px" data="snippet.html"></object>
<embed width="100%" height="500px" src="snippet.html" />

<!-- youtube -->

<!-- loop=1 -->
<iframe
  width="420"
  height="315"
  src="https://www.youtube.com/embed/tgbNymZ7vqY?playlist=tgbNymZ7vqY&loop=1"
>
</iframe>

<!-- autoplay=1, mute=1 or controls=0 -->
<iframe
  width="420"
  height="315"
  src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1"
>
</iframe>
```
