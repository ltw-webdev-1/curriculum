---
layout: slide-deck
title: "Link patterns"
desc: "A quick look at different link design patterns on the Open Web and how to code them."

group_work: true

slides:
  - type: super-big-text
    content: |
      **Link patterns**

  - content: |
      ## Highlighting current page

      Users should always be shown the currently highlighted page

      ![](current-page.svg)
    notes: |
      Highlighting the current navigation on a page helps users remember where they are; if they’re distracted or have trouble remembering things this is a clear indicator of their location on the website.

  - type: interactive
    html_lines:
      - num: 5
        text: |
          There’s no special way to highlight the current navigation. We solve the problem by putting a class onto the `<a>` tag in the navigation that represents the current page.

          Since there’s now a class on that `<a>` tag we can style it a little differently from the other links.

          To make other pages appear highlighted, in the code for that page, we move the `.current` class to the appropriate link.

          *There will never be more than one `<a>` tag highlighted with the `.current` class in one HTML file.*
    html: |
      <nav>
        <ul>
          <li><a href="#">Dinosaurs</a></li>
          <li><a href="#">Plesiosaurs</a></li>
          <li><a class="current" href="#">Pterosaurs</a></li>
          <li><a href="#">Insects</a></li>
        </ul>
      </nav>
    css: |
      .current {
        background-color: #3c3670;
        border-color: #3c3670;
        color: #fff;
      }
    css_hidden: |
      html {
        font-size: 1.125rem;
      }
      nav {
        padding: 1rem 0;
        background-color: #bbb6e3;
        text-align: center;
      }
      ul {
        margin: 0;
        padding: 0;
        list-style-type: none;
      }
      ul > li {
        display: inline-block;
      }
      nav a {
        display: inline-block;
        padding: 0.4em 0.75em 0.3em;
        background-color: transparent;
        border: 4px solid #5e54af;
        border-radius: 8px;
        color: #3c3670;
        text-decoration: none;
      }
      nav a:hover {
        background-color: #5e54af;
        border-color: #5e54af;
        color: #fff;
      }

  - content: |
      ## Button styles

      Websites have many button patterns—but in every design they should look consistent

      **Share styles by using multiple CSS classes on a single element**

  - type: interactive
    html_lines:
      - num: 2
        text: |
          Did you realize that HTML elements can have more than 1 class? It’s crazy.

          When there are multiple classes on the same HTML element it will get all the CSS from **both** classes applied to it.

          The order of the classes in the HTML doesn’t matter, only the order of the CSS code. That means that the CSS class code that’s further down the CSS file is the one that overwrites.
    html: |
      <a class="btn" href="#">Main button</a>
      <a class="btn btn-alt" href="#">Alternative style</a>
    css_lines:
      - num: "10-12"
        text: |
          In the case of this CSS, if an element has both `.btn` & `.btn-alt` it will get all the CSS from the basic `.btn` class but the `background-color` will be overwritten by `.btn-alt` to be slightly different.

          We can save so much code be using multiple classes for slight variations of a pattern.
    css: |
      .btn {
        display: inline-block;
        padding: 0.4em 0.75em 0.3em;
        background-color: #333;
        border-radius: 8px;
        border: 0;
        color: #fff;
        text-decoration: none;
      }
      .btn-alt {
        background-color: #00675a;
      }
    css_hidden: |
      .btn {
        margin-bottom: 0.75rem;
      }

  - content: |
      ## Link cards

      - Cards are boxes on screen with bits of information, images, links etc.
      - They usually sit in columns amongst other cards.

      *A link card is just a card that can be clicked anywhere.*

  - type: image
    image: cards.jpg
    alt: "Some different card examples from Facebook, Pinterest and Instagram"

  - type: interactive
    html: |
      <a class="link-card" href="">
        <h2>Dinosaurs</h2>
        <p>Large and small prehistoric reptilian animals that dominated Earth.</p>
        <div class="btn-wrap">
          <span class="btn">Learn More!</span>
        </div>
      </a>
    css_lines:
      - num: 6
        text: |
          When doing link cards we need to think about what thing we’re hovering on—in this case it’s `.link-card` itself.

          Because `.link-card` has elements inside, that means we can target those elements when `.link-card` is hovered. By using CSS like this we can hover anywhere on a larger box and make elements inside that box change style.
    css: |
      .link-card:hover {
        background-color: #5e54af;
        border-color: #5e54af;
        color: #fff;
      }
      .link-card:hover .btn {
        background-color: #bbb6e3;
      }
    css_hidden: |
      html {
        font-size: 1.125rem;
        line-height: 1.5;
      }
      .link-card {
        padding: 1rem;
        max-width: 15em;
        display: inline-block;
        border: 4px solid #5e54af;
        border-radius: 8px;
        color: #3c3670;
        text-decoration: none;
      }
      .link-card h2 {
        margin: 0;
      }
      .link-card p {
        margin: 0;
      }
      .link-card .btn-wrap {
        padding-top: 1.5rem;
        text-align: center;
      }
      .link-card .btn {
        display: inline-block;
        padding: 0.4em 0.75em 0.3em;
        background-color: #333;
        border-radius: 8px;
        border: 0;
        color: #fff;
        text-decoration: none;
      }

  - content: |
      ## Videos & tutorials

      - [Navigation ➔](/topics/navigation/)

---
