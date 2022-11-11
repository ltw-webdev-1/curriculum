---
layout: lesson
title: "Flexing your muscles"
desc: "Follow this lesson to learn some flexbox techniques to apply to different layouts."

hide_show_for_marks: true
markbot_submit: true

extra_tutorials:
  - title: "Flexbox"
    url: flexbox
  - title: "Flexbox cheat sheet"
    url: flexbox-cheat-sheet

markbot_notes: |
  We don’t have an `<h1>` in this code because this is the footer on a larger website so the `<h1>` would probably be somewhere else on the page.

goal:
  before: "We’re going to walk through writing some HTML and CSS, then use some flexbox, to create a common footer pattern."
  image: goal.png
  notes:
    - label: "Type it, type it real good"
      text: "Remember the purpose of this lesson is to type the code out yourself—build up that muscle memory in your fingers!"

fork:
  url: "https://github.com/ltw-webdev-1/flexing-your-muscles"

steps:
  - title: "Set up the project"
    before: |
      After cloning the repo to your computer we need to create the default files.
    folders:
      - label: "flexing-your-muscles"
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
      - label: "facebook.svg"
        indent: 2
        fade: true
      - label: "instagram.svg"
        indent: 2
        fade: true
      - label: "youtube.svg"
        indent: 2
        fade: true

    after: |
      1. Make a new `index.html` file in your `flexing-your-muscles` folder.
      2. Make a folder named `css` in your `flexing-your-muscles` folder.
      3. Make a new `main.css` in your `css` folder.
    notes:
      - label: "Naming conventions"
        text: "Don’t forget to follow the [naming conventions](/topics/naming-paths-cheat-sheet/#naming-conventions)."

  - title: "Add HTML boilerplate"
    before: "*Use the `html5`, `viewport` and `css` snippets.*"
    code_lang: "html"
    code_file: "index.html"
    code: |
      <!DOCTYPE html>
      <html lang="en-ca">
      <head>
        <meta charset="utf-8">
        <title>Flexing your muscles</title>
        <meta name="viewport" content="width=device-width,initial-scale=1">
        <link href="css/main.css" rel="stylesheet">
      </head>
      <body>

      </body>
      </html>
    lines:
      - num: 7
        text: "Don’t forget to attach the CSS file."
    notes:
      - label: "HTML snippets"
        text: "Create the boilerplate with `html5`, `viewport` & `css`"

  - title: "Add CSS boilerplate"
    before: |
      *Use the `borderbox` snippet.* Then add a few more of the default CSS lines we’ll need.
    code_lang: "css"
    code_file: "css/main.css"
    code: |
      html {
        box-sizing: border-box;
        font-family: sans-serif;
        line-height: 1.5;
      }

      *, *::before, *::after {
        box-sizing: inherit;
      }

      body {
        margin: 0;
      }

      img {
        display: block;
        width: 100%;
      }
    lines:
      - num: 3
        text: |
          Don’t forget to add a `font-family` to the top, in the `html` element.
      - num: 4
        text: |
          For now, we’re going to add a `line-height` of `1.5` to all our websites—at least until we start doing responsive websites with media queries.
    notes:
      - label: "CSS snippets"
        text: "Create the boilerplate with `borderbox`"
    after: "The `border-box` system changes the browsers layout math to include the `padding` in the `width`—the default is more difficult to manage when making flexible, responsive websites."

  - title: "Start with some HTML"
    before: |
      Let’s write all the necessary HTML the website footer and then we’ll move on to doing the flexbox CSS to make it look how we want.

      *Yeah, it’s quite a lot, but I’m confident you can manage writing all that at once so we can concentrate on the CSS.*
    code_lang: html
    code_file: "index.html"
    code: |
      ⋮
      <body>

        <footer class="footer">

          <nav class="links">
            <h2>Products</h2>
            <ul>
              <li><a href="#">Vegan Protein Bars</a></li>
              <li><a href="#">Vegan Protein Blends</a></li>
              <li><a href="#">Vitamins &amp; supplements</a></li>
              <li><a href="#">Herbs &amp; remedies</a></li>
            </ul>
          </nav>

          <nav class="links">
            <h2>Company</h2>
            <ul>
              <li><a href="#">About</a></li>
              <li><a href="#">Franchises</a></li>
              <li><a href="#">Locations</a></li>
              <li><a href="#">Contact</a></li>
            </ul>
          </nav>

          <ul class="social">
            <li><a href="#"><img src="images/instagram.svg" alt="Instagram"></a></li>
            <li><a href="#"><img src="images/facebook.svg" alt="Facebook"></a></li>
            <li><a href="#"><img src="images/youtube.svg" alt="YouTube"></a></li>
          </ul>

          <small class="copyright">© Protein Power House</small>

        </footer>

      </body>
      ⋮
    lines:
      - num: "2,36"
        fade: true
      - num: 4
        text: |
          This whole pattern we’re making today is a footer for a website, so let’s wrap it in the footer tag.
      - num: 11
        text: |
          See the `&amp;` code? That’s called an HTML entity. There are certain characters we cannot write in HTML because they are part of the language itself. The `&amp;` entity will output an `&`—we can’t write `&` directly in our code because it’s part of the HTML language.

          The other two characters we need to escape are:

          - `<` — `&lt;`
          - `>` — `&gt;`
      - num: "6, 16"
        text: |
          We have two chunks of navigation in the footer, each pointing to resources on the website—like a mini sitemap.
      - num: "26-30"
        text: |
          Let’s add some social media links to the footer too. The images you need are already in the `images/` folder.

          We’ll wrap each image in an `<a>` tag so they are clickable.

          **It’s extremely critical we add well thought-out `alt` attributes to the `<img>` tags** for accessibility, and in the event the images don’t download.
      - num: 32
        text: |
          The last hunk of HTML is a `<small>` tag that contains our copyright notice.
    after: |
      Refresh in your browser and you should see this:

      ![](html-only.png)

      *The image above is cropped because it’s really tall because of those huge social media icons.*

  - title: "Basic CSS layout"
    before: |
      Let’s add some CSS to the footer to add some colours and the basic layout. Also I think it’s a good time to get those huge social icons under control.
    code_file: "css/main.css"
    code_lang: css
    code: |
      ⋮
      img {
        display: block;
        width: 100%;
      }

      .footer {
        display: flex;
        justify-content: space-between;
        padding: 1em 0;

        background-color: #8bc9d9;
        border-top: 3px solid #005e76;

        color: #005e76;
      }

      .social > li {
        width: 3em;
      }
    lines:
      - num: "2-5"
        fade: true
      - num: 7
        text: |
          We added a class for the `<footer>` tag in the HTML because it’s possible we could use more than one footer in our code, so this is more forward thinking and safe.
      - num: "8-9"
        text: |
          Turn the footer into a flex container, meaning all it’s direct children will be flex items—and by default they’ll fit on the same line.

          We’ll also go ahead and add `justify-content` to spread them out and fill all the available space on the line.
      - num: "18-20"
        text: |
          Let’s get the size of those icons under control by setting a width of the `<li>` tags.

          By default we always want our images to scale, so we set a `width: 100%` on the `<img>` tags further up in the CSS. But we can overwrite & control the width of the images by setting a `width` on the **parent element**.
    after: |
      Refresh in your browser to see the basic footer—but it still needs some work.

      ![](basic-css-layout.png)

  - title: "Fix the copyright notice"
    before: |
      The copyright notice is currently jammed up beside the social media icons, but we really want it below, on its own line. So let’s add `flex-wrap` to our CSS.
    code_lang: css
    code_file: "css/main.css"
    code: |
      ⋮
      .footer {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        padding: 1em 0;

        background-color: #8bc9d9;
        border-top: 3px solid #005e76;

        color: #005e76;
      }

      .social > li {
        width: 3em;
      }

      .copyright {
        width: 100%;
      }
    lines:
      - num: "2-4,6-16"
        fade: true
      - num: 5
        text: |
          Add the `flex-wrap` property so that the flex items can move to the next line if they run out of space.
      - num: "18-20"
        text: |
          Target the copyright notice and force it onto its own line by giving it a width of `100%`
    after: |
      Refresh!

      ![](copyright.png)

  - title: "Fix up some typography"
    before: |
      Now we’ll make some adjustments to the typography: get rid of the bullets and their default space & add some colours to the links.

      We’re even going to get the social media icons onto the same line with the addition of another flex container.
    code_lang: css
    code_file: "css/main.css"
    code: |
      ⋮
        background-color: #8bc9d9;
        border-top: 3px solid #005e76;

        color: #005e76;
      }

      .footer ul {
        padding-left: 0;
        list-style-type: none;
      }

      .footer a {
        color: #003442;
      }

      .social {
        display: flex;
      }

      .social > li {
        width: 3em;
      }
      ⋮
    lines:
      - num: "2-6,21-23"
        fade: true
      - num: "8-11"
        text: |
          Target every single unordered list inside the footer and remove their bullets by setting `list-style-type` to none.

          We’ll also get rid of the default `padding` on the left that browsers set to have space for where the bullets sit.
    after: |
      **`⌘ Tab`, `⌘R`**

      ![](type.png)

      *Notice how the social media icons are now on their own line too, instead of being stacked.*
  - title: "Paddings & margins"
    before: |
      It’s time to tackle `padding` and `margin`—our goal being to create a cohesive space around and between all the different elements so they look balanced.
    code_lang: css
    code_file: "css/main.css"
    code: |
      ⋮
      .footer {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        padding: 1.5rem 0;

        background-color: #8bc9d9;
        border-top: 3px solid #005e76;

        color: #005e76;
      }

      .footer h2 {
        margin-top: 0;
        margin-bottom: 1.5rem;
      }

      .footer ul {
        margin-top: 0;
        margin-bottom: 1.5rem;
        padding-left: 0;
        list-style-type: none;
      }

      .footer a {
        color: #003442;
      }

      .links {
        padding: 0 1rem;
      }

      .social {
        padding: 0 1rem;
        display: flex;
      }

      .social > li {
        margin: 0 .5em;
        width: 3em;
      }

      .copyright {
        padding: 0 1rem;
        width: 100%;
      }
    lines:
      - num: "2-5,7-12"
        fade: true
      - num: 6
        text: |
          For the most consistent typography it’s a good idea to try to base vertical paddings and margins on the line-height—it’s called making a baseline rhythm.

          For the `<footer>` itself, we’re going to have `padding` on the top and bottom equal to the page’s `line-height`. Since the `line-height` is `1.5` a padding of `1.5rem` will be equal in size.
      - num: "14-17, 20-21"
        text: |
          It’s also super helpful to remove the top margins from elements and use only bottom margins—we can avoid the annoying margin collapse system by choosing a single margin direction.

          For the `<h2>` and for all the `<ul>` tags we’re going to remove their top margin & set the bottom margin equal to the line-height.
      - num: "22-23,26-29"
        fade: true
      - num: "30-32, 35, 45"
        text: |
          Finally we’ll add some nicer horizontal spacing to elements. Here we’ll target the two `.link` `<nav>` tags and add equal padding to their left & right. We’ll do the same thing to the `.social` icons and the `.copyright` notice. Now everything should align nicely.
      - num: 36
        fade: true
      - num: 40
        text: |
          I don’t like how the social media icons are touching each other; if we add a `margin` to their left & right sides we can space them out a little bit.
      - num: 41
        fade: true
      - num: 46
        fade: true
    after: |
      Another quick look in the browser before we move to the final step.

      ![](padding-margin.png)

  - title: "Adjust column alignment"
    before: |
      There are two final things I want to adjust:

      1. I want the social media icons to be centrally aligned,
      2. And I want to make the two navigation columns closer together.
    code_lang: css
    code_file: "css/main.css"
    code: |
      ⋮
      .footer {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        align-items: center;
        padding: 1.5rem 0;

        background-color: #8bc9d9;
        border-top: 3px solid #005e76;

        color: #005e76;
      }

      ⋮

      .social {
        margin-left: auto;
        padding: 0 1rem;
        display: flex;
      }
      ⋮
    lines:
      - num: "3-5,7-12"
        fade: true
      - num: 6
        text: |
          First we’re going to tackle the alignment of the social media icons. Because our `flex-direction` is set to `row` (default) we can use the `align-items` property to control the vertical alignment of the flex items.

          If we set `align-items` to `center` the social media icons will move down to be centrally aligned with the navigation.
      - num: 18
        text: |
          To push the social icons to the far right—and force the two navigations to squish against the left side—we can set the `margin-left` of the `.social` icons to `auto`. An automatic margin inside flexbox can force space to be used up by emptiness, pushing the elements endlessly farther apart.
      - num: "19-20"
        fade: true
    after: |
      **One final refresh to see the final result of all our code!**

---
