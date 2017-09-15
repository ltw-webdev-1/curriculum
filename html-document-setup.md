---
layout: lesson
title: "HTML document setup"
desc: "Create a valid HTML document with all the right starter code."

video: "DDMgQc6lX8o"

markbot_submit: true
hide_show_for_marks: true

extra_tutorials:
  - title: "HTML semantics"
    url: html-semantics
  - title: "HTML indentation"
    url: html-indentation
  - title: "HTML semantics cheat sheet"
    url: html-semantics-cheat-sheet
    highlight: true
  - title: "HTML semantics checklist"
    url: html-semantics-checklist
  - title: "HTML introduction slide deck"
    url: /courses/web-dev-1/html-introduction/
  - title: "Validators"
    url: validators

goal:
  before: "We’re going to walk through writing some HTML code and the bits that are necessary for a valid document."
  notes:
    - label: "Type it, type it real good"
      text: "Remember the purpose of this lesson is to type the code out yourself—build up that muscle memory in your fingers!"

fork:
  url: "https://github.com/acgd-webdev-1/html-document-setup"

steps:
  - title: "Set up project"
    before: |
      Before we get started, create some files and get ready.
    folders:
      - label: "html-document-setup"
        type: folder
      - label: "index.html"
        indent: 1
      - label: "images"
        type: folder
        indent: 1
        notes: "This folder already exists, it was cloned from GitHub"
      - label: "logo.svg"
        indent: 2
    after: |
      1. Drag the `html-document-setup` folder you cloned to your code editor (likely Atom).
      2. Using your code editor, create a new file, then immediate save it as exactly `index.html` into the `html-document-setup` folder.
    notes:
      - label: "Naming conventions"
        text: "Don’t forget to follow the [naming conventions](/topics/naming-paths-cheat-sheet/#naming-conventions)."

  - title: "Write the HTML"
    before: |
      In order for our HTML file to be read properly by all web browsers we need a bunch of specific elements in our code.

      Here’s the HTML we need to make a basic HTML file.
    code_lang: "html"
    code_file: "index.html"
    code: |
      <!DOCTYPE html>
      <html lang="en-ca">
      <head>
        <meta charset="utf-8">
        <title>HTML template</title>
        <meta name="viewport" content="width=device-width,initial-scale=1">
      </head>
      <body>

        <!-- All the HTML content goes in here -->

        <header>
          <h1>HTML template</h1>
        </header>

        <main>
          <p>Lorem ipsum dolor sit amet.</p>
          <img src="images/logo.svg" alt="">
          <a href="https://www.wikipedia.org">Wikipedia</a>
        </main>

      </body>
      </html>
    lines:
      - num: "1"
        text: "The `DOCTYPE` tells browsers we’re writing valid HTML. Without it browsers will render our sites like 1999."
      - num: "2"
        text: |
          Everything in the file is wrapped in an `<html>` element.
          This is where we specify the content language using the `lang=""` attribute.
      - num: "3"
        text: "The `<head>` is where we store extra metadata about our HTML file; stuff that isn’t rendered in the browser’s viewport."
      - num: "4"
        text: "By writing `utf-8` on this line we’re allowing any language to be written in our file. Allows accented characters, non-English characters, Klingon, etc."
      - num: "5"
        text: "The `<title>` is *the* most important element—it’s what’s shown in search results and in the browser tab."
      - num: "6"
        text: "The `viewport` tag tells mobile browsers how to render our website—we’ll discuss this more later."
      - num: "8"
        text: "Everything goes in the `<body>` tag. **This isn’t the body of the content it’s the body of the HTML file.**"
      - num: "10"
        text: "We can write notes to ourselves, called comments; they won’t be shown on the screen."
      - num: "13"
        text: "The `<h1>` tag *is the most important* piece of content on the page—every single HTML file needs one."
      - num: "16-20"
        text: "We can write as much HTML in here as we want. The indentation is there to help us understand our code, but the browser doesn’t really care."
    notes:
      - label: "Type it, type it real good"
        text: "Remember the purpose of this lesson is to type the code out yourself—build up that muscle memory in your fingers!"
    after: |
      **The code above is intentionally not copy-and-paste-able. You need to write the code by hand to learn it properly. So every single lesson will have the ability to copy-and-paste its code snippets disabled.**

  - title: "Test it in the browser"
    before: |
      Double click the `index.html` file Finder *or* right-click in your code editor and press “Open in browser”.

      You should see something that looks like this:

      ![](goal.jpg)
    notes:
      - label: "HTML snippets"
        text: |
          In the future you can create the HTML boilerplate stuff with a few snippets: `html5` and `viewport`

          Type the snippet keyword then press `Tab`

  - title: "Validate the HTML"
    before: |
      We can use an online tool, called a validator, to check our HTML for bugs like unclosed tags, missing, code, etc.

      **If your code isn’t doing what you expect it to do—validate it!**

      ![](html.jpg)

      2. Select all your HTML code with `⌘A`
      2. Copy the code with `⌘C`
      1. Go to the [W3C HTML validator](https://validator.w3.org/).
      3. Paste the code into the “Validate by Direct Input” text box with `⌘V`
      4. Press “Check”.
      5. See your errors, correct them, and validate again.

      *You want to get the green bar—green is good.*

      ![](html-valid.jpg)

---
