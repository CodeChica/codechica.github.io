# CSS

CSS is short for Cascading Style Sheets. It's a language that is used to tell
the browser how to make your page look.

In CSS you specify which types of element should get certain settings.

```css
/* Find all 'div' elements and give them a pink background. */
div {
  background-color: pink;
}

/* Find all elements with a `hero` class and center their text. */
.hero {
  text-align: center;
}

/*
  Find the one element with an id of `container`
  and give it a width of 90% of the screen then make sure
  the left and right margins are even so that the content
  is centered.
*/
#container {
  width: 90%;
  margin-left: auto;
  margin-right: auto;
}
```

## Getting Started

The easiest way to add a little bit of CSS to your web page is to add a
[`style`][style] element to your webpage.

```html
<!doctype html>
<html>
  <head>
    <title>Simple</title>
    <style>
      p {
        background-color: pink;
      }
    </style>
  </head>
  <body>
    <p>Is it just me or is it pink in here?</p>
  </body>
</html>
```

When your CSS starts to get a little more complicated then it's time to move it
to a separate file. This will make it easier to work on your HTML and CSS in
separate tabs.

index.html
```html
<!doctype html>
<html>
  <head>
    <title>Simple</title>
    <link rel="stylesheet" href="application.css">
  </head>
  <body>
    <p>Is it just me or is it pink in here?</p>
  </body>
</html>
```

application.css
```css
p {
  background-color: pink;
}
```

## Grid Layout

Using a grid layout will make it easier to build a responsive web site that can
adjust the way it looks depending on the type of device that you're viewing it
from.

<pre>
 Desktop                           Mobile

 -------------------------------   ----------
 | header                      |   | header |
 -------------------------------   |--------|
 |     ||                      |   | nav    |
 |     ||                      |   |--------|
 | nav || main                 |   |        |
 |     ||                      |   | main   |
 |     ||                      |   |        |
 |     ||----------------------|   |--------|
 |     || footer               |   | footer |
 -------------------------------   ----------
</pre>

{% include youtube.html youtube_id="rPOX2hcaFvw" %}

```html
<!doctype html>
<html>
  <head>
    <title>Grid Layout</title>
    <link rel="stylesheet" href="application.css">
  </head>
  <body>
    <header></header>
    <nav></nav>
    <main></main>
    <footer></footer>
  </body>
</html>
```

```css
body {
  min-height: 100vh;
  display: grid;
  grid-gap: 1em;
  grid: 'header' auto 'nav' auto 'main' 1fr 'footer' auto / 1fr;
}
header { grid-area: header; }
nav { grid-area: nav; }
main { grid-area: main; }
footer { grid-area: footer; }

@media (min-width: 40em) {
  body {
    grid: 'header header' auto 'nav main' 1fr 'nav footer' auto / 12em 1fr;
  }
}
```

[Grid layout](https://codepen.io/miriamsuzanne/pen/JjPeQYP?editors=1100)

## Flex Layout

{% include empty.html %}

[Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)

<!--
TODO:: Describe

* inline css
* document `<style>` section
* external css file.
* code comments
* selectors
  * element type
  * id - there can only be one
  * class
  * '.img' vs '#img' vs 'img'
* grid system
  * flex vs percentage/pixels
    * 960/12
* box model
* responsive design (desktop, mobile, tablet)
* confetti css
* testing a selector in the browser. `querySelector(selector)`

-->

## Animations

{% include youtube.html youtube_id="etQEBtvI4zQ" %}

Next, try the [JavaScript][js] guide!

[js]: ./javascript.html
