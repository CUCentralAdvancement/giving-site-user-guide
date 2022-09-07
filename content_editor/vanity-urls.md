---
layout: default
title: Vanity URLs
parent: Content Editors
nav_order: 2
---

# Vanity URLs

You can read all about the purpose of Vanity URLs in the web requester documentation at 
[web_requester/vanity-urls.md](/web_requester/vanity-urls.md).

For this documentation, we will only go over how to add, edit, and remove a VURL from the Giving site.

## Workfront Form

Users have a form that they can use to request a Vanity URL. The form is located at:
https://universityofcolorado.my.workfront.com/requests?activeTab=tab-new-helpRequest&projectID=5e78b9c9013651dd0db330e625ca787c&path=5e78be160139141988101a91b47abd33,5e7985890198d19da824828650710e5c

## Drupal Vanity URL Content Type

Once you get a request to add a VURL, you can enter it on the Giving site by using the Vanity URL 
content type. VURLs are just hyped up Redirects with a few extra fields to denote ownership.

### Adding/Editing a VURL

1. Go to https://giving.cu.edu/node/add/vanity-url.
2. Think of a good descriptive name for the VURL. This will be the title of the VURL.
3. For the Description field, add a link to the WF request and any notes. For example, you might make 
   a note that the VURL should expire at a certain time or relates to another VURL.
4. Enter the "Vanity URL" from WF into the "Vanity URL Path" field. Make sure to only include the 
   path and not the domain, e.g. for "https://giving.cu.edu/this-is-a-vurl", you would only enter 
   "/this-is-a-vurl" for the path.
5. Enter the "Web Fund URL" from WF into the "Vanity URL Destination" field. If it is an internal 
   link, you will only use a path, but if it is an external link, then you will use the full URL 
   provided.
6. Select if the VURL is internal or external. Internal means any link still pointing to the giving.
   cu.edu domain. External means any link pointing to a different domain.
7. Leave the expiration field as-is. VURLs are not being expired at this time.
8. Assign "Content Owners" field to the requester's campus affiliation. If for more than one campus 
   or unknown, then select "Central Advancement".

Once you create a VURL, you cannot edit the Vanity URL Path so you need to delete the VURL to correct 
any mistakes entering that field.

### VURL Stats

The last two fields for access count and last accessed are automatically updated by code and can be 
pulled in for reporting purposes. They mimic the same data stored on regular redirects.

To note, the values displayed are cached somewhat, so you won't see the most up-to-date values unless 
you clear the site's cache.
