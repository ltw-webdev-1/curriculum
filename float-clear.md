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

  - content: |
      ## Like inline-block but more precise

      ![](inline-block-float.png)

      *Inline-block will always have a little space between.*

  - content: |
      ## Float

      - `left`
      - `right`
      - `none` — helpful later for responsive sites

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

  - type: interactive
    html: |
      <div class="columns">
        <div class="col">Column 1</div>
        <div class="col">Column 2</div>
      </div>
    css_lines: 3
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

---
