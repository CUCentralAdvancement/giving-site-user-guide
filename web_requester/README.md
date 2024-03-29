---
layout: default
title: Web Requesters
nav_order: 2
has_children: true
permalink: /web-requesters
---

# Web Requester User Role

Web Requesters control all aspects of how funds are marketed on the website including creating Landing Pages,
Vanity URLs, and Fund Page marketing content. 

## Login

After you log into the website, you will be taken to the content area...need to check if this is true.

Types of content:
- [Landing Pages](landing-pages.md) - Landing Pages allow
- [Fund Pages](fund-pages.md) - Funds users can donate to. You can also set the suggested amount and recurring 
  options when a user visits the page.
- [Vanity URLs](vanity-urls.md) - Vanity URLs allow a shorter, more human-readable URL to redirect to another page 
  on the Giving website or another service Central Advancement uses. 

Other Features:
- [Appeal Codes](#appeal-codes)

## Video Embeds

1. Follow instructions to get an embed code in an `<iframe></iframe>` HTML tag.
2. Click "Source" on the WYSIWYG editor
3. Paste the `<iframe>` in between HTML tags with CSS styling classes.

```html
<div class="video-wrapper">
    <div class="video-wrapper-div">
        <!--insert iframe code here-->
    </div>
</div>
```

## Appeal Codes

You can track a user via something called an appeal code...

notes on feature: https://github.com/CUCentralAdvancement/giving-frontend/issues/571
