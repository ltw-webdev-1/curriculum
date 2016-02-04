---
layout: slide-deck

title: "HTML introduction"

slides:
  - type: super-big-text
    content: |
      **HTML introduction**

  - content: |
      ## The layers of the web

      1. HTML
      2. CSS
      3. Javascript

  - type: image
    image: layer-1.svg

  - type: image
    image: layer-2.svg

  - type: image
    image: layer-3.svg

  - content: |
      ## Semantics

      *Choose elements for their purpose<br>not what they look like*

      - The `b` tag doesn’t mean “bold”
      - The `ul` doesn’t mean add “bullets”
      - The `h1` doesn’t mean “big text”

  - type: image
    image: parts-basic.svg

  - type: image
    image: parts-basic-bits.svg

  - type: image
    image: parts-attr.svg

  - type: image
    image: parts-self-closing.svg

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

  - content: |
      ## Videos & tutorials

      - [HTML semantics ➔](http://learn-the-web.algonquindesign.ca/topics/html-semantics/)
      - [HTML indentation ➔](http://learn-the-web.algonquindesign.ca/topics/html-indentation/)
      - [HTML semantics cheat sheet ➔](http://learn-the-web.algonquindesign.ca/topics/html-semantics-cheat-sheet/)
      - [HTML semantics checklist ➔](http://learn-the-web.algonquindesign.ca/topics/html-semantics-checklist/)

---
