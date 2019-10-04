---
layout: slide-deck
title: "CSS introduction"
desc: "A quick introduction to CSS, what it is, what it does, and how to write it."

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

      ![The folder structure we’re following, a folder named “css” with a file named “main.css” inside.](folder-structure.jpg)
    notes: |
      You can name the CSS file whatever you want, but for this courses we’re going to standardize on `main.css` to make everything consistent for everybody.

      Also, it doesn’t have to be in a `css` folder to work, but it’s a good for organization and consistency.

      **Follow the naming conventions!**

  - type: image
    image: css.svg
    alt: "An example piece of CSS, h1 selector, with the colour set to purple."

  - type: image
    image: css-parts.svg
    alt: "The different parts of CSS code: rule set, selector, declaration, property & value."
    notes: |
      - **Rule set:** The whole chunk of CSS that changes how elements look.
      - **Selector:** The piece of code that tells the CSS which HTML element should be targeted.
      - **Declaration:** A fancy name for a line of CSS that changes the look of an element.
      - **Property:** A defined set of attributes about the look of HTML that can be changed.
      - **Value:** What that attribute’s style will be changed to.

  - type: interactive
    notes: |
      CSS works by targeting something in the HTML the changing is visual design properties.
    html: |
      <h1>Brontosaurus</h1>
      <p class="intro">The “Thunder Lizard” with a long neck and long tail.</p>
      <p>Not a <b>dinosaur</b> for a long time, but now, again, real.</p>
    css_lines:
      - num: 1
        text: "The selector, `html`, what element we want to change. The `html` element surrounds the whole page so it’s a good thing to target to change the background colour of the whole website."
      - num: 2
        text: "The `background-color` property changes the color *behind* the text. Make sure to spell “color” the American way."
      - num: 7
        text: "The `font-weight` property controls whether something is bold or not; setting `font-weight` to normal makes the text not bold."
      - num: 9
        text: "Selecting with a tag, like `p` will change every single `<p>` element. If we want to style some elements differently from others we can give them names, called classes. This selector will target only the elements that are named `.intro`"
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
    notes: |
      There are many different ways to specify colours in CSS, here are a few popular ones.
    html: |
      <h1>Brontosaurus</h1>
      <p class="intro">The “Thunder Lizard” with a long neck and long tail.</p>
      <p>Not a <b>dinosaur</b> for a long time, but now, again, real.</p>
    css_lines:
      - num: 2
        text: "There are ~256 color keywords built into CSS, I generally only use these for testing purposes and stick to the basics like `red`, `green`, `blue`, etc. I have never used `cornsilk` and probably never will."
      - num: 5
        text: |
          Probably the most common way to specify colours is using hex values; hex colours always start with a `#`. It’s a number made of 3 pieces (red, green & blue). It don’t pretend to know these numbers, I just copy and paste them from Photoshop, but I can guess at how light or dark the colour is based on the value.

          They’re called “hex” numbers because they are “hexadecimal” meaning not based on 10 digits, but 16 digits.

          To count hex you start at 0 and go to 9, then start at A and go to F:

          ```
          0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e, f
          ```
      - num: 8
        text: "If we want semi-transparent colours, the best way is to use `rgba`. The last number is the opacity of the color, a decimal between 0 and 1, so `.5` is 50% transparent; the lower the number the more transparent."
      - num: 9
        text: |
          If the hex colour is made of duplicated letters in 3 pairs, it can be shortened to use only one of each duplicate.

          - `#fff` expands to `#ffffff`
          - `#f00` -> `#ff0000`
          - `#f39` -> `#ff3399`
    css: |
      html {
        background-color: cornsilk;
      }
      b {
        color: #22bb22;
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
      ## Core typefaces

      - Arial
      - Verdana
      - Georgia
      - Times New Roman
      - Comic Sans *(um… really!?)*
      - Courier
      - Impact *(not as reliable)*
    notes: |
      We can guarantee that these typefaces will exist on every computer (as much as we can guarantee on the web).

      The only reason they exist is because Microsoft gave away all the typefaces in the early 90s to help the web be a consistent platform.

  - content: |
      ## Google Fonts

      Can’t just use any typeface available on your computer

      Google has many good typefaces (Typekit too)

      Include another CSS `<link>` tag
    notes: |
      As designers you’ll likely want to use more than just the default typefaces. That’s where online services like Google Fonts of Typekit help out. They provide large databases of properly web-licensed fonts for you to use on your website.

      You cannot just use any font that’s on your computer, like you can in print, because the user of the website would have to also have that font installed on their computer to view it properly. Not to mention the fact that almost all of the fonts on your computer aren’t licensed to be used on the web so it’d be illegal to use the in a website anyways.

  - content: |
      ## Font sizes

      Suggestions for the size to be displayed—user is always in control

      - **`rem` — scalable size based on browser settings**
      - `em` — scalable size based on parent element
      - `px` — don’t use for font-size—ever
    notes: |
      We are not—and shouldn’t be—in control of the font-size a person uses to view our website. They can increase or decrease the font-size however they want.

      Instead we specify a scale of font-sizes. Using the `rem` unit we can say that the font-size should be 1.5× larger than the body copy.

      The default font-size in browsers (assuming you didn’t change it) is `16px`. This is a nice readable size and you **should never** make the body copy small than that. So, translated to `rem`: *the body copy of your website should never be smaller than `1rem`*

  - content: |
      ## Videos & tutorials

      - [Using CSS ➔](/topics/using-css/)
      - [CSS indentation ➔](/topics/css-indentation/)
      - [CSS selectors & units cheat sheet ➔](/topics/css-selectors-units-cheat-sheet/)
      - [Basic typography ➔](/topics/basic-typography/)
      - [Using Google Fonts ➔](/topics/google-fonts/)
      - [Web typography cheat sheet ➔](/topics/web-typography-cheat-sheet/)

---
