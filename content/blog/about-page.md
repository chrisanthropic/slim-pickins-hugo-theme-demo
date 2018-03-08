---
title: "About Page"
date: 2018-03-08T00:59:04-08:00
categories: ["docs"]
toc: true
---
This theme includes a prebuilt about page layout.

# How to Add an About Page
- Create a new page `content/about.md` with the following front-matter:

```
---
Title: About
type: about
logo: "/PATH/TO/A/LOGO/OR/PHOTO.jpg"
---
```

- Add any content to page itself.

# Add it to the Navigation Menu
- Optionally, you can add the page to the [navigation menu](/blog/navigation/) by adding the following to the front-matter:

```
menu:
  main:
    identifier: "about"
    name: "about"
    weight: 4
```
