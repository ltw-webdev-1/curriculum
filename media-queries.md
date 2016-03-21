---
layout: slide-deck

title: "Media queries"

slides:
  - type: super-big-text
    content: |
      **Media queries**

  - content: |
      ## The Web is for everybody

      It’s our job as web designers to make our website work in as many situations as possible

      **The web is responsive by default—if it doesn’t work on a specific device it’s your fault!**

  - type: code
    html: |
        <!-- Tells the browser we support whatever size it is & not to zoom in -->
        <meta name="viewport" content="width=device-width,initial-scale=1">
    css: |
      /* Same as the HTML viewport, but for different browsers */
      @-moz-viewport { width: device-width; scale: 1; }
      @-ms-viewport { width: device-width; scale: 1; }
      @-o-viewport { width: device-width; scale: 1; }
      @-webkit-viewport { width: device-width; scale: 1; }
      @viewport { width: device-width; scale: 1; }

      html {
        /* Tells the browser not to automatically scale the fonts—we want complete control */
        -moz-text-size-adjust: 100%;
        -ms-text-size-adjust: 100%;
        -webkit-text-size-adjust: 100%;
        text-size-adjust: 100%;
      }

  - content: |
      ## Media queries

      Detect the dimensions of the user’s screen and make layout adjustments

      - minimum width/height, orientation

      ---

      ### Or other things

      - print, black & white, retina, touch, mouse, etc.

  - content: |
      ## Do not use pixels—use em

      Try to avoid using pixels in media queries—they make us think in terms of devices instead of content

      **Our media queries should be based on content irregularities not on device sizes**

  - content: |
      ## Converting px to em

      Divide by 16 (the browser’s default size)

      ```
      400px ÷ 16 = 25em
      960px ÷ 16 = 60em
      ```

  - content: |
      ## Common media query widths

      - `25em` — small screens
      - `38em` — medium screens
      - `60em` — large screens
      - `90em` — extra large screens

      *I found these numbers work for me based on making lots of websites and seeing what numbers appear*

  - content: |
      ## Always start small!

      Media queries compound on top of each other and rely on the previous CSS

      1. Design for the small screen first
      2. Add media queries when the content becomes awkward

      **Do not start on large screens first—it doubles the amount of CSS you need to write!**

  - type: interactive
    resizeable: true
    html: |
      <h1>Media queries</h1>
    css: |
      h1 {
        background-color: red;
      }

      @media only screen and (min-width: 25em) {
        h1 {
          background-color: green;
        }
      }

      @media only screen and (min-width: 38em) {
        h1 {
          background-color: yellow;
        }
      }

  - type: interactive
    resizeable: true
    html: |
      <ul>
        <li>Pteranodon</li>
        <li>Quetzalcoatlus</li>
      <ul>
    css: |
      ul {
        padding: 0;
        list-style-type: none;
      }
      li {
        padding: .5em .7em;
        background-color: #00675a;
        color: #fff;
      }
      @media only screen and (min-width: 60em) {
        ul { text-align: center; }
        li { display: inline-block; }
      }

  - type: code
    html: |
      <header>
        <h1>Quetzalcoatlus</h1>
        <nav>
          <ul>
            <li><a href="#env">Environment</a></li>
            <li><a href="#diet">Diet</a></li>
            <li><a href="#size">Dimensions</a></li>
          </ul>
        </nav>
      </header>
    css: |
      @media print {
        nav {
          display: none;
        }
      }

  - content: |
      ## Videos & tutorials

      - [All devices setup ➔](/topics/all-devices-setup/)
      - [Media queries ➔](/topics/media-queries/)
      - [Screen sizes cheat sheet ➔](/topics/screen-sizes-cheat-sheet/)

---
