---
layout: slide-deck

title: "Position & z-index"

slides:
  - type: super-big-text
    content: |
      **Position & z-index**

  - content: |
      ## position

      - Turn on coordinate-based movement
      - Control the movement container

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

  - type: image
    image: position-2.svg

  - type: image
    image: position-3.svg

  - type: image
    image: position-4.svg

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

      - controls layering
      - higher number is closer to you
      - only on `absolute` or `relative` elements

  - type: image
    image: z-index-1.svg

  - type: image
    image: z-index-2.svg

  - content: |
      ## Videos & tutorials

      - [Position & z-index ➔](/topics/position-zindex/)

---
