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

  - type: interactive
    html_lines: "5"
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
    html_lines: "2"
    html: |
      <a class="btn" href="#">Main button</a>
      <a class="btn btn-alt" href="#">Alternative style</a>
    css_lines: "10-12"
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

  - type: interactive
    html: |
      <a class="link-card" href="">
        <h2>Dinosaurs</h2>
        <p>Large and small prehistoric reptilian animals that dominated Earth.</p>
        <div class="btn-wrap">
          <span class="btn">Learn More!</span>
        </div>
      </a>
    css_lines: "6"
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
