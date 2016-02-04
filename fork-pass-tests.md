---
layout: lesson
title: "Fork & pass tests"
desc: "Use the full power of GitHub for the whole whack load of code you have to write this year—copying my repos and getting things automatically marked."

video: "e3KbxNpcsdo"
hide_show_for_marks: true

steps:
  - title: "Fork the assignment repo"
    before: |
      Every coding exercise you do by yourself will start with a repository on GitHub. **You’ll follow this process for every code exercise to submit it and get it automatically graded.**

      That repository contains a bunch of files used to automatically mark and submit your code—running it through a battery of tests like checking commits, checking naming conventions, validation, indentation and more.

      [**Go to this repository and press the “Fork” button**](https://github.com/acgd-webdev-1/fork-pass-tests)

      Forking makes a copy of the repository, in your account, that you can edit.

      ![](fork.jpg)

      *Forking action…*

      ![](forking.jpg)
    notes:
      - label: "Reminder"
        text: "This is the process you’ll use for submitting all code exercises. If the code exercise points to a GitHub repository follow this process."
      - label: "Notice"
        text: "All the testing files, like `package.json`, `.tests`, `.editorconfig`, etc. should be left untouched."

  - title: "Clone the fork to your computer"
    before: |
      After forking, clone the repository to your computer by clicking the GitHub Desktop button.

      *You don’t have to make the `gh-pages` branch because that’s already done.*

      ![](clone.jpg)

      Make sure to choose your `web-dev` folder as the location—it isn’t easy to move the repository afterwards.

      ![](clone-2.jpg)

  - title: "Open folder in code editor"
    before: |
      When editing code it’s always best to drag the whole project folder to your code editor. That way it will give you a file listing on the left side.

      ![](folder.jpg)

  - title: "Create a new HTML file"
    before: |
      Create a new file and save it as `index.html` directly in your `fork-pass-tests` folder.

      Inside the file write just “Hello”—**and save.**

      ![](index.jpg)
    notes:
      - label: "Notice"
        text: "You’ll probably notice a whole bunch more files show up in the left of the file browser. They are part of the automated marking system and not part of your website—**completely ignore them.**"
      - label: "Naming conventions"
        text: "Don’t forget to follow the [naming conventions](http://learn-the-web.algonquindesign.ca/topics/naming-paths-cheat-sheet/#naming-conventions)."

  - title: "Test it in your browser"
    before: |
      Go to your folder in Finder and double click the HTML to preview in your browser.


      ![](local.jpg)
    notes:
      - label: "Shortcut"
        text: "In your code editor, right mouse click and press “Open in Browser”."
      - label: "Reminder"
        text: "Leave this tab open while working and jump back to the window when you want to test—press `⌘R` to refresh."

  - title: "Commit & sync"
    before: |
      If you’re satisfied with how it looks in your browser go to the GitHub app and commit the changes.


      ![](commit.jpg)

      Sync your changes to GitHub afterwards.

      ![](sync.jpg)
    notes:
      - label: "Reminder"
        text: "Make sure to write a descriptive commit message so I know what you did at this save point."

  - title: "Test live website in browser"
    before: |
      After you’ve synced to GitHub, we want to make sure it works on the live website before submitting.

      Go to the live url: `http://username.github.io/fork-pass-tests`
      Or go to “Settings” > “GitHub Pages” and click the link.

      ![](settings.jpg)
      ![](gh-pages.jpg)
      ![](live.jpg)
    notes:
      - label: "Reminder"
        text: "Always test the live website before submitting—it can easily look different from the local one."

  - title: "Create a pull request"
    before: |
      If you’re happy with the results of your website, after testing it live, you are ready to submit.

      *You can create a Pull Request at any point when working because we can use it as a Q&A discussion board for your code.*

      ![](pr.jpg)
      ![](pr-create.jpg)

      Change the Pull Request title to something descriptive like “Submitting assignment”.

      ![](pr-save.jpg)

  - title: "Check automated test status"
    before: |
      After creating your Pull Request the automated marking tests will immediately run. *They can take a little time, so just wait on this page for them to finish.*

      If the tests failed you’ll see the big red “x”—our goal is to make that a green check. **No green check, no grade.**

      ![](failed.jpg)

      By pressing the “details” link you can see a big list of what’s missing, each error will be described in red.

      ![](fail-details.jpg)

      In our current code we have two problems:

      1. We don’t have enough commit messages, representative of sloppy code
      2. The test is expecting “Hello World!” inside our `index.html`

      *So we need to fix them…*

  - title: "Fix problems, commit & sync"
    before: |
      Open up your code again and change `index.html` to say “Hello World!”.

      1. Save
      2. Refresh browser
      3. Commit
      4. Sync

      If everything is good you should get a green check mark! *Don’t forget to also test the live website to make sure it looks right.*

      ![](passed.jpg)
    notes:
      - label: "Notice"
        text: "Do not create another Pull Request. Now that one already exists, every commit will show on the original Pull Request and trigger the tests again."

  - title: "Automatically graded on Canvas"
    before: |
      As soon as you see a green checkmark your assignment will be submitted and graded on Canvas.

      *Go check it out to make sure.*

      ![](canvas.jpg)

---
