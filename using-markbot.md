---
layout: lesson
title: "Using Markbot"
desc: "Use Markbot to check that your code follows all the requirements and submit it for grades when it passes."

video: "Li9RIuDSMFo"
hide_show_for_marks: true
hide_markbot: true

extra_tutorials:
  - title: "Markbot download (MacOS)"
    url: "https://assets.learn-the-web.algonquindesign.ca/markbot/Install%20Markbot.dmg"
  - title: "Markbot download (Windows)"
    url: "https://assets.learn-the-web.algonquindesign.ca/markbot/Markbot%20Setup.exe"
  - title: "Markbot source code"
    url: "https://github.com/thomasjbradley/markbot"

steps:
  - title: "Fork the assignment repo"
    before: |
      Every coding exercise you do by yourself will start with a repository on GitHub. **You’ll follow this process for every code exercise to submit it and get it automatically graded.**

      The repository contains a `.markbot.yml` hidden file used to check and submit your code—running it through a battery of tests like checking commits, checking naming conventions, validation, indentation and more.

      ### [Go to this repository and press the “Fork” button ➔](https://github.com/acgd-webdev-1/using-markbot)

      Forking makes a copy of the repository, in your account, that you can edit.

      ![](fork.jpg)

      *Forking action…*

      ![](forking.jpg)
    notes:
      - label: "Reminder"
        text: "This is the process you’ll use for submitting all code exercises. If the code exercise points to a GitHub repository follow this process."
      - label: "Notice"
        text: "All the testing files, like `.markbot.yml`, `.gitignore`, `.editorconfig`, etc. should be left untouched."

  - title: "Clone the fork to your computer"
    before: |
      After forking, clone the repository to your computer by clicking the GitHub Desktop button.

      *You don’t have to set this repo up as a hosted website because that’s already done.*

      ![](clone.jpg)

      Make sure to choose your `web-dev` folder as the location—it isn’t easy to move the repository afterwards.

      ![](clone-save.jpg)

  - title: "Open folder in code editor"
    before: |
      When editing code it’s always best to drag the whole project folder to your code editor. That way it will give you a file listing on the left side.

      ![](folder.jpg)

  - title: "Create a new HTML file"
    before: |
      Create a new file and save it as `index.html` directly in your `using-markbot` folder.

      Inside the file write just “Hello”—**and save.**

      ![](index.jpg)
    notes:
      - label: "Notice"
        text: "You’ll probably notice a whole bunch more files show up in the left of the file browser. They are part of the automated marking system and not part of your website—**completely ignore them.**"
      - label: "Naming conventions"
        text: "Don’t forget to follow the [naming conventions](/topics/naming-paths-cheat-sheet/#naming-conventions)."

  - title: "Test it in your browser"
    before: |
      Go to your folder in Finder and double click the HTML to preview in your browser.

      ![](local.jpg)
    notes:
      - label: "Shortcut"
        text: "In your code editor, right mouse click and press “Open in Browser”."
      - label: "Reminder"
        text: "Leave this tab open while working and jump back to the window when you want to test—press `⌘R` to refresh."

  - title: "Commit"
    before: |
      If you’re satisfied with how it looks in your browser go to the GitHub app and commit the changes.

      ![](commit.jpg)
    notes:
      - label: "Reminder"
        text: "Make sure to write a descriptive commit message so I know what you did at this save point."

  - title: "Check with Markbot"
    before: |
      After you’ve completed your work and you’re ready to hand it in: **drag and drop the folder into Markbot.**

      ![](drag-to-markbot.jpg)

      If the tests fail you’ll see red “x”s—our goal is to get green checks. **No green check, no grade.**

      ![](failed.jpg)

      We can scroll through the big list of what’s missing, each error will be described & point to the line of code.

      In our current code we have a few problems:

      1. We don’t have enough commit messages, representative of sloppy code and poor forethought
      2. The test is expecting “Hello World!” inside our `index.html`
      3. The website isn’t live online yet—because we haven’t pushed

      *So we need to fix them…*

  - title: "Fix problems, Markbot, commit"
    before: |
      Open up your code again and change the content inside `index.html` to say “Hello World!”.

      1. Save
      2. Refresh browser
      3. Check Markbot
      4. Commit
      5. Push

      If everything is good you should get a green check mark!

      ![](passed.jpg)
    notes:
      - label: "Shortcut"
        text: "To run the test in Markbot again press `⌘R`."

  - title: "Test the live website"
    before: |
      After you’ve finalized your code, making sure it passes Markbot, we need to test the live website.

      *We want to make sure it works on the live website before submitting for grades.*

      - Go to the live url: `http://username.github.io/using-markbot`
      - Or go to `Settings > GitHub Pages` and click the link.

      ![](settings.jpg)
      ![](gh-pages.jpg)

      *It’s alive!*

      ![](live.jpg)
    notes:
      - label: "Reminder"
        text: "Always test the live website before submitting—it can easily look different from the local one."

  - title: "Submit for grades"
    before: |
      When everything is working perfectly, submit the assignment for grades with the big button in Markbot.

      ![](submit.jpg)

      [**Go check Progressinator it out to make sure.**](https://progress.learn-the-web.algonquindesign.ca/)

      ![](progressinator-grades.jpg)

---
