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

  - title: "Set up for hosting"
    before: |
      Before we write any code we’re going to set up the code repository so it’s a live, hosted website.

      By default the code stored on GitHub isn’t assumed to be a website—any code can be store on the service. We need to opt-into the free website hosting that GitHub provides, named GitHub Pages.
    image_steps:
      - url: "settings.jpg"
        text: |
          Click the “Settings” tab at the top of the repository.
      - url: "gh-pages.jpg"
        text: |
          Scroll down a little and under the “GitHub Pages” section, where it says “None”, select “master branch”.
      - url: "gh-pages-save.jpg"
        text: |
          Press “Save”

  - title: "Clone to computer"
    before: |
      After our repository is created and set up we need to clone (copy) it to our computer by pressing the “Clone to desktop” button.

      ![](clone.jpg)

      The GitHub Desktop application will pop up and ask you where to save the repository. Put it into your `web-dev` folder—**you don’t have to make a folder specifically for this repo, the app will make it for you.**

      ![](desktop-location.jpg)

      Then click the “Clone” button:

      ![](desktop-clone.jpg)

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

      Then send it to the GitHub website with the “Push” button.

      ![](push.jpg)
    notes:
      - label: "Shortcut"
        text: "`⌘Return` to save the commit."
      - label: "Shortcut"
        text: "`⌘P` to push your changes."
      - label: "Best practices"
        text: |
          Refer to the [**commit messages cheat sheet**](/topics/commit-message-cheat-sheet/) for the commit best practices.

  - title: "Test the live website"
    before: |
      After syncing our website will be live, online, at a specific URL.

      The URLs always look like this:
    code: |
      https://username.github.io/repo-name/
    after: |
      Find the URL on the GitHub website under the repository’s “Settings” tab.

      ![](settings-url.jpg)

      **And you should see your website!** The URL is completely open to anyone in the world.

      ![](live.jpg)

  - title: "Fork instead…"
    before: |
      **For all the code exercises in class we don’t have to go through the process of setting up for hosting—the assignments are all ready.**

      **We’ll be using the [fork & pass tests method with Markbot](/courses/web-dev-1/using-markbot/) to hand in all work.**
      [**That lesson comes next ➔**](/courses/web-dev-1/using-markbot/)

---
