---
layout: lesson
title: "Dinosaur designs"
desc: "Work to build this website and style its typography using your new CSS skills."

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
      After cloning the repository to your computer you should have some starter images. And a file named `content.txt` that contains all the text content so you can copy and paste.

      **Drag the `dinosaur-designs` folder to Atom and make an HTML file & a CSS file.**
    folders:
      - label: "dinosaur-designs"
        type: folder
      - label: "content.txt"
        indent: 1
        fade: true
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

  - title: "Basic styling"
    before: |
      Open up your `main.css` file in a tab in Atom and we’re going to write some code.
    code_file: 'main.css'
    code_lang: 'css'
    code: |
      html {
        background-color: #f2f1ed;
        font-family: Georgia, serif;
        line-height: 1.5;
      }
    lines:
      - num: 1
        text: |
          Target the whole page—since the `html` element surrounds everything we can use it to style the whole visible space
      - num: 2
        text: |
          Change the background colour  of the whole page to `#f2f1ed`
      - num: 3
        text: |
          Change the text on the whole page to `Georgia` with a backup font of `serif`
      - num: 4
        text: |
          Set the `line-height` of the whole page to `1.5`—this is a nice line-height for the web, a little loose but makes the text very readable.

          We should do this every time we start a new website.
      - num: 5
        text: |
          Don’t forget to close this chunk of CSS with a closing curly brace.
    after: |
      Now open the `index.html` in your browser and make the window narrower than normal.

      It should look like this in your browser:

      ![](bg.jpg)

  - title: "Add some content"
    before: |
      Switch to your `index.html` file inside Atom—open it in a new tab.

      *You can copy and paste the text content from `content.txt` to make sure there are no typos.*
    code_lang: 'html'
    code_file: 'index.html'
    code: |
      ⋮
      </head>
      <body>

        <header>
          <h1><img src="images/dinos-r-us.svg" alt="Dinos ’R’ Us"></h1>
        </header>

        <main>

          <h2>Hadrosaur</h2>
          <figure>
            <img src="images/hadrosaur.jpg" alt="">
            <figcaption>Hadrosaurids are descendants of the Upper Jurassic/Lower Cretaceous iguanodontian dinosaurs and had a similar body layout.</figcaption>
          </figure>

        </main>

      </body>
      </html>
    lines:
      - num: '2,3,19,20'
        fade: true
      - num: 5
        text: |
          We’ll start with a `<header>` to surround the title and masthead area of the page.
      - num: 6
        text: |
          We can surround `<img>` tags in headings, like `<h1>` in the case of logos, if we add the very important `alt` attribute.

          In this case the `alt` attribute should say exactly the text inside the image, essentially what you’d write in the `<h1>` if there wasn’t an image.
      - num: 9
        text: |
          Open up a `<main>` tag to surround the page’s main content.
      - num: 11
        text: |
          Since we’re starting a new information section we should begin with a heading, an `<h2>` because the previous heading was an `<h1>`
      - num: '12-15'
        text: |
          We’ll use a `<figure>` element in this situation because the text appears to be a caption for the image itself.

          When using the `<figure>` tag the `alt` attribute on the image can be blank if the `<figcaption>` itself provides enough information to describe the image.
    after: |
      Jump back over to your browser tab a refresh the HTML—you should see this:

      ![](starter-content.jpg)

  - title: "Style the header & first image"
    before: |
      Now we’re ready to write a little more CSS to style the new content we added.
    code_file: 'main.css'
    code_lang: 'css'
    code: |
      ⋮
        line-height: 1.5;
      }

      img {
        width: 100%;
      }

      h1, h2 {
        color: #5d8432;
        text-transform: uppercase;
      }

      figcaption {
        font-size: .8rem;
        font-style: italic;
        text-align: center;
      }
    lines:
      - num: '2,3'
        fade: true
      - num: '5-7'
        text: |
          Here we’re targeting every single image on the website and we’re giving them a width of 100%. This will allow the images to scale to fit their parent element.
      - num: 9
        text: |
          We’re going to target all the `<h1>` and `<h2>` tags on the page to add some styles to them.
      - num: 10
        text: |
          Change the colour of their text to a greenish hue.
      - num: 11
        text: |
          Change the letters to uppercase. We never want to write actual uppercase letters in HTML (except for acronyms, etc.) because, digitally, uppercase means yelling. So if we visually want uppercase we can use CSS to do it.
      - num: '14-18'
        text: |
          Target the `<figcaption>` tag to adjust the text underneath the image. Change the font size, style and align the text to the centre.

    after: |
      After you’ve written the above code it should look like this in your browser:

      ![](styled-masthead.jpg)

  - title: "Add the navigation & remaining images"
    before: |
      Pop back over to your HTML file and add the navigation. We’re going to insert it into the `<header>` tag right below the `<h1>`.
    code_lang: 'html'
    code_file: 'index.html'
    code: |
      ⋮
      </head>
      <body>

        <header>
          <h1><img src="images/dinos-r-us.svg" alt="Dinos ’R’ Us"></h1>
          <nav>
            <ol>
              <li><a href="#hadrosaur">Hadrosaur</a></li>
              <li><a href="#iguanodon">Iguanodon</a></li>
              <li><a href="#stegosaurus">Stegosaurus</a></li>
            </ol>
          </nav>
        </header>

        <main>

          <h2 id="#hadrosaur">Hadrosaur</h2>
          <figure>
            <img src="images/hadrosaur.jpg" alt="">
      ⋮
    lines:
      - num: '2,3,5,6,14,16,19,20'
        fade: true
      - num: 7
        text: |
          We must always wrap navigation on our website in the `<nav>` tag.
      - num: 8
        text: |
          It’s best practice to surround the navigation links in a list. In this situation we’re using an `<ol>` because the order of the links matches the order of the content.
      - num: '9-11'
        text: |
          These links are going to jump down to each of the dinosaurs on the page that’s why we’re using internal `#` links.
      - num: 18
        text: |
          We are adding a matching `id` attribute to the `<h2>` tag that will show the matching navigation item where to jump down to in the content.
    after: |
      **The next part is completely up to you: copy and paste the `<h2>` & `<figure>` tags to add the remaining two dinosaurs onto the page.**

      After you’ve added the final two dinosaurs you should see this:

      ![](content-nav.jpg)

  - title: "Style the navigation"
    before: |
      We’re going to style the navigation so it doesn’t use the browser’s default CSS. Open up your CSS file and add this code:
    code_lang: 'css'
    code_file: 'main.css'
    code: |
      ⋮
      figcaption {
        font-size: .8rem;
        font-style: italic;
        text-align: center;
      }

      nav {
        font-size: 1.125rem;
        font-weight: bold;
      }

      nav ol {
        list-style-type: none;
      }

      nav a {
        color: #793284;
        text-decoration: none;
      }

      nav a:hover {
        color: #b42885;
        text-decoration: underline;
      }
    lines:
      - num: '2,3,4,5,6'
        fade: true
      - num: '8-11'
        text: |
          Target the whole navigation element to adjust the text: making it bold and slightly larger.
      - num: '13-15'
        text: |
          Target the list inside the navigation to remove the bullets.
      - num: '17-20'
        text: |
          Target the links inside the navigation to change their colour and remove the underline. It’s usually bad practice to remove underlines from links, but in the case of primary navigation it’s usually okay.
      - num: '22-25'
        text: |
          We’re going to style the hover state of the nav links to change their colour and reinstate the underline.
    after: |
      Look like this in your browser, you should see this:

      ![](styled-nav.jpg)

  - title: "Style the first caption differently"
    before: |
      Just for fun, I want to make the caption of the first dinosaur have larger text than the rest.

      To do that, we need to target that caption separately from the other captions. The best way to accomplish that is to use a `class`. A class is like a name that we can assign to any HTML element, then use that name in the CSS for styling.
    multi_code:
      - code_file: 'index.html'
        code_lang: 'html'
        code: |
          ⋮
          <h2 id="#hadrosaur">Hadrosaur</h2>
          <figure>
            <img src="images/hadrosaur.jpg" alt="">
            <figcaption class="intro">Hadrosaurids are descendants of the Upper Jurassic/Lower Cretaceous iguanodontian dinosaurs and had a similar body layout.</figcaption>
          </figure>
          ⋮
        lines:
          - num: '2,3,4,6'
            fade: true
          - num: 5
            text: |
              Notice the new attribute on the `<figcaption>`. We add the `class` attribute and make up whatever we want inside the quotes—but make sure the [class name follows our naming conventions](/topics/naming-paths-cheat-sheet/).
      - code_before: |
          Now we pop over to our CSS file and target that class to make some style changes.
        code_file: 'main.css'
        code_lang: 'css'
        code: |
          ⋮
          nav a:hover {
            color: #b42885;
            text-decoration: underline;
          }

          .intro {
            font-size: 1rem;
          }
        lines:
          - num: '2,3,4,5'
            fade: true
          - num: '7-9'
            text: |
              Target the class directly—make sure to put a period in front (`.`). The period in CSS means: “this is a class”.

              Then style the font size so it’s a little larger than the rest of the captions.
    after: |
      Refresh in the browser to see the caption is a little larger.

      ![](first-caption.jpg)

  - title: "Web fonts"
    before: |
      **Here’s something for you to complete on your own…**

      1. Go to Google Fonts and find the Patua One typeface. [(Follow this step-by-step tutorial if you need help.)](/topics/google-fonts/)
      2. Add it to a collection and copy the `<link>` tag Google
      3. Put the new font in your HTML
      4. Change the headings and the navigation to use the new font

      *After you’re done the above steps it should look like this in your browser:*

      ![](goal.jpg)

---
