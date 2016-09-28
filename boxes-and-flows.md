---
layout: slide-deck

title: "Boxes & flows"

slides:
  - type: super-big-text
    content: |
      **Boxes and flows**

  - content: |
      ## Everything is a box

      Every single thing—every tag—is a box

      The browser uses a flow to lay out the page—like how Word or Pages works

  - type: interactive
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

  - type: image
    image: box-model-padding.svg

  - type: image
    image: box-model-border.svg

  - type: image
    image: box-model-margin.svg

  - type: image
    image: margin-order.svg

  - type: code-n-image
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
        text-align: center;           /* Only centres children, not the box itself */
      }

  - content: |
      ## Videos & tutorials

      - [Everything is a box ➔](/topics/box-model/)
      - [Flow & display ➔](/topics/flow-display/)
---
