---
layout: slide-deck
title: "Boxes & flows"
desc: "A quick introduction to how the browser displays a website & the CSS box model."

slides:
  - type: super-big-text
    content: |
      **Boxes and flows**

  - content: |
      ## Everything is a box

      Every single thing—every tag—is a box

      The browser uses a flow to lay out the page—like how Word or Pages works
    notes: |
      Like Microsoft Word, web browsers will attempt to fit an element on the same line as the previous element unless there isn’t enough space.

      When the space on a “line” runs out the element will be moved to the line below.

      There are a whole whack CSS properties to control this flow and control how elements are situated and displayed.

  - type: interactive
    notes: |
      In CSS there is a property named `display`, this helps control the flow of the HTML elements.

      There are 3 basic values to `display`:

      1. `inline` — essentially just text, allows elements on the same line, but elements will get broken when wrapped to multiple lines.
      2. `block` — force the element to be on its own line regardless of its width.
      3. `inline-block` — a combination of `inline` & `block`: allows elements on the same line, but won’t get broken when it wraps.
    resizable: true
    html: |
      <!--
        # Flow control

        Boxes are controlled by:

        - The available space
        - The display property
      -->
    html_hidden: |
      <p class="inline-wrap">
        <span class="">Inline</span>
        <span class="">Inline</span>
        <span class="">Inline</span>
        <span class="">Inline</span>
        <span class="with-width">Inline with width</span>
      </p>
      <div class="">Block</div>
      <span class="ib">Inline-block</span>
      <span class="ib">Inline-block</span>
      <span class="ib">Inline-block</span>
      <div class="with-width margin-fixer">Block with width</div>
      <div class="with-width-2">Block with width</div>
      <span class="ib with-width">Inline-block with width</span>
      <span class="ib">Inline-block</span>
    css_hidden: |
      html {
        box-sizing: border-box;
        font-size: 1rem
      }
      *, *::before, *::after {
        box-sizing: inherit;
      }
      body {
        font-family: "Source Code Pro", monospace;
      }
      span {
        border: 3px solid #c883d4;
      }
      .inline-wrap {
        margin: 0;
        padding: .4em 0;
      }
      .ib {
        display: inline-block;
        padding: 1em;
        margin: .2em 0;
        text-align: center;
      }
      div {
        padding: 1em;
        margin: .2em 0;
        border: 3px solid #672373;
        text-align: center;
      }
      .with-width {
        width: 50%;
      }
      .with-width-2 {
        width: 40%;
      }
      .margin-fixer {
        margin-bottom: .4em;
      }

  - type: code
    css: |
      div {
        /* Default: flows with the browser
           CANNOT have margin, padding, width
           <span>, <a>, <strong>, <em>, etc. */
        display: inline;

        /* Forced onto a single line
           CAN have margin, padding, width
           <h1>, <p>, <div>, <figure>, etc. */
        display: block;

        /* Flows with the browser
           CAN have margin, padding, width
           <img>, etc. */
        display: inline-block;
      }

  - type: image
    image: box-model-content.svg
    notes: |
      The CSS box models starts with the content, which defines the basic box.

  - type: image
    image: box-model-padding.svg
    notes: |
      Next to the content, pushing the edge of the box away is called `padding`

  - type: image
    image: box-model-border.svg
    notes: |
      At the edge of the `padding` is a stroke around the edges of the box called `border`

  - type: image
    image: box-model-margin.svg
    notes: |
      Outside the border, pushing other boxes away, is called `margin`

  - type: image
    image: margin-order.svg
    notes: |
      Since a box has 4 sides, we can specify different `margin`, `padding` and `border` for each side.

      When specifying `margin` or `padding` we can write 1–4 numbers.

      - 1 number specifies a margin (or padding) on all 4 sides
      - 2 numbers: top/bottom & left/right
      - 3 numbers: top, left/right, bottom

      Then we writing 4 numbers we’re specifying all different sizes, starting at the top and working around the box clockwise: top, right, bottom, left.

  - type: code-n-image
    notes: |
      Browser’s have a few different layout width calculation models. The default is called `content-box` and the one we’re **always** going to use is called `border-box`. When making responsive websites `border-box` simplifies the math.

      With the default `content-box` if we specify a `width` the actual layout width is not what we specify but the sum of the `width` + `padding` + `border` so our layouts become cumbersome because we always have to make mathematical choices.

      With `border-box` the `width` we define is the final `width`: `border` and `padding` are inside what we define, making the math inconsequential.
    image: border-box.svg
    css: |
      /*
        Reset the layout math:
        - the padding is inside the width
        - friendlier for flexible layouts

        Put this at the top of EVERY CSS file
      */

      html {
        box-sizing: border-box;
      }

      *, *::before, *::after {
        box-sizing: inherit;
      }

  - content: |
      ## Centering boxes

      `text-align: center`
      — works on children only
      — only works on `inline` and `inline-block`

      `margin: 0 auto`
      — works on the box directly
      — only works on `block`

  - type: code
    css: |
      div {
        width: 50%;                   /* Control the size of a box */
        max-width: 20em;              /* Stop the box from growing wider than defined */
        min-width: 5em;               /* Stop the box from shrinking smaller than defined */
        border: 1px solid #000;       /* Add a stroke around the outside of the box */
                                      /*   border: thickness style color; */
        border-radius: 10px;          /* Add rounded corners to a box */
        box-shadow: 1px 1px 5px #000; /* Add a drop shadow to a box */
                                      /*   box-shadow: x-offset y-offset blur-radius color; */
        margin: 1rem auto 2rem auto;  /* 4 sides individually: top right bottom left */
                                      /*   `auto` allows a display block box to centre */
        padding: 1em;                 /* All 4 sides the same */
        display: inline-block;        /* inline, block, inline-block */
        vertical-align: middle;       /* Shift elements up & down to align different positions */
        text-align: center;           /* Only centres children, not the box itself */
      }

  - content: |
      ## Videos & tutorials

      - [Everything is a box ➔](/topics/box-model/)
      - [Flow & display ➔](/topics/flow-display/)
      - [Boxes & borders cheat sheet ➔](/topics/boxes-borders-cheat-sheet/)
      - [CSS layout cheat sheet ➔](/topics/css-layout-cheat-sheet/)

---
