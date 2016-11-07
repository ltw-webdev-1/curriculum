---
layout: lesson
title: "Making an image card"
desc: "Use CSS position absolute and relative to make an image card."

extra_tutorials:
  - title: "Position & z-index"
    url: position-zindex
  - title: "Position & z-index slide deck"
    url: /courses/web-dev-1/position-zindex/

markbot_notes: |
  *Ignore the “the first heading is an `<h2>`…” error message—but fix everything else.*

  I feel like these cards are part of a larger website so the `<h1>` would probably be somewhere else on the page.

goal:
  before: "We’re going to look at how to make the image card pattern, concentrating on position absolute and relative."
  notes:
    - label: "Important"
      text: "The two important bits are the “Plant-eater” label and the “Stegosaurus” heading and how they’re on top of the image."
    - label: "Type it, type it real good"
      text: "Remember the purpose of this lesson is to type the code out yourself—build up that muscle memory in your fingers!"

steps:
  - title: "Set up project"
    before: |
      Before we get started, create some files and get ready.
    folders:
      - label: "image-card"
        type: folder
      - label: "index.html"
        indent: 1
      - label: "css"
        type: folder
        indent: 1
      - label: "main.css"
        indent: 2
    after: |
      1. Create a folder named `image-card`
      2. Make an `index.html`
      3. Make a `main.css` in your `css` folder.
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
        <title>Image card</title>
        <meta name="viewport" content="width=device-width,initial-scale=1">
        <link href="css/main.css" rel="stylesheet">
      </head>
      <body>

      </body>
      </html>
    lines:
      - num: 7
        text: "Don’t forget to attach the CSS file."
    notes:
      - label: "HTML snippets"
        text: "Create the boilerplate with `html5`, `viewport` & `css`"

  - title: "Add CSS boilerplate"
    before: "*Use the `borderbox` snippet.*"
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      html {
        box-sizing: border-box;
        font-family: sans-serif;
      }

      *, *::before, *::after {
        box-sizing: inherit;
      }

      .img-flex {
        display: block;
        width: 100%;
      }
    lines:
      - num: "10-13"
        text: "Make a class to use on any image to make it scalable."

  - title: "Write the HTML for the card"
    before: "Let’s start with a little HTML before moving into the CSS guts."
    code_lang: "html"
    code_file: "index.html"
    code: |
      ⋮
      </head>
      <body>

        <article class="card">
          <header class="card-head">
            <h2 class="card-title">Stegosaurus</h2>
            <span class="card-label">Plant-eater</span>
            <img class="img-flex" src="http://placehold.it/640x480" alt="">
          </header>
          <div class="card-body">
            <p>The Stegosaurus is an armoured dinosaur with distinctive back plates and tail spikes.</p>
          </div>
        </article>

      </body>
      </html>
      ⋮
    lines:
      - num: "2-3"
        fade: true
      - num: 5
        text: "Semantically an `<article>` makes sense because this can stand by itself."
      - num: 6
        text: "The important bits are in the `<header>` because a group will be needed for CSS later."
      - num: 9
        text: "Don’t forget the `img-flex` class to make the image flexible."
      - num: "16-17"
        fade: true
    notes:
      - label: "Notice"
        text: "There’re classes on just about everything to distinguish them from other elements in our page."

  - title: "Some basic CSS for the card"
    before: "Before we get into the positioning stuff, let’s get the basic card look done."
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      ⋮
        display: block;
        width: 100%;
      }

      .card {
        overflow: hidden;
        border: 1px solid #ccc;
        border-radius: 0 6px 6px;
      }

      .card-body {
        padding: .2rem 1rem;
      }

      .card-title {
        margin: 0;
        padding: .3rem 1rem;
      }

      .card-label {
        padding: .3rem 1rem .3rem calc(1rem - 4px);
        border-left: 4px solid green;
        background-color: rgba(255, 255, 255, .6);
      }
    lines:
      - num: "2-4"
        fade: true
      - num: 7
        text: "The `overflow: hidden` is here to chop the corners of the image off."
      - num: 22
        text: |
          The crazy `calc()` is just really to make the text align properly when it also has a border.

          The `calc()` value allows us to get the browser to calculate between two different units.
    after: |
      With a refresh what you should see is this:

      ![](stage-1.jpg)

      **Make sure to shrink the width of your browser—the image card is completely flexible.**

  - title: "Position the card title"
    before: "Now let’s position the `.card-title` so that it sits at the bottom of the image."
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      .card-title {
        ⋮
        margin: 0;
        padding: .3rem 1rem;
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
      }
    lines:
      - num: "3-4"
        fade: true
      - num: 5
        text: "Setting it to `position: absolute` allows us to move it around using coordinates."
      - num: "6-7"
        text: "Using `left` and `bottom` to move it to the bottom of the image."
      - num: 8
        text: "The `width` is there because `absolute` elements shrink to be as small as possible."
    after: |
      Notice how the title is now at the bottom of the screen, that’s because the coordinates for `absolute` default to position against `<body>`

      ![](stage-2.jpg)

      **Make sure to shrink the width of your browser—the image card is completely flexible.**

  - title: "Fix card title position"
    before: |
      To fix the positioning of the `.card-title` we need to find a parent element that we can set `position: relative`

      Using `relative` will reset the coordinates so the `bottom` and `left` position against the parent container instead.

      *Luckily, it’s inside the `<header class="card-head">` tag. So let’s target that!*
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      ⋮
        border-left: 4px solid green;
        background-color: rgba(255, 255, 255, .6);
      }

      .card-head {
        position: relative;
      }
    lines:
      - num: "2-4"
        fade: true
      - num: 7
        text: "Using `position: relative` on this element will reset the coordinate system for all `absolute` children."
    after: |
      Now the `.card-title` snaps right into place.

      ![](stage-3.jpg)

  - title: "Position the card label"
    before: |
      Since the `.card-head` is already `relative` all we need to do is just put `absolute` and coordinates onto `.card-label`

      Because it’s parent container is `relative` it will automatically position itself against that box.
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      .card-label {
        ⋮
        padding: .3rem 1rem .3rem calc(1rem - 4px);
        border-left: 4px solid green;
        background-color: rgba(255, 255, 255, .6);
        position: absolute;
        left: 0;
        top: 0;
      }
    lines:
      - num: "3-5"
        fade: true
---
