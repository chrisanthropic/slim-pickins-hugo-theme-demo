---
title: "Contact Page"
date: 2018-03-08T03:59:04-08:00
categories: ["docs"]
toc: true
categorylist: true
---
This theme includes a custom contact page and requires a free [Netlify](https://app.netlify.com/) account to function properly.

# Contact Form
## Requirements
A Netlify Account and a website deployed from your Netlify account. The contact form **requires** [Netlify](https://app.netlify.com/) to work. The free tier works perfectly fine for this (it's what this Demo site uses).


## Creating a Contact Form
- Create a new page `content/contact.md` with the following front-matter:

```
---
Title: Contact
type: contact
---
```

- Add any content to page itself.

## Add it to the Navigation Menu
- Optionally, you can add the page to the [navigation menu](/blog/navigation/) by adding the following to the front-matter:

```
menu:
  main:
    identifier: "contact"
    name: "contact"
    weight: 5
```

## Verifying Netlify
Submit a test to your contact page and then log in to your Netlify account and navigate to Forms. You should see an active form listed as `contact` with 1 submission that you just sent. 

## Adding Email Notifications
If you want it to forward the contact form message to your email address, you can do that!

- From the Forms page
- Click on the `notifications` button in the _Form Handling_ section.
- Click on the `Add notification` drop-down in the _Outgoing notifications_ section.
- Select `Email notification`
- Enter your email address in the `Email to notify` section

And that's it. Now anytime someone submits to your contact form it'll get forwarded to your email address for free.
