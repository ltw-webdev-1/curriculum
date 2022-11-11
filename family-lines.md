---
layout: slide-deck
title: "Family lines"
desc: "An activity to help reinforce indentation best practices & the understanding of parent-child relationships in HTML."

group_work: true

slides:
  - type: super-big-text
    content: |
      **Family lines**

  - content: |
      ## What & why

      When learning HTML (and Flexbox) the parent-child relationships of the elements is critical to good structure & code understanding.

      We can use code indentation to help us distinguish the parent-child relationships in HTML and reinforce the structure of our code.

      **Indentation is a memory aid to find parent & child relationships.**

  - type: big-text
    content: |
      ## Set up

      1. Form into pairs
      2. [Download the files](https://github.com/ltw-webdev-1/family-ties/archive/master.zip)
      3. Print “family-ties.pdf”
      4. Get out a pencil for marking up the paper

  - type: big-text
    content: |
      ## Instructions

      1. Draw lines to match the opening & closing tags
      2. Answer questions about family relationships

  - type: big-text
    content: |
      ![](atreides.png)

      1. Parent of `article#paul`?
      2. Sibling of `article#paul`?
      3. Child of `article#paul`?

  - type: two-col-code
    col1:
      html: |
        <h1>Skywalkers</h1>

        <main id="shmi">
        <article id="vader">
        <ol id="leia">
        <li id="jaina"></li>
        <li id="jacen"></li>
        <li id="anakin"></li>
        </ol>
        <strong id="luke"></strong>
        </article>
        </main>
    col2:
      before: |
        #### 1. Parent of `article#vader`?
        #### 2. Sibling of `li#jacen`?
        #### 3. Sibling of `strong#luke`?
        #### 4. Great-grandparent of `li#anakin`?

  - type: two-col-code
    col1:
      html: |
        <h1>Weasleys</h1>

        <ol id="molly">
          <li id="bill"></li>
          <li id="charlie"></li>
          <li id="percy"></li>
          <li id="fred"></li>
          <li id="george"></li>
          <li id="ron">
            <span id="rose"></span>
            <span id="hugo"></span>
          </li>
          <li id="ginny">
            <span id="james"></span>
            <span id="albus"></span>
            <span id="lily"></span>
          </li>
        </ol>
    col2:
      before: |
        #### 1. Parent of `li#ron`?
        #### 2. Parent of `span#albus`?
        #### 3. Sibling of `li#george`?
        #### 4. Grandchild of `ol#molly`?

  - type: two-col-code
    col1:
      html: |
        <h1>Starks</h1>

              <article id="rickard">
        <div id="eddard">
            <strong id="robb"></strong>
        <strong id="sansa"></strong>
          <strong id="arya"></strong>
                  <strong id="bran"></strong>
          <del id="rickon"></del>
          </div>
                  <p id="benjen"></p>
              <div id="lyanna">
        <small id="jon"></small>
                    </div>
        </article>
    col2:
      before: |
        #### 1. Parent of `small#jon`?
        #### 2. Sibling of `strong#arya`?
        #### 3. Child of `div#eddard`?
        #### 4. Sibling of `div#eddard`?

---
