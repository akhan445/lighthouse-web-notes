# Flexbox

Flexbox is a one-dimensional layout model
- one dimensional meaning flexbox deals with layout one dimension at a time (either **row** or **column**)

As oppose to styling using CSS, flexbox gives you the ability to layout your site using containers.
- if you want 3 columns/rows then you would divide your code into 3 containers and use those to style out the site
```html
<body>
  <div class="container">
    <div class="a">A</div>
    <div class="b">B</div>
  </div>
  <div class="container2">
    <div class="c">C</div>
    <div class="d">D</div>
  </div>
  <div class="container3">
    <div class="e">E</div>
    <div class="f">F</div>
  </div>
</body>
```

You usethe `display` property to specify that you are using `flex`

## **Inline and Block**

Html elements have inherent properties.

**Block** elements take up the entire space of their parent. These include:
- headings(`<h1>`, `<h6>`, ... `<h6>`)
- division (`<div>`) 
- section (`<section>`) 
- footer (`<footer>`) 
- article (`<article>`) 
- paragraph (`<p>`)
-lists (`<ul>`, `<li>`)
- nav (`<nav>`)

**Inline** elements do not start a new line when rendered in the browser. They only **take up as much space as content**.
- Inline elements contain only data and other inline elements
- You cannot add height, width, padding, margin etc to inline elements.
- These include:
  - anchor (`<a>`)
  - em (`<em>`)
  - strong (`<strong>`)
  - span (`<span>`)

![block-vs-inline](https://cl.ly/030Y00123f2z/Image%202017-10-11%20at%207.07.33%20PM.png)

**Inline-block** elements have properties of both.
- Doesn't automatically crate a new line but it **can have width, height, padding and margin properties**. Only two:
- image (`<img>`)
- buttons (`<button>`)


This guide covers flexbox in detail: [here](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
