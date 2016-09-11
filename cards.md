---
layout: lesson
title: "Cards"
desc: "Dig into the browser’s layout models to make a simple, flexible informational design."

extra_tutorials:
  - title: "Everything is a box"
    url: box-model
  - title: "Flow & display"
    url: flow-display
  - title: "Browser developer tools"
    url: browser-developer-tools

goal:
  before: "We’re going to walk through writing some HTML and CSS to generate an informational layout."
  notes:
    - label: "Type it, type it real good"
      text: "Remember the purpose of this lesson is to type the code out yourself—build up that muscle memory in your fingers!"

steps:
  - title: "Set up the project"
    before: |
      Set up a folder on your computer and get things ready to go.
    folders:
      - label: "cards"
        type: folder
      - label: "index.html"
        indent: 1
      - label: "css"
        type: folder
        indent: 1
      - label: "main.css"
        indent: 2
    after: |
      1. Create a new folder named `cards`
      2. Make a new `index.html` file in your `cards` folder.
      3. Make a new `main.css` in your `css` folder.
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
        <title>Cards</title>
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
      }

      *, *::before, *::after {
        box-sizing: inherit;
      }
    notes:
      - label: "CSS snippets"
        text: "Create the boilerplate with `borderbox`"
    after: "The `border-box` system changes the browsers layout math to include the `padding` in the `width`—the default is more difficult to manage when making flexible, responsive websites."

  - title: "Write the card HTML"
    before: |
      For the cards, an unordered list makes sense because the website is a list of space probes.
    code_lang: "html"
    code_file: "index.html"
    code: |
      ⋮
        <link href="css/main.css" rel="stylesheet">
      </head>
      <body>

        <ul class="cards">

          <li>
            <img src="http://placehold.it/32x32" alt="">
            <strong>Voyager 1</strong>
            <dl>
              <dt>Launched:</dt>
              <dd><time datetime="1977-09-05">Sept. 5, 1977</time></dd>
              <dt>Destination:</dt>
              <dd>Jupiter & beyond</dd>
            </dl>
            <div>
              <a href="https://en.wikipedia.org/wiki/Voyager_1">Wikipedia</a>
            </div>
          </li>

          <!-- Copy and paste the above <li> here to make the second card -->

        </ul>

      </body>
      </html>
      ⋮
    lines:
      - num: "2-4"
        fade: true
      - num: 6
        text: "Add a `class` to the `<ul>` so we can style it directly."
      - num: 9
        text: |
          We’re using an image placeholder service to make an image for us—that way we don’t have to go into Photoshop to create a new image.

          The `32x32` part is the pixel dimensions of the image we want. [You can see more options on the PlaceHold.it website.](https://placehold.it/)
      - num: 10
        text: "The `<strong>` tag makes semantic sense because the name of the probe is more important than the surrounding text."
      - num: "17-19"
        text: "There’s a semantically meaningless `<div>` tag here that we’re going to use as a CSS styling hook later."
      - num: "26-27"
        fade: true
    after: |
      **Copy the `<li>` tag you wrote above and paste it in the place of the comment. Change its details to reflect the “New Horizons” probe.**

      *This is what you should see in your browser:*

      ![](after-html.jpg)

  - title: "Basic CSS styles"
    before: |
      Let’s add some basic CSS style to make the website look a little nicer.
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      html {
        box-sizing: border-box;
        background-color: #f2f2f2;
        font-family: Georgia, serif;
        line-height: 1.5;
      }

      *, *::before, *::after {
        box-sizing: inherit;
      }
    lines:
      - num: 2
        fade: true
      - num: "3-5"
        text: "Adjust the `background-color`, `font-family` and `line-height` to make it look a little more pleasant."
      - num: "8-10"
        fade: true
    after: |
      *This is what you should see in your browser:*

      ![](css-basics.jpg)

  - title: "Style the boxes"
    before: |
      Next up we’ll style the card itself by adding some colours, borders, and sizes.
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      ⋮
      *, *::before, *::after {
        box-sizing: inherit;
      }

      .cards {
        margin: 0;
        padding: 0;
        list-style-type: none;
      }

      .cards li {
        display: inline-block;
        margin: 0 .5em 1em .5em;
        max-width: 20em;
        padding: 1em;
        background-color: #fff;
        border: 3px solid #e2e2e2;
        border-radius: 10px;
      }
    lines:
      - num: "2-4"
        fade: true
      - num: "7-9"
        text: "By using the developer tools I know that the `<ul>` has `margin`, `padding`, and `list-style-type` on it by default—this code will reset the defaults provided by the browser."
      - num: 12
        text: "Use a child selector to get the `<li>` tags inside of `.cards`"
      - num: 13
        text: "The `<li>` tags are `display: block` by default, which makes them go on their own lines. This code will change them to `inline-block` allowing them to sit beside each other."
      - num: 14
        text: |
          The `margin` property adds space **outside** of the box.

          This `margin` is composed of four values:

          1. top
          2. right
          3. bottom
          4. left

          Start at the top and work clockwise around the box.
      - num: 15
        text: "Using `max-width` allows the boxes can scale up to only a certain size."
      - num: 16
        text: |
          The `padding` property will add spacing **inside** the box.

          Padding can have four values like margin or only one value that will affect all four sides. (Margin does this too.)
      - num: 18
        text: |
          The `border` property allows us to add a stroke around the outside of a box.

          Borders require three pieces of information:

          1. The thickness, usually in pixels.
          2. The style: `solid`, `dotted`, `dashed`, etc.
          3. The border’s colour.
      - num: 19
        text: "The `border-radius` property allows us to round the corners of a box."
    after: |
      *This is what you should see in your browser when the window’s width is small:*

      ![](card-s.jpg)

      *And when the width is a little wider:*

      ![](card-l.jpg)

      **Notice how we’re taking advantage of the browser’s flow:**

      - When there isn’t enough space the boxes stack on top of each other.
      - When there is enough space they fit beside each other on the same line.

      *This is because we’re using `display: inline-block` on the `<li>` tags.*

  - title: "Centering the boxes"
    before: |
      It would look a little better if the boxes were centred on the screen instead of flush-left.
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      ⋮
      *, *::before, *::after {
        box-sizing: inherit;
      }

      .cards {
        ⋮
        padding: 0;
        list-style-type: none;
        text-align: center;
      }

      .cards li {
        ⋮
        border: 3px solid #e2e2e2;
        border-radius: 10px;
        text-align: left;
      }
    lines:
      - num: "2-4"
        fade: true
      - num: "8-9"
        fade: true
      - num: 10
        text: |
          Because the `<li>` tags are `inline-block` we can use `text-align: center`, which works on all `inline` and `inline-block` elements.

          **We need to put `text-align: center` on a parent element so that it affects all of its children.**
      - num: "15-16"
        fade: true
      - num: 17
        text: "Because we set everything inside `.cards` to be centred that would affect all the text too, but we only want to center the boxes not the text—so we have to reset the interior of the boxes to `text-align: left`"
    after: |
      *This is what you should see in your browser when the window’s width is small:*

      ![](center-s.jpg)

      *And when the width is a little wider:*

      ![](center-l.jpg)

  - title: "Style the image and text"
    before: |
      Let’s concentrate on the inside of the boxes by styling the small image and some of the text.
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      ⋮
        border: 3px solid #e2e2e2;
        border-radius: 10px;
        text-align: left;
      }

      .cards img {
        display: block;
        margin: 0 auto 1rem auto;
      }

      .cards strong {
        display: block;
        margin-bottom: 1rem;

        font-size: 1.125rem;
      }

      .cards dl {
        margin-bottom: 1rem;
      }
    lines:
      - num: "2-5"
        fade: true
      - num: 8
        text: "The `display: block` will put the image on its own line instead of beside the probe’s name."
      - num: 9
        text: |
          The image will look better centred, but because the image is `block` `text-align: center` no longer works. Instead we can use automatic left and right margins.

      - num: "13-14"
        text: "Adding `margin` to a `<strong>` tag doesn’t work by default because `<strong>` tags are `inline`—margins only work on `block` and `inline-block`"
      - num: 20
        text: "Add a little space after the `<dl>` to push the “Wikipedia” link further down."
    after: |
      *This is what you should see in your browser:*

      ![](spacing.jpg)

  - title: "Style the data list"
    before: "Using the `display` property and some widths we can style the `<dl>` so that the `<dt>` and `<dd>` tags are on the same line."
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      ⋮
      .cards dl {
        margin-bottom: 1rem;
      }

      .cards dt {
        display: inline-block;
        width: 6em;
        font-style: italic;
      }

      .cards dd {
        display: inline-block;
        margin: 0;
        min-width: 9em;
      }
    lines:
      - num: "2-4"
        fade: true
      - num: 7
        text: "Setting both the `<dt>` and `<dd>` tags to `display: inline-block` (overwriting the browser’s default `block`) will allow them to be on the same line."
      - num: 8
        text: |
          By adding a `width` to the `<dt>` tag we can get a nice alignment of all the `<dd>` tags.

          The `width` is set in `em` units so that it can grow with the font size.
      - num: 15
        text: "Adding a `min-width` to the `<dd>` tags will force the `<dt>` tag that follows onto its own line."
    after: |
      *This is what you should see in your browser:*

      ![](dls.jpg)

  - title: "Style the links"
    before: "Using display and a few other box properties we can make the `<a>` tags look like full buttons."
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      ⋮
        margin: 0;
        min-width: 9em;
      }

      .cards div {
        text-align: center;
      }

      .cards a {
        display: inline-block;
        padding: .5em .75em;
        background-color: #ccc;
        border-radius: 4px;
        color: #000;
        text-decoration: none;
      }

      .cards a:hover {
        background-color: #333;
        color: #fff;
      }
    lines:
      - num: "2-4"
        fade: true
      - num: 7
        text: |
          Using the `<div>` that surrounds the `<a>` tag we can centre the link.

          - If we were to put `text-align: center` directly on the link only the text inside it would be affected—because `text-align` only targets children.
          - We can’t use `auto` margins because that only works on `display: block` elements, and we don’t want the link to stretch all the way across.
      - num: 11
        text: "Adding `display: inline-block` to the `<a>` tag will allow us to add `padding` since padding doesn’t work well on `inline` elements."
      - num: 16
        text: "It’s okay to remove the `underline` from links when they are distinctly separate from the body copy. In this case it’s okay because the link looks like a button."
      - num: 19
        text: "Don’t forget to add a `:hover` state to the link."
    after: "**Test it in your browser to make sure it looks like the goal at the top.**"
---
