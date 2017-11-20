---
layout: lesson
title: "Responsive navigation"
desc: "Use media queries and knowledge of how display works to create a responsive navigation."

markbot_submit: true
hide_show_for_marks: true

goal:
  before: "We’re going to look at how to make the image card pattern, concentrating on position absolute and relative."
  image: goal.gif
  notes:
    - label: "Type it, type it real good"
      text: "Remember the purpose of this lesson is to type the code out yourself—build up that muscle memory in your fingers!"

extra_tutorials:
  - title: "All devices setup"
    url: all-devices-setup
  - title: "Media queries"
    url: media-queries
  - title: "Screen sizes cheat sheet"
    url: screen-sizes-cheat-sheet
  - title: "Media queries slide deck"
    url: "/courses/web-dev-1/media-queries/"

fork:
  url: "https://github.com/acgd-webdev-1/responsive-navigation"

steps:
  - title: "Set up project"
    before: |
      After forking & cloning, before writing some code, create some files and get ready.
    folders:
      - label: "responsive-navigation"
        type: folder
      - label: "index.html"
        indent: 1
      - label: "css"
        type: folder
        indent: 1
      - label: "main.css"
        indent: 2
    after: |
      1. Make an `index.html`
      2. Make a `main.css` in your `css` folder.
    notes:
      - label: "Naming conventions"
        text: "Don’t forget to follow the [naming conventions](/topics/naming-paths-cheat-sheet/#naming-conventions)."

  - title: "Add HTML boilerplate"
    before: "*Use the `html5`, `viewport` and `css` snippets.*"
    code_lang: "html"
    code_file: "index.html"
    code: |
      <!DOCTYPE html>
      <html lang="en-ca">
      <head>
        <meta charset="utf-8">
        <title>Responsive navigation</title>
        <meta name="viewport" content="width=device-width,initial-scale=1">
        <link href="css/main.css" rel="stylesheet">
      </head>
      <body>

      </body>
      </html>
    lines:
      - num: 6
        text: |
          The `viewport` tag is extremely critical for responsive websites—it tells mobile browsers a couple things:

          1. Tells the browser that our website support whatever size the viewport currently is.
          2. Tells the browser not to zoom—our website is properly sized for the current viewport.

      - num: 7
        text: "Don’t forget to attach the CSS file."
    notes:
      - label: "HTML snippets"
        text: "Create the boilerplate with `html5`, `viewport` & `css`"

  - title: "Add CSS boilerplate"
    before: |
      Our CSS now needs a little more default code to better support all the browsers that exist. Making sure we tell the browsers that our website is properly set up for the device.

      *Use the `cssviewport`, `borderbox` & `textsize` snippets.*
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      @-moz-viewport { width: device-width; scale: 1; }
      @-ms-viewport { width: device-width; scale: 1; }
      @-o-viewport { width: device-width; scale: 1; }
      @-webkit-viewport { width: device-width; scale: 1; }
      @viewport { width: device-width; scale: 1; }

      html {
        -moz-text-size-adjust: 100%;
        -ms-text-size-adjust: 100%;
        -webkit-text-size-adjust: 100%;
        text-size-adjust: 100%;
        box-sizing: border-box;
        font: normal 100%/1.3 sans-serif;
      }

      *, *::before, *::after {
        box-sizing: inherit;
      }

      body {
        margin: 0;
      }
    lines:
      - num: "1-5"
        text: |
          The CSS `@viewport` lines have the same functionality as the `viewport` tag in HTML, they just serve different browsers.

          Eventually the CSS `@viewport` will replace the HTML version.

          The `-moz-`, `-ms-`, `-o-` & `-webkit-` parts are called vendor prefixes. They are beta versions of the feature that target specific browsers.

          - `-moz-` — Mozilla, aka Firefox
          - `-ms-` — Microsoft: IE & Edge
          - `-o-` — Opera, older versions
          - `-webkit-` — Webkit: Safari, Chrome, newer Opera
      - num: "8-11"
        text: |
          The `text-size-adjust` property tells the browser not to scale the fonts because we’ve set them up properly to be readable on any device screen.
      - num: 13
        text: |
          Set up a good `font` for small screens:

          - A `font-size` of `100%`
          - A `line-height` of `1.3`
    notes:
      - label: "CSS snippets"
        text: "Create the boilerplate with `cssviewport`, `borderbox` & `textsize`"

  - title: "Add the navigation HTML"
    before: |
      Let’s add the standard HTML we need to making navigation in a website.

      Even though this website will be responsive the HTML is exactly the same as we’ve written many times before.
    code_lang: html
    code_file: "index.html"
    code: |
      ⋮
      </head>
      <body>

        <header>
          <h1>Quetzalcoatlus</h1>
          <nav>
            <ul>
              <li><a href="#">Environment</a></li>
              <li><a href="#">Dimensions</a></li>
              <li><a href="#">Diet</a></li>
              <li><a href="#">Flight</a></li>
            </ul>
          </nav>
        </header>

      </body>
      </html>
      ⋮
    lines:
      - num: "2-3"
        fade: true
      - num: "17-18"
        fade: true

  - title: "Style the extra small screen navigation"
    before: |
      **We always—always—style the small screen version of our website first—this does not require media queries.**

      If we start with larger screen we end up making significantly more work for ourselves and we require so much extra, unnecessary CSS.
    code_lang: css
    code_file: "css/main.css"
    code: |
      ⋮
      body {
        margin: 0;
      }

      header {
        padding: .5rem 0;
        background-color: #ccc;
        text-align: center;
      }

      h1 {
        margin: 0 0 .5rem;
        font-size: 1.5rem;
      }

      nav ul {
        margin: 0;
        padding: 0;
        list-style-type: none;
      }

      nav li {
        text-align: left;
      }

      nav a {
        display: block;
        padding: .5em .75em;
        color: #333;
        text-decoration: none;
      }

      nav a:hover {
        background-color: #333;
        color: #fff;
      }
    lines:
      - num: "2-4"
        fade: true
    notes:
      - label: "Notice"
        text: |
          The small screen CSS is the most critical part of the CSS—it works on the most devices.

          **The small screen CSS always goes at the top of our file because it influences all other screen sizes.**
    after: |
      There’s nothing special in this CSS—it’s exactly the same CSS we’ve written many times before.

      *With a refresh in our browser this is what we should see.* **Make sure to open the developer tools and set the browser width to `320px`.**

      ![](extra-small.png)

  - title: "Adjust the screen for awkwardness"
    before: |
      Next we slowly increase the width of our browser window until the content looks awkward or could be improved.

      At around 400px—25em—the navigation can fit all across one line instead of being stacked—this is a good point to add a media query.
    code_lang: css
    code_file: "css/main.css"
    code: |
      ⋮
      nav a:hover {
        background-color: #333;
        color: #fff;
      }

      @media only screen and (min-width: 25em) {

        nav li {
          display: inline-block;
          text-align: center;
        }

      }
    lines:
      - num: "2-5"
        fade: true
      - num: 7
        text: |
          Here’s our media query—we do not repeat any of the above CSS in the media query because it adds onto what’s already there.

          At the `25em` breakpoint the only differences are that the `<li>` tags are side-by-side and centred—so no other CSS is written.

          **The media queries build on top of everything before them.**
    after: |
      Adjust the browser’s width over 400 pixels to see the navigation change:

      ![](small.png)

  - title: "Responsive typography"
    before: |
      As the screen sizes get bigger we want to make small adjustments to the typography so it looks better and fits better on the screen.

      The defaults for small and extra small screens are `100%/1.3`—which is great on tiny screens but too small and too tight on larger screens.

      So we incrementally enlarge the sizes as the screens get bigger.
    code_lang: css
    code_file: "css/main.css"
    code: |
      ⋮
          text-align: center;
        }

      }

      @media only screen and (min-width: 38em) {

        html {
          font-size: 110%;
          line-height: 1.4;
        }

      }

      @media only screen and (min-width: 60em) {

        html {
          font-size: 120%;
          line-height: 1.5;
        }

      }

      @media only screen and (min-width: 90em) {

        html {
          font-size: 130%;
        }

      }
    lines:
      - num: "2-5"
        fade: true
      - num: "9-12"
        text: |
          We target the `<html>` element to adjust the font-size because `rem` is based on it—so all the `rem` font-sizes we’ve specified naturally increase.

          Medium screens—`38em` get these settings:

          - A `font-size` of `110%`
          - A `line-height` of `1.4`
      - num: "18-21"
        text: |
          Large screens—`60em` get these settings:

          - A `font-size` of `120%`
          - A `line-height` of `1.5`
      - num: "27-29"
        text: |
          Extra large screens—`90em` get these settings:

          - A `font-size` of `130%`
          - We don’t need to change the `line-height` because it will just be inherited from the `60em` media query.
    after: |
      Play with the width of the browser window to see the font-size increase as the browser gets wider:

      ![](medium.png)

  - title: "Use more horizontal space"
    before: |
      As the browser window gets wider we should capitalize on the fact that we now have more horizontal space by putting the logo and the navigation on the same line.
    code_lang: css
    code_file: "css/main.css"
    code: |
      @media only screen and (min-width: 60em) {
        ⋮
        html {
          font-size: 120%;
          line-height: 1.5;
        }

        header {
          padding-left: 1rem;
          padding-right: 1rem;
          text-align: left;
        }

        h1,
        nav {
          display: inline-block;
          vertical-align: middle;
        }

        h1 {
          margin-bottom: 0;
          margin-right: 1.5rem;
        }

      }
      ⋮
    lines:
      - num: "3-6"
        fade: true
      - num: "14-18"
        text: |
          Change both the `<h1>` and the `<nav>` tag to `inline-block` so they sit beside each other on the same line.
      - num: 21
        text: |
          We need to remove the bottom `margin` from the `<h1>` because we added a margin further up in the CSS.

          **All the CSS above this media query is still in effect—our media query is just adding on top of what’s already there.**
    after: |
      Now our header uses the space more effectively on larger screens:

      ![](large.png)

  - title: "Media queries work together…"
    before: |
      *The media queries are always building on top of what’s above them.*

      Therefore the order that you put them in is important—smallest at the top & larger sizes as you go down the stylesheet.

      There are standard sizes that I almost always use [see the screen size cheat sheet for the defaults.](/topics/screen-sizes-cheat-sheet/)

      **But remember these are not the only sizes that you can use—use any size that makes sense for your design.**

---
