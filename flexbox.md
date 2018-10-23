---
layout: slide-deck
title: "Flexbox"
desc: "A quick introduction to the CSS Flexbox properties, how they work and what they do."

slides:
  - type: super-big-text
    content: |
      **Flexbox**

  - content: |
      ## Side-by-side

      Use Flexbox to get things beside other things

      ![](flexbox.png)

  - content: |
      ## Like inline-block but more precise

      ![](inline-block-flex.png)

      *Inline-block will always have a little space between—where flexboxes can touch.*

  - content: |
      ## Works on children

      Many of the flexbox properties are applied to the parent element, but affect the child elements.

      *This is different from many other CSS properties that directly affect the selected element.*

  - content: |
      ## Flexbox

      - **`display: flex`** — turn the system on
      - `flex-direction: row` — make all the children go side-by-side
      - `justify-contents` — control the spacing around the children
      - `align-items` — control the space above/below the children

  - type: interactive
    html: |
      <div class="columns">
        <div class="col">Column 1</div>
        <div class="col">Column 2</div>
      </div>
    css: |
      .columns {
        display: flex;
        flex-direction: row;
      }
      .col {
        width: 50%;
        background-color: yellow;
      }
    css_lines:
      - num: 2
        text: |
          We’re targeting all the child elements with the `.columns` class and applying a flexbox layout to them.
      - num: 3
        text: |
          We don’t have to specify `flex-direction` if we want `row`—that’s the default. I’ve added it here just be more explicit.

  - type: interactive
    html: |
      <div class="columns">
        <div class="col">Column 1</div>
        <div class="col">Column 2</div>
      </div>
    css: |
      .columns {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
      }
      .col {
        background-color: yellow;
      }
    css_lines:
      - num: 4
        text: |
          Without a width the flexbox’d elements will shrink to their smallest size. We can control how they are arranged using the `justify-content` property.

          - `space-between` — push them to the edges and distribute space between them evenly
          - `space-around` — distribute even space on the sides of the boxes, meaning they will no longer touch the edges

  - type: interactive
    html: |
      <div class="columns">
        <div class="col">Column 1</div>
        <div class="col">
          <h2>Column 2</h2>
        </div>
      </div>
    css: |
      .columns {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
      }
      .col {
        background-color: yellow;
      }
    css_lines:
      - num: 5
        text: |
          The `align-items` property allows us to control the *vertical†* alignment of the elements in a row.

          - `center` — align their centres within the parent box
          - `stretch` — force the elements to be exactly the same height
          - `flex-start` — align them to the top
          - `flex-end` — align them to the top

          † “Vertical” is a real simplification because Flexbox can actually work vertically too, so `align-items` technically works on the “cross axis” of the flex container. [Learn more about flexbox axes ➔](/topics/flexbox/#flexbox-axes)

  - content: |
      ## Videos & tutorials

      - [Flexbox ➔](/topics/flexbox/)
      - [Flexbox cheat sheet ➔](/topics/flexbox-cheat-sheet/)
      - [CSS layout cheat sheet ➔](/topics/css-layout-cheat-sheet/)

---
