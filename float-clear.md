---
layout: slide-deck
title: "Float & clear"
desc: "A quick introduction to the CSS float & clear properties, how they work and what they do."

slides:
  - type: super-big-text
    content: |
      **Float & clear**

  - content: |
      ## Side-by-side

      - Use `float` to get things beside other things
      - Or to have text wrap around something

      ![](float.png)
    notes: |
      The primary, original, purpose of `float` is to do very basic text wrapping. We’re really misusing it to create layouts & columns.

      There are newer, better solutions, like [Flexbox](/topics/advanced-layout-systems/), but they also introduce more complexity.

  - content: |
      ## Like inline-block but more precise

      ![](inline-block-float.png)

      *Inline-block will always have a little space between—where floated boxes can touch.*

  - content: |
      ## Float

      - `left`
      - `right`
      - `none` — helpful later for responsive sites
    notes: |
      There are three options for `float`:

      - `left` — moves the element to the left, wrapping text around the right
      - `right` — moves the element to the right, wrapping text around the left
      - `none` — disables the `float` and will be helpful later with responsive websites

  - content: |
      ## Almost always add width

      ```css
      .column {
        float: left;
        width: 25%;
      }
      ```

  - type: interactive
    html: |
      <div class="columns">
        <div class="col">Column 1</div>
        <div class="col">Column 2</div>
      </div>
    css: |
      .col {
        float: left;
        width: 50%;
        background-color: yellow;
      }
    css_lines:
      - num: 1
        text: |
          We’re targeting all the elements with the `.col` class and floating them the same way—making two equal width columns.

  - type: interactive
    html: |
      <div class="columns">
        <div class="col">Column 1</div>
        <div class="col">Column 2</div>
      </div>
    css: |
      .columns {
        border: 3px solid red;
      }
      .col {
        float: left;
        width: 50%;
        background-color: yellow;
      }
    notes: |
      If we put a border around the parent element you’ll see that it has no height. When elements are floated they’re removed from the browsers flow and don’t take up any space inside their parent element.

      **If everything inside an element is floated that element will collapse to a height of `0px`**

      *This isn’t a problem with the newer [Flexbox](/topics/advanced-layout-systems/) layout system.*
  - type: interactive
    html: |
      <div class="columns">
        <div class="col">Column 1</div>
        <div class="col">Column 2</div>
      </div>
    css_lines:
      - num: 3
        text: |
          The solution to the problem, of the parent element collapsing, is called a “clearfix”. There are many different ways to “clearfix” but the simplest is to just apply `overflow: hidden` to the parent element.

          *With [Flexbox](/topics/advanced-layout-systems/) we don’t have to worry about any “clearfix” stuff.*
    css: |
      .columns {
        border: 3px solid red;
        overflow: hidden; /* Simple clearfix */
      }
    css_hidden: |
      .col {
        float: left;
        width: 50%;
        background-color: yellow;
      }

  - type: interactive
    html: |
      <div class="columns clearfix">
        <div class="col">Column 1</div>
        <div class="col">Column 2</div>
      </div>
    css: |
      /* Alternative clearfix */
      .clearfix::after {
        content: " ";
        display: block;
        clear: both;
      }
    css_hidden: |
      .columns {
        border: 3px solid red;
      }
      .col {
        float: left;
        width: 50%;
        background-color: yellow;
      }
    notes: |
      If `overflow: hidden` isn’t doing what you want, because we’re abusing it for one of its unindented side-effects, you can try this `.clearfix` class.

  - content: |
      ## Clearing

      **You almost always have to clearfix the parent of floated elements.**

      1. `overflow: hidden`
        — Can clearfix parents, but also crops

      2. `.clearfix {…}`
        — More reliable, more code

  - content: |
      ## Videos & tutorials

      - [Float & clear ➔](/topics/float-clear/)
      - [CSS layout cheat sheet ➔](/topics/css-layout-cheat-sheet/)

---
