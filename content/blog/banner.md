---
title: "Banner"
date: 2018-03-05T11:59:04-08:00
categories: ["docs"]
toc: true
header: "banner-flipped.png"
---
You can set the banner via Hugo params. This can be done site-wide via config.toml and also overridden per-page via frontmatter.

# Site Wide Banner Image
Add the following to your config.toml, replacing `banner.png` with the name of your banner image.

```
[params]
  header = "banner.png"
```

# Per Page Banner Image
As you can see, this post has a different banner than the rest of the site. You can _optionally_ set a custom banner image per page/post by including this snippet in the frontmatter:    
`header: "NAME-OF-BANNER.png"`
