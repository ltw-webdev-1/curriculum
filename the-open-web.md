---
layout: slide-deck
title: "The Open Web"
desc: "A small overview of the World Wide Web, why it matters to our program and how it became what it is today."

slides:
  - type: super-big-text
    content: |
      **The Open Web**

  - content: |
      ## World Wide Web

      Tim Berners-Lee—*1990*
      Invented at CERN for research documents
    notes: |
      - Originally the Web was made so scientists could easily share their research
      - *It was made for just text*
      - It has changed much since then with lots of new features and media abilities

  - content: |
      ## Specialized computers

      - Web servers—*just serve websites*
      - Chat servers
      - File servers
      - *etc.*
    notes: |
      - The web is really just a whole bunch of computers that are connected together
      - *And they all magically know how to speak the same languages*

  - content: |
      ## Connected computers

      Each with a unique name—the IP Address

      - 127.0.0.1
      - 2001:0db8:85a3:0000:0000:8a2e:0370:7334
    notes: |
      - The IP address is the unique name that computers use to address each other

  - content: |
      ## IPs are for computers

      *IP addresses are confusing for humans*

      Domains, like `github.com`, are for us

  - content: |
      ## DNS

      (Domain Name System)

      ### Maps Domains ⬌ IPs
    notes: |
      - The DNS is the way computers will take the human-friendly domain and convert it into a computer friendly IP address
      - It’s a system to computers that have huge lists of Domain-To-IP conversions

  - type: image
    image: dns-1.svg
    notes: |
      Everything starts in your browser, on your computer…

      1. You type in a domain you’d like to reach, like `google.ca`
      2. Your computer has no idea what `google.ca` is or where to find the computer that is `google.ca`

  - type: image
    image: dns-2.svg
    notes: |
      But your computer does know how to contact the DNS…

      1. Your computer sends a message to the DNS and says, “Hey DNS, I’m looking for ‘google.ca’ can you tell me where that is?”
      2. The DNS responds one of two ways:
        - “Yes, the IP address is 8.8.8.4”
        - or “No, try this other DNS that might know about ‘google.ca’; its IP address is 4.4.4.2”

      All of this usually happens really quickly, we’re talking milliseconds here. Your computer even keeps a cache/history of all the domain-to-IP mappings so it doesn’t have to look them up in the future

      And all the DNS computers regularly synchronize themselves all over the world

  - type: image
    image: dns-3.svg
    notes: |
      Now that your computer knows the IP address of the computer ‘google.ca’ is on it contacts that computer directly:

      - “Hey 8.8.8.4, I’m looking for ‘google.ca’, do you have it?”
        - “Yep, I have ‘google.ca’, here’s the `index.html` file you’ll need”
        - or maybe even, “Nope, I don’t have ‘google.ca’, but this computer over here does

        After your computer starts downloading the `index.html` file a whole series of other things start to happen…

  - content: |
      ## Websites are lots and lots of files…

      - HTML
      - CSS
      - Javascript
      - Images
      - Video

      *Each downloaded separately*
    notes: |
      Websites are just code (except for images & video)

      As your browser reads the HTML code it finds that it needs other code, like CSS or Javascript or other files like images and videos

      *Each of these things are downloaded to your computer separately*

      And often saved in the cache so they don’t need to be downloaded the next time you visit the website

  - content: |
      ## Performance matters

      The more files the slower your website

      *Performance is the most important design constraint*

---
