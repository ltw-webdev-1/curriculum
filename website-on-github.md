---
layout: lesson
title: "Website on GitHub"
desc: "Create a repository on GitHub, set it up to host a website, and launch a single page site."

hide_markbot: true

video: "okAvvY_LeyI"

extra_tutorials:
  - title: "Version control & GitHub"
    url: version-control-github
  - title: "Version control & GitHub slide deck"
    url: /courses/web-dev-1/version-control-github/
  - title: "Hosting with GitHub Pages"
    url: github-pages

steps:
  - title: "Sign in to GitHub"
    before: |
      **We’ll be using GitHub as our code version control system—and our web host.**

      We’ll put all of our coding exercises on GitHub where they will be live websites visible to anybody.
    notes:
      - label: "Reminder"
        text: "For most coding exercises you won’t need to perform these steps, you’ll be using the [fork & pass tests method](/courses/web-dev-1/fork-pass-tests/) to hand in all your work."

  - title: "Create a new repo"
    before: |
      Before starting this project we need to create a repository on GitHub. The repository will hold all of our website code, all the history of our project, and be our host.

      ![](repo.jpg)

      When we get to the new repository page there’s a few fields to complete.

      ![](repo-new.jpg)

      - **Repository name** — create a unique name for the repo, make sure it follows the [naming conventions](/topics/naming-paths-cheat-sheet/#naming-conventions).
      - **Description** — come up with a short description describing the purpose of the project.
      - **Public/Private** — choose “Public” because we don’t have a paid accounts.
      - **Initialize this repository with a README** — always make sure this is enabled.
    notes:
      - label: "Naming conventions"
        text: "Don’t forget to follow the [naming conventions](/topics/naming-paths-cheat-sheet/#naming-conventions)."

  - title: "Create the gh-pages branch"
    before: |
      Our repository is completely usable—but it’s not a live website. By default GitHub allows us to share code online, but we have to opt-in to their website hosting service.

      To opt-in to the hosting service we have to make a new branch named `gh-pages`

      ![](gh-pages.jpg)

      1. Click the “Branch” button.
      2. Type `gh-pages` into the text field.
      3. Press “Create branch: gh-pages” to execute.

    notes:
      - label: "Shortcut"
        text: "Hit `Return` after typing `gh-pages` to create the branch."

  - title: "Set the default branch"
    before: |
      Now we have two branches in our repository—but we only need `gh-pages`

      We should set `gh-pages` as the default branch and delete the old `master` branch.
    image_steps:
      - url: branches.jpg
        text: "Click “2 branches” in the top navigation."
      - url: change-default.jpg
        text: "Press the “Change default branch” button."
      - url: master-default.jpg
        text: "Change `master` to `gh-pages`"
      - url: update.jpg
        text: "Press “Update”."
      - url: back-to-repo.jpg
        text: "Go back to the main page for the repo."
      - url: branches-2.jpg
        text: "Press “2 branches” again."
      - url: delete-master.jpg
        text: "Delete `master` by pressing the trash icon."
    after: |
      **We now have a completely hosted GitHub website repository. But it doesn’t work yet because there’s no HTML in it.**

  - title: "Clone to computer"
    before: |
      After our repository is created and set up we need to clone (copy) it to our computer by pressing the “Clone to desktop” button.

      ![](clone.jpg)

      The GitHub Desktop application will pop up and ask you where to save the repository. Put it into your `web-dev` folder—**you don’t have to make a folder specifically for this repo, the app will make it for you.**

      ![](desktop.jpg)

  - title: "Open in code editor"
    before: |
      We can now open up the project in our code editor.

      ![](folder.jpg)

      Drag **the folder** that was created to your code editor in the Dock.

      ![](code-editor.jpg)

  - title: "Add an HTML file"
    before: |
      We’re ready to make a new HTML file.

      Go to `File > New` or press `⌘N` to make a new file.
    folders:
      - label: "first-website"
        type: folder
      - label: "index.html"
        indent: 1
    after: |
      **Immediately save the file.** Call it exactly `index.html`. Put it into the `first-website` folder.

      ![](index.jpg)
    notes:
      - label: "Naming conventions"
        text: "Don’t forget to follow the [naming conventions](/topics/naming-paths-cheat-sheet/#naming-conventions)."
      - label: "Shortcut"
        text: "Use `⌘S` to save."
      - label: "Shortcut"
        text: "Use `⌘⌥N` to make, name, and save a new file in one step. Only works when a folder is open in your code editor."

  - title: "Write some code"
    before: |
      In the `index.html` file write a little bit of HTML:
    code_lang: "html"
    code_file: "index.html"
    code: |
      <h1>It works!</h1>
    after: |
      ![](html.jpg)

      **Then save!**

  - title: "Test the website"
    before: |
      After saving our HTML we need to test it in a web browser to confirm it works.

      **Use Chrome or Firefox to test websites while developing—Safari isn’t good enough.**

      Double click on the icon in Finder to open it in the browser.

      ![](double-click.jpg)

      Make sure it looks all good in the browser.

      ![](local.jpg)

      *Leave this tab open all the time while working to easily jump back and forth.*
    notes:
      - label: "Reminder"
        text: "Leave this tab open while working and jump back to the window with `⌘Tab` when you want to test—press `⌘R` to refresh the browser."
      - label: "Shortcut"
        text: "`⌘S`, `⌘Tab`, `⌘R`, `⌘Tab`, repeat."

  - title: "Commit & sync"
    before: |
      When happy with how it looks in the browser it’s time to make a commit to save the state of our code.

      **Make sure to write a descriptive message!**

      ![](commit.jpg)

      Then sync it to the GitHub website.

      ![](sync.jpg)
    notes:
      - label: "Shortcut"
        text: "`⌘Return` to save the commit."
      - label: "Shortcut"
        text: "`⌘S` to sync your changes."

  - title: "Test the live website"
    before: |
      After syncing our website will be live, online, at a specific URL.

      The URLs always look like this:
    code: |
      https://username.github.io/repo-name/
    after: |
      Find the URL on the GitHub website under the repository’s “Settings” tab.

      ![](settings.jpg)

      **And you should see your website!** The URL is completely open to anyone in the world.

      ![](live.jpg)

  - title: "Fork instead…"
    before: |
      **For all the code exercises in class we don’t have to go through the `gh-pages` branching set up process above.**

      **We’ll be using the [fork & pass tests method with Markbot](/courses/web-dev-1/using-markbot/) to hand in all work.**
      [**That lesson comes next ➔**](/courses/web-dev-1/using-markbot/)

---
