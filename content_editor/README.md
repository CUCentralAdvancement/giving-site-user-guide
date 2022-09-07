---
layout: default
title: Content Editors
nav_order: 3
has_children: true
permalink: /content-editors
---

# Content Editor User Role

Content editors control all the content for their advancement group whether they are under the CU Foundation, 
Central Advancement, or other university departments.

- [FAQs](faqs.md) - Frequently asked questions about the Giving site.
- [Fund Pages](fund-pages.md) - How to add and edit fund pages.
- [Vanity URLs](vanity-urls.md) - How to add and edit vanity URLs.

## Content Owners

Each piece of content on the Giving website is supposed to be owned by some group at CU. We've broken 
things down into the four campuses, Central Advancement, and the CU Foundation. Some content types 
have a "Content Owners" field on it, and the Funds are denoted ownership by the affilated campus.

Content that has Content Owners:
- Funds - The campus field denotes ownership.
- Custom Fund Landing Pages - The "Content Owners" field denotes ownership.
- Vanity URLs - The "Content Owners" field denotes ownership.
- FAQs - The "Content Owners" field denotes ownership.
- Static Pages - The "Content Owners" field denotes ownership.

Content that does not use the Content Owners field:
- CUF Staff - No "Content Owners" field, but the CU Foundation is the owner.
- Essential Idea - Old content that Central Advancement owns.
- Front Page - This is the homepage of the site and owned by Central Advancement.
- License Plate Fund - This is a dumb content type, but Boulder, Anshutz, and Denver have license plate 
  funds.
- Story - Old content that Central Advancement owns.
- Webform - There are a few forms about payroll deduction that the CU Foundation mainly owns. One 
  form allows users to update their contact information.

## Content Owner Taxonomy

Drupal has many taxonomies useful for classifying content. We have made a "Content Owners" taxonomy 
that is used to add ownership to content on the Giving site.

The Content Owners taxonomy can also be used for communicating with the owner groups about content 
decisions. For example, the CU Foundation can be notified when content they own appears to be 
outdated or full of broken links, and that process can be automated. However, to make that feature 
work, developer hours and code changes are needed.

For now, you can add users and emails to Content Owner groups:
1. Go to https://giving.cu.edu/admin/structure/taxonomy/content_owners
2. Click "Edit" on the owner group you wish to edit.
3. Add or remove emails and users as staff changes are made.
