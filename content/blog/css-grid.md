---
title: "Grid with CSS Grid"
date: 2018-02-17T11:59:04-08:00
categories: ["docs"]
toc: true
---
This theme uses a mobile-first CSS Grid to create our grid layout with overrides for screens larger than 1280px.

# Grid
The `grid` CSS class defines the base grid:

## Mobile
```
.grid {
  display: grid;
  width: 100%;
  height: 100vh;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: 50px 44px auto auto 50px;
}
```

- spread over 100% width and 100vh height of the screen
- 12 evenly divided columns
- 5 rows
  - header: 50px height
  - navigation: 44px height
  - main content: auto
  - sidebar: auto
  - footer: 50px height

## Larger than 1280px
```
@media (min-width: 1280px) {
  .grid {
      grid-template-rows: 300px 44px auto 54px;
  }
```

You'll notice that there are only 4 rows defined for larger screens, this is because on larger screens we can add a sidebar to the same row as the main content rather than it's own row. This is explained in more detail below in the **Grid Template Areas** section.

- 4 rows
  - header: 300px height
  - navigation: 44px height
  - main content: auto
  - footer: 54px height

# Grid Areas
We assign a grid area to each one of the 5 rows created by our grid using the `grid-area` attribute.

- header
  - `grid-area: hd;`
- nav
  - `grid-area: hnav;`
- main
  - `grid-area: main;`
- aside
  - `grid-area: sd;`
- footer
  - `grid-area: ft;`

# Grid Template Areas
Now that our grid and grid areas have been defined we can use them to create `template areas` that _visually_ define the grid for specific pages. The layout is a literal representation of the 12 columns and 5 rows defined above. 

## Mobile
```
#index {
  grid-template-areas: 
    "hd   hd   hd   hd   hd   hd   hd   hd   hd   hd   hd   hd"
    "hnav hnav hnav hnav hnav hnav hnav hnav hnav hnav hnav hnav"
    "main main main main main main main main main main main main"
    "sd   sd   sd   sd   sd   sd   sd   sd   sd   sd   sd   sd"
    "ft   ft   ft   ft   ft   ft   ft   ft   ft   ft   ft   ft";
}
```

We currently define the template for the following types of pages:
- Index
- Single
- About
- Gallery

## Larger than 1280px
The mobile-first focus of this theme means that the mobile versions are all identical to the `#index` posted above.

Here's an example of how that template differs for larger screens, You can see that the 3rd row is significantly different - we include some blank spaces as well as removing the 4th row completely by splitting the 3rd row between content _and_ sidebar rather than the mobile version which defaults to 1 area per row:

```
  #index {
    grid-template-areas: 
      "hd   hd   hd   hd   hd   hd   hd   hd   hd   hd   hd   hd"
      "hnav hnav hnav hnav hnav hnav hnav hnav hnav hnav hnav hnav "
      ".    .    main main main main main sd   sd   sd   .    ."
      "ft   ft   ft   ft   ft   ft   ft   ft   ft   ft   ft   ft";
  }
```

- The `.` in this case means leave the area blank
- Followed by 5 `columns` of `main`
- Followed by 3 `columns` of `sd`
- Followed by an additional 2 `columns` of empty space
