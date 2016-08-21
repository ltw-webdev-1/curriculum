---
layout: lesson
title: "Using your code editor"
desc: "A quick overview of how to use the Atom code editor—though many of these techniques apply to Sublime Text and many others."

hide_show_for_marks: true
hide_markbot: true

extra_tutorials:
  - title: "Keyboard shortcut cheat sheet"
    url: keyboard-shortcut-cheat-sheet
    highlight: true
  - title: "Code editors"
    url: code-editors
  - title: "Snippets cheat sheet"
    url: snippets-cheat-sheet
    highlight: true
  - title: "Code character cheat sheet"
    url: code-character-cheat-sheet

video: "09XV2psDAZ4"

steps:
  - title: "Opening projects"
    before: |
      The best way to open code in Atom is to drag a whole folder from finder right to the Atom icon in your dock.

      ![](drag-to-dock.jpg)

      **The best part about this is that all the files within the folder will then be listed on the right hand side for easy access.**

      ![](sidebar.jpg)

      ### Opening multiple projects

      Same idea applies here: drag the folder to the dock icon. This will open a completely new Atom window which is significantly help you keep all the code files organized.
    notes:
      - label: "Shortcut"
        text: "If you don’t have Atom in your dock, put it there right now—you’ll be needing it a lot."
      - label: "Shortcut"
        text: "Use ``⌘` `` to switch between multiple project windows in Atom."

  - title: "Previewing & opening files"
    before: |
      **Single clicking** on a file within the Atom sidebar will preview that document in the Atom window.

      *You can tell it’s being previewed because a tab doesn’t get created or the name on the tab doesn’t change.*

      **Double clicking** on a files will open that document into a new tab in Atom that you can then edit.
    notes:
      - label: "Shortcut"
        text: "Pressing `⌘P`—then you can search through all the files and open one without taking your hands off the keyboard."

  - title: "Making a new file"
    before: |
      In Atom, since we installed a package, there’s a shortcut key that will make a new file and save it directly into the folder we have open.

      ![](advanced-open-file.jpg)

      1. Press `⌘⌥O` to trigger a new dialog.
      2. Type the name of the file, including the extension.
      3. Hit `Return`—the file is saved into the folder you opened.

  - title: "Navigating between tabs"
    before: |
      Using a mouse is slow and cumbersome—that’s why keyboard shortcuts are amazing.

      ![](tab-numbers.gif)

      To navigate between tabs you can use the `⌘` key and numbers:
    shortcuts:
      - keys: '`⌘1`'
        text: 'Will go to the first tab.'
      - keys: '`⌘2`'
        text: 'Will go to the second tab.'
      - keys: '`⌘3`'
        text: 'Will go to the third tab.'
      - keys: '*etc.*'
        text: ''
    after: |
      Or you can use `⌘⇧[` and `⌘⇧]` to go backwards and forwards through the tabs.

  - title: "Navigating code"
    before: |
      Navigating code in Atom is the same as any text field in MacOS—all the same shortcuts apply.

      *It’s a really good idea to get a handle on these shortcuts because they will greatly increase your efficiency.*
    shortcuts:
      - keys: '`⌘C`'
        text: 'Copy the selected text.'
      - keys: '`⌘X`'
        text: 'Cut the selected text.'
      - keys: '`⌘V`'
        text: 'Paste the previously copied item.'
      - keys: '`⌘Z`'
        text: 'Undo the recent change.'
      - keys: '`⌘⇧Z`'
        text: 'Redo the recent undo.'
      - keys: '`⌘F`'
        text: 'Find within this file.'
      - keys: '`⌘G`'
        text: 'Find next matching item.'
      - keys: '`⌘⇧G`'
        text: 'Find previous matching item.'
      - keys: '`⌘→`'
        text: 'Move to the end of the line.'
      - keys: '`⌘←`'
        text: 'Move to the start of the line.'
      - keys: '`⌥→`'
        text: 'Move to the next word.'
      - keys: '`⌥←`'
        text: 'Move to the previous word.'
      - keys: '`⌘↑`'
        text: 'Move to the top of the file.'
      - keys: '`⌘↓`'
        text: 'Move to the bottom of the file.'
      - keys: '`Shift+Arrows`'
        text: |
          - Highlight text.
          - Can be combined with `⌘` & `⌥`

    after: |
      ### Manipulating multiple lines of code

      ![](multi-line.gif)

      By pressing the `` key and clicking on multiple lines you can change code on many lines at once.

      **The great thing is that all the keyboard shortcuts you use for one line will now apply to all of those lines too!**

  - title: "Other important keyboard shortcuts"
    before: |
      Here are a few other important keyboard shortcuts you should remember to help you get more efficient:
    shortcuts:
      - keys: '`⌘⇧P`'
        text: 'Open the command palette to search everything the code editor can do.'
      - keys: '`⌘/`'
        text: 'Toggle comments on/off for code, knowing the correct language.'
      - keys: '`⌘]`, `Tab`'
        text: 'Indent a line of code or multiple lines of code.'
      - keys: '`⌘[`, `Shift+Tab`'
        text: 'Outdent a line of code or multiple lines of code.'
      - keys: '`⌘⌥F`'
        text: 'Find and replace within this file.'
      - keys: '`⌘⇧F`'
        text: 'Find and replace within this folder.'
      - keys: '`⌘R`'
        text: 'Filter & find by keyword in this file.'
      - keys: '`⌃⌘↑`'
        text: 'Move a line up.'
      - keys: '`⌃⌘↓`'
        text: 'Move a line down.'
      - keys: '`⌘J`'
        text: 'Join the line below with this line.'
      - keys: '`⌘⇧D`'
        text: 'Duplicate this line.'
      - keys: '`⌃⇧K`'
        text: 'Delete this line.'

---
