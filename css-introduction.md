---
layout: slide-deck

title: "CSS introduction"

slides:
  - type: super-big-text
    content: |
      **CSS introduction**

  - content: |
      ## CSS — the look

      *The chocolate to our peanut*

      The only thing CSS knows how to do is make something look a certain way

      It doesn’t understand content—only style

  - content: |
      ## In a separate file — `main.css`

      ![](folder-structure.jpg)

  - type: image
    image: css.svg

  - type: image
    image: css-parts.svg

  - type: interactive
    html: |
      <h1>Brontosaurus</h1>
      <p class="intro">The “Thunder Lizard” with a long neck and long tail.</p>
      <p>Not a <b>dinosaur</b> for a long time, but now, again, real.</p>
    css_lines: "1,2,7,9"
    css: |
      html {
        background-color: cornsilk;
        font-family: Georgia, serif;
      }
      b {
        color: forestgreen;
        font-weight: normal;
      }
      .intro {
        color: darkolivegreen;
        font-style: italic;
      }
    css_hidden: |
      html {
        font-size: 2.5rem;
      }

  - type: interactive
    html: |
      <h1>Brontosaurus</h1>
      <p class="intro">The “Thunder Lizard” with a long neck and long tail.</p>
      <p>Not a <b>dinosaur</b> for a long time, but now, again, real.</p>
    css_lines: "2,5,8,9"
    css: |
      html {
        background-color: cornsilk;
      }
      b {
        color: #228b22;
      }
      .intro {
        background-color: rgba(85, 107, 47, .4);
        color: #fff;
      }
    css_hidden: |
      html {
        font-size: 2.5rem;
        font-family: Georgia, serif;
      }

  - type: code
    css: |
      h1 {
        background-color: #f2f1ed;      /* Colour behind text */
        color: #222;                    /* Text colour */
        font-family: Georgia, serif;    /* Suggested typeface & backup */
        font-size: 2rem;                /* Suggested size of the type */
        font-style: italic;             /* Italic or normal */
        font-weight: bold;              /* Bold, normal, or number like 200 */
        line-height: 1.5;               /* Multiplier against the size */
        list-style-type: square;        /* Bullets: none, circle, decimal, lower-alpha, etc. */
        text-align: center;             /* Left, right, center, justify */
        text-decoration: underline;     /* Underline or none */
        text-transform: uppercase;      /* Uppercase, lowercase */
      }
      img {
        width: 100%;                    /* Make the width fill the whole space */
      }

  - content: |
      ## Font sizes

      Suggestions for the size to be displayed—user is always in control

      - **`rem` — scalable size based on browser settings**
      - `em` — scalable size based on parent element
      - `px` — don’t use for font-size—ever

  - content: |
      ## Core typefaces

      - Arial
      - Verdana
      - Georgia
      - Times New Roman
      - Comic Sans *(um… really!?)*
      - Courier
      - Impact *(not as reliable)*

  - content: |
      ## Google Fonts

      Can’t just use any typeface available on your computer

      Google has many good typefaces (Typekit too)

      Include another CSS `<link>` tag

  - content: |
      ## Videos & tutorials

      - [Using CSS ➔](/topics/using-css/)
      - [CSS indentation ➔](/topics/css-indentation/)
      - [CSS selectors & units cheat sheet ➔](/topics/css-selectors-units-cheat-sheet/)
      - [Basic typography ➔](/topics/basic-typography/)
      - [Using Google Fonts ➔](/topics/google-fonts/)
      - [Web typography cheat sheet ➔](/topics/web-typography-cheat-sheet/)

---
