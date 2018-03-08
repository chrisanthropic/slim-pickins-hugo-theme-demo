---
title: "Custom Partials"
date: 2018-03-08T02:59:04-08:00
categories: ["docs"]
toc: true
categorylist: true
---
This theme includes a few handy custom partials you can use.

# Partials
## Table Of Contents
The `table of contents` partial creates a Table of Contents for posts based that is based on headings. You can set it on a per-post basis by adding the following line the yaml frontmatter of any post: 
```
---
toc: true
---
```

## Recent Posts
The `recent posts` partial creates a list of the 10 most recent posts. You can add it to a page by importing the partial in any layout:  
`{{ partial "recent_posts.html" . }}`

## Category List
The `category list` partial creates a list of all cateories in use, followed by a `(#)` of how many posts exist in that category. You can set it on a per-post basis by adding the following line to the yaml frontmatter of any post:  
```
---
categorylist: true
---
```
