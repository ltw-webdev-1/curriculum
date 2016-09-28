---
layout: lesson
title: "Developer tools"
desc: "Learn about the developer tools in browsers and use them to modify an existing website."

hide_markbot: true

extra_tutorials:
  - title: "Browser developer tools"
    url: browser-developer-tools

video: "09XV2psDAZ4"

goal:
  before: |
    Learn about using the browser developer tools to modify and inspect websites.

    *The developer tools are really helpful when making websites because we can see what code is being applied and test solutions live in the browser.*

    **The developer tools should almost always be open when working on websites.**
  no_image: true

steps:
  - title: "Watch the video"
    before: |
      Watch the video linked above to learn how to use the developer tools built into browsers.

  - title: "Modify a website"
    before: |
      [**Go to this website**](https://acgd-webdev-1.github.io/dev-tools-modifier/) and, using the developer tools, modify it to look like the screenshots below.

      ![](goal.jpg)

      ### List of changes

      1. Background colour is different—`#f2f1ed`
      1. Heading font-size is larger—`3rem`
      1. Navigation items are rearranged
      1. The first navigation item is bold
      1. The broken image is displaying
      1. Second paragraph is gone
      1. The first paragraph is center aligned
      1. The first paragraph has the class of `intro`
      1. The `<h2>` tags all have the same font-size
      1. All the figcaptions have smaller font-sizes—`.875rem`
        *(See if you can do this with only one modification)*
    notes:
      - label: "Reminder"
        text: |
          The stuff you do in the developer tools isn’t permanent.
          **If you refresh this exercise you’ll have to start over.**
      - label: "Shortcut"
        text: "`⌘⌥I` opens the developer tools."
      - label: "Hint"
        text: "When working with multiple screens I often put the developer tools on my laptop screen and have my code on the big monitor."
---
