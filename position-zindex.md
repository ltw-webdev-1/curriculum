---
layout: slide-deck
title: "Position & z-index"
desc: "A quick overview of how CSS positioning works with relative & static and a small intro to z-index."

slides:
  - type: super-big-text
    content: |
      **Position & z-index**

  - content: |
      ## position

      - Turn on coordinate-based movement
      - *or* Control the coordinate container

  - content: |
      `position: static`

      - the default

      `position: absolute`

      - move with coordinates

      `position: relative`

      - reset coordinates
      - always on parent container

  - type: image
    image: position-1.svg
    notes: |
      There are two boxes inside another box on the page.

  - type: image
    image: position-2.svg
    notes: |
      If the first box is set to `position: absolute` the second box will layout itself as if the first box didn’t exist.

      Without coordinates the `absolute` element will stay in the same place it would have before being set to `position: absolute`

      When an element has `position: absolute` set, it will collapse to be as small as it can be.

  - type: image
    image: position-3.svg
    notes: |
      When coordinates are used, like `top: 0` & `right: 0` the box will move to be positioned against the edges of the `<body>` tag.

  - type: image
    image: position-4.svg
    notes: |
      We can set `position: relative` onto a parent element of the first box and the coordinate system will be reset to be based upon the parent element’s position instead of `<body>`

      The `<body>` element is the only element that’s `position: relative` by default, which is why `absolute` elements coordinate with the `<body>` if their parent elements don’t set `position: relative`

  - type: interactive
    html: |
      <div class="banner">
        <img src="placeholder-16by9.svg" alt="">
        <div class="banner-content">
          <h2>Free Mars!</h2>
          <p>The Free Mars Coalition needs your help to take back our planet.</p>
        </div>
      </div>
    css: |
      .banner {
        position: relative;
      }
      .banner-content {
        padding: 0 1rem;
        position: absolute;
        bottom: 1rem;
      }
    css_lines:
      - num: 2
        text: |
          By setting the parent element to `relative` all the coordinates of the children elements will be “relative” to the parent instead of the `<body>`
    css_hidden: |
      html {
        font-size: 200%;
      }
      img {
        display: block;
        width: 100%;
      }
      h2 {
        margin: 0;
      }
      p {
        margin: 0;
      }

  - content: |
      `z-index: 10`

      - Controls layering
      - Higher number is closer to you
      - Only on `absolute` or `relative` elements

      *Like layers in Photoshop or Illustrator: higher up in the palette is closer*

  - type: image
    image: z-index-1.svg
    notes: |
      With two elements set to `position: absolute` the element further down in the HTML code will be closer to you in the layers and therefore cover the earlier element.

  - type: image
    image: z-index-2.svg
    notes: |
      If the first element sets `z-index` it will come to the front.

      The `z-index` number has to be higher than the number of layers to force it to the front. In this example, since there are 2 boxes, `z-index: 2` is sufficient to bring it to the front.

      Most of the time when I use `z-index` I set it to something ridiculously high, like `1000`, because my whole purpose is to “bring the thing to the front no matter what”.

  - content: |
      ## Videos & tutorials

      - [Position & z-index ➔](/topics/position-zindex/)
      - [CSS layout cheat sheet ➔](/topics/css-layout-cheat-sheet/)

---
