---
layout: lesson
title: "Set up your code editor"
desc: "Set up Atom, GitHub’s code editor, to fill out it’s features and simplify repetitive tasks."

hide_markbot: true

extra_tutorials:
  - title: "Code editors"
    url: code-editors
  - title: "Snippets cheat sheet"
    url: snippets-cheat-sheet
    highlight: true
  - title: "Keyboard shortcut cheat sheet"
    url: keyboard-shortcut-cheat-sheet
    highlight: true
  - title: "Code character cheat sheet"
    url: code-character-cheat-sheet

steps:
  - title: "Download & install Atom"
    before: |
      Atom is a code editor created by GitHub—it’s got lots of great features, the community is really big—and the setup is quick for beginners.

      ### [Download Atom.](https://atom.io/)

      1. Download Atom
      2. Unzip the download
      3. Drag the app to your `Applications` folder

      **Run Atom!**

      *You’ll probably also want to keep Atom it your dock—since you’ll be using it every day.*
    notes:
      - label: "Not the only option"
        text: |
          Atom isn’t the only code editor out there—there are lots!

          Another really popular option is [Sublime Text](/topics/sublime-text/).

  - title: "Important settings"
    before: |
      Atom will work immediately after downloading it—but if you want to get the most out of it, some customization will be needed.

      First let’s double-check some important settings—in the menu go to:

      ```
      Atom > Preferences…
      ```

      ![](preferences.jpg)

      ![](settings.jpg)

      ### Important settings to change

      - Turn on “Scroll Past End”
      - Turn on “Show Indent Guide”
      - Turn on “Show Invisibles”
      - Turn on “Show Line Numbers”
      - Turn on “Soft Tabs”
      - Turn off “Soft Wrap”
      - Tab length: “2”

      *These settings will be important when we start using Markbot later—it will check your code for some of these things.*

  - title: "Install packages"
    before: |
      Adding a few packages (aka plugins) to Atom will give you a bunch more convenient features.

      Inside preferences to to the “Packages” tab to see all the ones already installed.

      Go to the “Install” tab if you want to add new packages to your editor.

      On the install screen you can search for packages and install them into Atom.

      ![](install.jpg)

      ### Packages to install

      **The names must match exactly!**

      - `autoprefixer` — when run, adds the appropriate vendor prefixes to all CSS
      - `browser-refresh` — pressing Fn+F5 will refresh the current HTML file in the browser
      - `color-picker` — a pop-up color picker
      - `pigments` — displays the colours in the code behind the number
      - `editorconfig` — for matching other designers’ coding standards
      - `emmet` — quick way to write HTML, using CSS selectors
      - `advanced-open-file` — opens up a quick new file input at the bottom of the screen, ⌘⌥O
      - `file-icons` — shows icons for each file type in the sidebar
      - `linter` — finds and points out bugs<br>*try searching “linter base package” if it doesn’t show up*
      - `minimap` — adds an overview column of your code like Sublime Text
      - `open-in-browser` — pressing ⌘⌥M will pop open the HTML file in the browser
      - `auto-update-packages` — to help keep your copy of Atom up-to-date

  - title: "Install snippets"
    before: |
      Snippets are little samples of code you can get Atom to automatically insert into your document.

      You type a keyword then hit `Tab` and it will insert a bunch of code automatically.

      #### [Copy my starter snippets.](https://raw.githubusercontent.com/ltw-learn-the-web/atom-code/master/snippets.cson)

      From Atom, go in the menu to:

      ```
      Atom > Snippets…
      ```

      ![](snippets-menu.jpg)

      This will open up a new code file. Paste everything you’ve copied from the GitHub into the bottom of this file. And save.

      ![](snippets.jpg)
    notes:
      - label: "Cheatsheet"
        text: "Check out the [Snippets cheat sheet](/topics/snippets-cheat-sheet/)."

  - title: "Fix shortcut key collisions"
    before: |
      We need to make sure some of the packages don’t take over the `tab` key, so we need to fix our keymap.

      Go to your keymap file:

      ```
      Atom > Keymap…
      ```

      ![](keymap-menu.jpg)

    code_file: "keymap.cson"
    code_can_copy: true
    code: |
      '.pane .editor:not(.mini)':
        'tab': 'snippets:expand'
    after: |
      Copy the above couple of lines of code and paste them at the bottom of your keymap file.

      ![](keymap.jpg)

      **That’s it—Atom is ready to use!**

---
