---
layout: lesson
pair: true
title: "Dinosaur designs"
desc: "Work together in a pair to build this website and style its typography."

extra_tutorials:
  - title: "CSS introduction slide deck"
    url: /web-dev-1/css-introduction/
  - title: "Using CSS"
    url: using-css
  - title: "CSS indentation"
    url: css-indentation
  - title: "CSS selectors & units cheat sheet"
    url: css-selectors-units-cheat-sheet
    highlight: true
  - title: "Basic typography"
    url: basic-typography
  - title: "Using Google Fonts"
    url: google-fonts
  - title: "Web typography cheat sheet"
    url: web-typography-cheat-sheet
    highlight: true
  - title: "Validators"
    url: validators

goal:
  before: |
    We’re going to explore CSS selectors and properties to design the typography of a simple website.

    ### [Download the content and images.](https://github.com/acgd-webdev-1/dinosaur-designs/archive/gh-pages.zip)
  notes:
    - label: "Pair programming"
      text: |
        Each person will take turns being the **driver** and the **pointer**—switching at each denoted section.

        - **Driver** — controls the code editor, does the typing.
        - **Pointer** — has references open on their screen, guides the driver on what to type.

        **Together you’ll produce one coded project that you can share when complete.**
    - label: "Type it, type it real good"
      text: "Remember the purpose of this lesson is to type the code out yourself—build up that muscle memory in your fingers!"

steps:
  - title: "Set up project"
    before: |
      ### HTML setup

      1. Make a new folder named `dinosaur-designs`
      2. Move the `images` folder from the download into your `dinosaur-designs` folder
      2. Drag the `dinosaur-designs` folder into your code editor
      3. Make a new `index.html` file
      4. Add the HTML boilerplate code to `index.html`

      *Use the snippets we installed in the first class: `html5 — Tab`*

      ![](html5-snippet.gif)

      *And: `viewport — Tab`*

      ![](viewport-snippet.gif)

      ### CSS setup

      1. Make a new folder named `css` inside `dinosaur-designs`
      2. Create a new file named `main.css` and save it into the `css` folder
      3. Connect the HTML to the CSS

      *Use the snippet: `css — Tab`*

      ![](css-snippet.gif)

      ### Basic styling

      *Inside `main.css`:*

      1. Target the whole page and change the background colour to `#f2f1ed`
      2. Change the text on the whole page to `Georgia` with a backup font of `serif`
      3. Open in your browser—make the window narrower than normal

      *After you’re done the above steps it should look like this in your browser:*

      ![](goal-step-1.jpg)

  - title: "Style some content"
    before: |
      1. Add the logo into the HTML
      2. Add the first dinosaur image and content; look inside `content.txt` for text
      3. Add a width of `100%` to all images
      4. Make all the headings this green, `#5d8432`, and uppercase
      5. Make the image caption smaller, italic & centred

      *After you’ve done the above steps it should look like this in your browser:*

      ![](goal-step-2.jpg)

  - title: "Style the navigation"
    before: |
      1. Add the two remaining images and content
      2. Add the navigation & style it to match—[see the tutorial on styling links](http://learn-the-web.algonquindesign.ca/topics/basic-typography/#styling-links)
        — normal colour: `#793284`
        — `:hover` colour: `#b42885`

      *After you’re done the above steps it should look like this in your browser:*

      ![](goal-step-3.jpg)

  - title: "Web fonts"
    before: |
      1. Go to Google Fonts and find the Patua One typeface—[see the step-by-step tutorial](http://learn-the-web.algonquindesign.ca/topics/google-fonts/)
      2. Add it to a collection and use it
      3. Include the new font in your HTML
      4. Change the headings and the navigation to use the new font
      5. Make the caption on the first dinosaur larger than the rest

      *After you’re done the above steps it should look like this in your browser:*

      ![](goal.jpg)

---
