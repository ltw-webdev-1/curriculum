---
layout: lesson
title: "Dinosaur designs"
desc: "Work to build this website and style its typography."

markbot_submit: true
hide_show_for_marks: true

extra_tutorials:
  - title: "CSS introduction slide deck"
    url: /courses/web-dev-1/css-introduction/
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
  notes:
    - label: "Type it, type it real good"
      text: "Remember the purpose of this lesson is to type the code out yourself—build up that muscle memory in your fingers!"

fork:
  url: "https://github.com/acgd-webdev-1/dinosaur-designs/"

steps:
  - title: "Set up project"
    before: |
      After cloning the repository to your computer you should have some starter images.

      **Drag the `dinosaur-designs` folder to Atom and make an HTML file & a CSS file.**
    folders:
      - label: "dinosaur-designs"
        type: folder
      - label: "index.html"
        indent: 1
      - label: "css"
        type: folder
        indent: 1
      - label: "main.css"
        indent: 2
      - label: "images"
        type: folder
        indent: 1
        fade: true
        notes: "Already full of images to use"
      - label: "dinos-r-us.svg"
        indent: 2
        fade: true
      - label: "hadrosaur.jpg"
        indent: 2
        fade: true
      - label: "iguanodon.jpg"
        indent: 2
        fade: true
      - label: "stegosaurus.jpg"
        indent: 2
        fade: true
    after: |
      ### HTML setup

      1. Make a new `index.html` file
      2. Add the HTML boilerplate code to `index.html`

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

      **Don’t forget to fill in the `href` with the path to your CSS file!** It should look like this:

      ```html
      <link href="css/main.css" rel="stylesheet">
      ```

      ### Basic styling

      *Inside `main.css`:*

      1. Target the whole page and change the background colour to `#f2f1ed`
      2. Change the text on the whole page to `Georgia` with a backup font of `serif`
      3. Set the `line-height` of the whole page to `1.5`
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
      2. Make the links in the navigation `bold`
      3. Make the size of the links `1.125rem`
      4. Add the navigation & style it to match—[see the tutorial on styling links](/topics/basic-typography/#styling-links)
        — normal colour: `#793284`
        — `:hover` colour: `#b42885`

      *After you’re done the above steps it should look like this in your browser:*

      ![](goal-step-3.jpg)

  - title: "Web fonts"
    before: |
      1. Go to Google Fonts and find the Patua One typeface. [(Follow this step-by-step tutorial if you need help.)](/topics/google-fonts/)
      2. Add it to a collection and use it
      3. Include the new font in your HTML
      4. Change the headings and the navigation to use the new font
      5. Make the caption on the first dinosaur larger than the rest

      *After you’re done the above steps it should look like this in your browser:*

      ![](goal.jpg)

---
