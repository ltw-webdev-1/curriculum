---
layout: slide-deck
title: "HTML introduction"
desc: "A quick introduction to HTML, how it works, what it’s purpose is, and how to write it."

slides:
  - type: super-big-text
    content: |
      **HTML introduction**

  - content: |
      ## The layers of the web

      1. HTML
      2. CSS
      3. Javascript
    notes: |
      Each layer is a completely unique and independent coding language.

      And each layer has a specific purpose.

      *I want you to envision a peanut M&M.*

  - type: image
    image: layer-1.svg
    alt: "HTML: content/peanut"
    notes: |
      ### The HTML

      HTML—the content—is the base level, the peanut.

      By itself it’s tasty and nutritious.
      It doesn’t need anything else.

  - type: image
    image: layer-2.svg
    alt: "CSS: design/chocolate"
    notes: |
      ### The CSS

      CSS—the design—is the next level, the chocolate.

      A chocolate-covered peanut is supremely better than a peanut by itself.
      Does the peanut need the chocolate? No. But it’s so much better with chocolate.

      *HTML does not need CSS, but CSS makes things sweeter.*

  - type: image
    image: layer-3.svg
    alt: "Javascript: interactivity/candy"
    notes: |
      ### The Javascript

      Javascript—the interactivity—the third level, the candy.

      A candy-coated, chocolate-covered peanut is infinitely better than just a chocolate covered peanut.
      Does the chocolate peanut need the candy? No. But it’s totally better with candy.

      *CSS does not need Javascript, HTML does not need Javascript—but Javascript makes the website better.*

  - content: |
      ## Semantics

      *Choose elements for their purpose<br>not what they look like*

      - The `b` tag doesn’t mean “bold”
      - The `ul` doesn’t mean add “bullets”
      - The `h1` doesn’t mean “big text”
    notes: |
      When writing HTML the only thing that matters when writing the code is describing the content. *HTML’s whole purpose is to describe what the content **is** not what the content looks like.*

  - type: image
    image: parts-basic.svg
    alt: "A basic HTML element, specifically and <h1>"

  - type: image
    image: parts-basic-bits.svg
    alt: "The different parts of an HTML element"
    notes: |
      - The “open tag” is the bit of code before the content—it always has a word, the tag name, surrounded by `<` & `>`
      - The “close tag” is the bit of code after the content—it is written as `<`, followed by `/`, followed by the name of the tag, then `>`—nothing else.
      - An “element” is the open tag, plus the content, plus the close tag.

  - type: image
    image: parts-attr.svg
    alt: "An example of an <a> (link) tag"
    notes: |
      Some open tags have more pieces of information in them, called attributes.

      The attributes generally define extra properties that aren’t specifically visible.

      For example, the `<a>` tag must have an attribute named `href` that points to the URL the link will navigate to.

  - type: image
    image: parts-self-closing.svg
    alt: "An example of an <img> tag"
    notes: |
      Some tags don’t have a close tag—only and open tag. These are called self-closing tags.

      A `<img>` tag is an example: it’s only an open tag with a few attributes that define the image to display at that location.

  - type: code
    html: |
      <header>
        <h1>Titanosaur</h1>
        <img src="images/titanosaur.jpg" alt="Titanosaur skeleton">
        <p>The heaviest creatures ever to walk the earth.</p>
        <nav>
          <ul>
            <li><a href="#desc">Description</a></li>
            <li><a href="#paleo">Paleobiology</a></li>
            <li><a href="#tax">Taxonomy</a></li>
          </ul>
        </nav>
      </header>
    notes: |
      This sample of code is a very good example of the code you’d need for the masthead/navigation of a website.

      Notice how there’s no indication of what it looks like, only some content and tags that describe the purpose of the content.

  - content: |
      ## Videos & tutorials

      - [HTML semantics ➔](/topics/html-semantics/)
      - [HTML indentation ➔](/topics/html-indentation/)
      - [HTML semantics cheat sheet ➔](/topics/html-semantics-cheat-sheet/)
      - [HTML semantics checklist ➔](/topics/html-semantics-checklist/)

---
