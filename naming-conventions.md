---
layout: slide-deck
title: "Naming conventions"
desc: "An overview of the naming conventions we’ll follow for all of the Web Dev courses."

slides:
  - type: super-big-text
    content: |
      **Naming conventions**

  - content: |
      ## Naming conventions

      1. All lowercase.
      2. No spaces!
      3. Only letters, numbers, and dashes (-).

      **These apply to all files & all folders created for the Web Dev courses.**

  - content: |
      ## All lowercase

      Different operating systems treat capitalization in filenames differently.

      **We’ll standardize on lowercase to make things more consistent and easier.**
    notes: |
      MacOS & Windows are case-insensitive operating systems: they don’t distinguish between upper & lower case letters.

      `hello.txt` & `HELLO.txt` are exactly the same file.

      Linux and other Unix-based operating systems are case-sensitive—when we deploy our websites they will be going onto Linux-based web hosts.

      `hello.txt` & `HELLO.txt` are completely different files.

  - content: |
      ## No spaces!

      URLs literally cannot have spaces in them.

      **Since we’re making websites & everything is a URL, our filenames also cannot have spaces.**
    notes: |
      Technically URLs can have spaces, but not space characters. In URLs spaces are usually encoded as: `+` or `%20`

  - content: |
      ## Only letters, numbers, and dashes (-)

      URLs only allow ASCII characters unless the characters are encoded.

      **Since the specification specifically disallows non-ASCII characters our filenames will use only basic characters.**
    notes: |
      As for dashes, that’s a Google-specific problem:

      *Google will separate words with dashes into separate keywords:*
      - `prehistoric-creatures-of-the-deep.jpg` becomes `prehistoric`, `creatures` `deep`

      *Google combines together words separated with underscores:*
      - `underwater_amphibians.html` you’d have to search for exactly `underwater_amphibians` to find this page
      - This is sometimes a good thing, specifically with code & function names—but in most situations it doesn’t help search results.

  - content: |
      ## Good

      ```
      index.html
      dinosaurs.jpg
      t-rex.jpg
      prehistoric-creatures-of-the-deep.html
      ```

  - content: |
      ## Bad

      ```
      Index.html   <-- Web server won’t find & load the page
      t rex.jpg    <-- Browser may not be able to find the image
      prehistoric_creatures_of_the_deep.jpg    <-- Google will treat this as a single word
      ```

  - content: |
      ## Naming conventions

      1. All lowercase.
      2. No spaces!
      3. Only letters, numbers, and dashes (-).

  - content: |
      ## Videos & tutorials

      - [Naming conventions ➔](/topics/naming-conventions/)
      - [Naming & paths cheat sheet ➔](/topics/naming-paths-cheat-sheet/)

---
