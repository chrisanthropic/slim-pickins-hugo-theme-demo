---
title: "Gallery"
date: 2018-03-07T11:59:04-08:00
categories: ["docs"]
toc: true
---
This theme includes a prebuilt gallery layout & lightbox pop-up that can be configured via Hugo's Data feature.

# How to Add a Gallery Page
- Create a new page `content/gallery.md`
- Optionally, you can add the page to the [navigation menu](/blog/navigation/) by adding the following to the front-matter:
```
menu:
      main:
        identifier: "gallery"
        name: "gallery"
        weight: 3
```

## How to Add a Single Gallery Image
- with the following front-matter content:
```
---
Title: Gallery
type: gallery
layout: single
---
```

- Create the data file `data/gallery.yml` with the following content:

```
---
name: "gallery"
images:

- image: ""
  order: 1
  artist: ""
  title: ""
  description: ""
---
```

- Fill out the data:
  - image: This should be a relative path to image file
  - order: This is what order the images are displayed in when using the lightbox pop-up
  - artist: If filled out it will display this beneath the image when using the lightbox pop-up
  - title: If filled out it will display this beneath the image when using the lightbox pop-up
  - description: If filled out it will display this in the lightbox description

## How to Add Multiple Gallery Images

- Add additional 'image' blocks to the data file `data/gallery.yml`:

``` 
- image: ""
  order: 
  artist: ""
  title: ""
  description: ""
```

- Example with 3 images:

```
---
name: "gallery"
images:

- image: ""
  order: 1
  artist: ""
  title: ""
  description: ""

- image: ""
  order: 2
  artist: ""
  title: ""
  description: ""

- image: ""
  order: 3
  artist: ""
  title: ""
  description: ""
---
```

# Working Example for This Site
Below is the code used to create the gallery page of this demo site:

```
---
name: "gallery"
images:
- image: "/images/galleries/covers/Thieves-at-Heart.jpg"
  order: 1
  artist: "Sam Wood"
  title: "Thieves at Heart"
  description: "Original cover art by Sam Wood for Tristan J. Tarwater's 'Thieves at Heart' novel."
 
- image: "/images/galleries/covers/Self-Made-Scoundrel.jpg"
  order: 2
  artist: "Sam Wood"
  title: "Self-Made Scoundrel"
  description: "Original cover art by Sam Wood for Tristan J. Tarwater's 'Self-Made Scoundrel' novel."

- image: "/images/galleries/covers/Red-Moon-Rising.jpg"
  order: 3
  artist: "Sam Wood"
  title: "Red Moon Rising"
  description: "Original cover art by Sam Wood for Tristan J. Tarwater's 'Red Moon Rising' novel."

- image: "/images/galleries/covers/TheMaraudersIsland.jpg"
  order: 4
  artist: "Mildred Louis"
  title: "The Marauders' Island"
  description: "Original cover art by Mildred Louis for Tristan J. Tarwater's 'The Marauders' Island' novel."

- image: "/images/galleries/covers/A-Fistful-of-Lunars.jpg"
  order: 5
  artist: "Adrian Ricker"
  title: "A Fistful of Lunars"
  description: "Original cover art by Adrian Ricker for Tristan J. Tarwater's graphic novel 'A Fistful of Lunars'."

- image: "/images/galleries/covers/Lone-Idiot-and-Cub.jpg"
  order: 6
  artist: "Adrian Ricker"
  title: "Lone Idiot and Cub"
  description: "Original cover art by Adrian Ricker for Tristan J. Tarwater's graphic novel 'Lone Idiot and Cub'."

- image: "/images/galleries/covers/Tired.jpg"
  order: 7
  artist: "Genue Revuelta"
  title: "Tired"
  description: "Original cover art by Genue Revuelta for Tristan J. Tarwater's short story 'Tired'."
---
```
