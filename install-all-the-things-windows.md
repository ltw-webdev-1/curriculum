---
layout: lesson
title: "Install all the things!"
desc: "Set up your computer, install all the different web browsers, install a code editor, and set up GitHub."

hide_markbot: true

steps:
  - title: "Configure File Explorer"
    before: |
      Let’s change a few settings on your computer to make development life easier.

      ![](file-explorer.jpg)

      1. Go to a folder.
      2. Go to the “View” tab.
      3. Make sure “File name extensions” is checked.
    notes:
      - label: "Mac"
        text: |
          If you’re a Mac user, this tutorial isn’t for you.
          <br>[**☛ Go to the Mac installation tutorial.**](/courses/web-dev-1/install-all-the-things/)

  - title: "Install Firefox"
    before: |
      We need to install a bunch of browsers because, as web designers, we don’t know what browser someone will be using—so we need to test our websites in all of them.

      1. Go to Mozilla’s website and [download Firefox](http://getfirefox.com/).
      2. Run the installer on your computer by double clicking.
    notes:
      - label: "Warning"
        text: "Make sure to only download Firefox directly from Mozilla—other websites may inject malware."

  - title: "Install Chrome"
    before: |
      Go to Google’s website and [download Chrome](https://www.google.com/chrome/).
      <br>*(Ditto steps above.)*
    notes:
      - label: "Warning"
        text: "Make sure to only download Chrome directly from Google—other websites may inject malware."

  - title: "Install Opera"
    before: |
      Go to Google’s website and [download Chrome](https://www.google.com/chrome/).
      <br>*(Ditto steps above.)*
    notes:
      - label: "Warning"
        text: "Make sure to only download Opera directly from Opera—other websites may inject malware."

  - title: "Get HTML files to open properly"
    before: |
      This will make it so double clicking HTML files opens your browser instead of a code editor.

      ![](properties.jpg)

      1. <a href="fixer.html" download="fixer.html">Download this HTML file.</a>
        *(If clicking this link doesn’t download the file, `Right Click > Download Linked File`.)*
      2. Go to where it was downloaded and right click—press “Properties”.
      3. Under the “Opens with” section, click the “Change…” button and set it to “Firefox” or “Chrome”.
      5. Close the properties window and trash the HTML file.

  - title: "Create a GitHub account"
    before: |
      Git is a version control system and GitHub allows us to host all our code & websites online. (More on these two things next week.)

      1. Go to [GitHub](https://github.com/) and sign up for an account.
        *Choose whatever username and email address you’d like.*
      2. Choose the *free* plan when you get to that screen.

      You’ll be handing in your profile page to Canvas later.
    notes:
      - label: "Remember"
        text: "Though it shouldn’t need to be said: remember your password!"

  - title: "Install GitHub Desktop"
    before: |
      We need to install the GitHub Desktop application so that we can manage and upload our code to GitHub.

      1. Download the app from the [GitHub Desktop](https://desktop.github.com/) website.
      2. Double click the installer and let it do its thing.
      3. Sign in with your GitHub username, email address, and password.
      4. When it asks you to look for repositories—press “Skip”.
      5. *It will try to get you to do a tutorial with these little pop-up bubbles—don’t bother, press the little “x” icon on the bubble.*

  - title: "Install the Command Line Tools"
    before: |
      We need to install some extra development tools on our computer so Markbot can work well.

      **Go to [Git’s download page](https://git-scm.com/download/win) and download the Windows version.**

      Install Git onto your computer. One of the setup screens has options we have to change.

      *On the “Adjusting your PATH environment” screen, switch to “Use Git from the Windows Command Prompt”.*

      ![](git.jpg)

  - title: "Install the Java Developer Kit"
    before: |
      We need to install the JDK because the automated marking program, Markbot, needs access to Java for performing some of it’s tasks.

      Go to the JDK download page on [Oracle’s Java Downloads](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) website.

      ![](jdk-license.jpg)

      *Don’t forget to accept the license agreement.*

      ![](jdk.jpg)

      1. Download the JDK for your computer.
      3. Double click the installer and let it do its thing.
      5. Delete the downloaded file.

  - title: "Install Markbot"
    before: |
      All of the coding exercises we do in this class will be using Markbot to automatically grade your work. So, we need to set that up.

      1. Download [Markbot](https://assets.learn-the-web.algonquindesign.ca/markbot/Markbot%20Setup.exe1). (*or [Markbot for Mac](https://assets.learn-the-web.algonquindesign.ca/markbot/Install%20Markbot.dmg)*)
      3. Double click the installer and let it do its thing.
      5. Delete the downloaded file.

      **Open up Markbot and sign in with your GitHub username.**

      *If Markbot gives you an “Unidentified developer” security warning—click the “More info” link and press “Run anyways”.*

      ![](markbot.jpg)
---
