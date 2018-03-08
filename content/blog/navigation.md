---
title: "Navigation"
date: 2018-03-05T11:59:04-08:00
categories: ["docs"]
toc: true
---
Slim Pickins Hugo theme uses a fully responsive HTML + CSS navigation bar with 2 navigation areas:
- Primary navigation
- Social media links

# Primary Navigation
Navigation can be set via the config.toml file _or_ in the front matter of a page. This demo site uses both.

First, we enable the menu via config.toml with the following line of code: `SectionPagesMenu = "main"`
Next, we create a new menu entry in the frontmatter of the following pages: **Home**, **Gallery**, and **About**.

## Home
/content/_index.html

```
---
menu:
  main:
    identifier: "home"
    name: "home"
    weight: 1
---
```

## Gallery
/content/gallery.md

```
---
menu:
  main:
    identifier: "gallery"
    name: "gallery"
    weight: 3
--- 
```

## About
/content/about.md

```
---
menu:
  main:
    identifier: "about"
    name: "about"
    weight: 4
---
```

## Blog
This is our example of defining menus in config.toml instead of the frontmatter for that page. In this case I chose to define it here for demonstration purposes _as well as_ working around a quirk I experienced. In short, my chosen layout structure broke `active` class menu highlighting for blog posts when I defined the menu in the page meta data but worked as expected when defined in the config.toml file.

So, here's the exeample of what was added to config.toml to create the Blog entry of the navigation menu.

```
[[menu.main]]
  name = "blog"
  identifier = "blog"
  url = "/blog/"
  weight = 2
```

# Social Media Links
The `socials` menu is defined and modified in the config.toml file using Hugo's [menu management](https://gohugo.io/content-management/menus/#add-non-content-entries-to-a-menu) feature.

Below is an example of the code used to generate the socials menu of this demo:

```
[[menu.socials]]
  name = "linkedin"
  identifier = "linkedin"
  url = "https://www.linkedin.com"
  weight = 1

[[menu.socials]]
  name = "tumblr"
  identifier = "tumblr"
  url = "https://www.tumblr.com"
  weight = 2

[[menu.socials]]
  name = "facebook"
  identifier = "facebook"
  url = "https://www.facebook.com"
  weight = 3

[[menu.socials]]
  name = "twitter"
  identifier = "twitter"
  url = "https://www.twitter.com"
  weight = 4

[[menu.socials]]
  name = "github"
  identifier = "github"
  url = "https://www.github.com"
  weight = 5

[[menu.socials]]
  name = "rss"
  identifier = "rss"
  url = "/index.xml"
  weight = 6
```
