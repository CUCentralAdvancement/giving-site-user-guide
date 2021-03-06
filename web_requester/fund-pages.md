---
layout: default
title: Fund Pages
parent: Web Requesters
nav_order: 1
---

# Fund Pages

## Adding a Fund

1. [Go to WorkFront](https://universityofcolorado.my.workfront.com/requests/content-dashboard__5cc1f24e003cc55938884ff5fdbf4220), 
  view the submission, and copy the allocation code.
2. Go to https://giving.cu.edu/node/add/donation, fill in the "Allocation Code" field, and use the "Check Allocation Code is valid" 
  button to see if you can add the fund.
    1. If you get an error message then follow the prompts and report it back in the Workfront issue.
4. If no errors, copy request information into a new fund following [fund field instructions](#fund-fields).
5. If requester asks to "hide the fund" or any other special instructions, look through the [special snowflakes](#special-snowflakes) section.

## Removing a Fund

To remove a fund:

1. Go to the WorkFront submission.
2. Check and see that the user got permission from the appropriate staff members.
3. Go to the link in "Current URL on giving.cu.edu" in the Issue Details.
4. Click "Edit" once logged in.
5. Scroll down to the "Active" checkbox and uncheck it.
6. Ignore the redirect URL field. Once deactivated, users will be redirected to the fund search page with the campus 
   and interest of the deactivated fund selected.
7. Reply to the Workfront issue and let them know users will be redirected.

## Fund Fields

There are several historical fields on the fund node that served a purpose at one point but are no longer relevant 
to fill in. We will ignore those fields in this document, and who knows, they might disappear by the next time you 
read this.

- **Title** - The "Fund Title" from the Fund Details section.
- **Fund Owners** - The email(s) of the staff member who made the submission.
- **Description** - The "Official Fund Description" from the Fund Details section. 
- **Marketing Content** (Optional) - The "Additional marketing content for fund page" from the Optional Additional 
  Fund Page Content section. 
- **Marketing Content Expiration** (Optional) - The "Schedule additional content?" from the Optional Additional Fund 
  Page Content section.
- **Allocation Code** - The "Allocation Code" from the Fund Details section. It always must start with a zero.
- **Active** - This should be checked to make the fund available to the public.

### Allocation Code Breakdown

The allocation codes can be broken down into a pattern that tells the campus and endowment status of each fund.

<img width="651" alt="Screen Shot 2022-06-11 at 3 01 49 PM" src="https://user-images.githubusercontent.com/3640707/173201519-7104e8e4-69b6-4488-8462-9a615f263f09.png">

### Product Catalog Section

These fields are at the bottom of the screen in a tabbed interface.

- **Campus** - The "Campus or Organization" from the Fund Details section.
- **Keywords** (Optional) - Do not add unless requested.
- **Additional Keywords** (Optional) - Do not add unless requested.
- **Interest** (Optional) - The "Interest Category" from the Fund Details section. 
- **Fund Type** (Optional) - If "Is this an endowed fund?" is "Yes" in the Fund Details section, then select 
  "Endowed Funds".

Now you can save the form. After saving, the form, you should see the fund page as a site visitor will see it.

### Vanity URL

If the submission requests a Vanity URL, then you should:

1. Click "Edit" to go back to the fund page's edit form.
2. Scroll to the bottom of the page and the tabbed interface.
3. Select the "URL redirects" tab.
4. Click "Add URL redirect".
5. Enter the Vanity URL path in the "From" field on the next screen.
6. Save to add the redirect.
7. Check the Vanity URL to see it redirects to the fund page.

You can read more about Vanity URLs in [the main Vanity URL documentation section](vanity-urls.md).

## Special Snowflakes

Sometimes, the requester will ask for additional things than just adding a fund. 

- **Hide a fund** - If they ask to hide a fund from the fund search add an "Additional Keyword" of "HIDE" from the autocomplete field. This will exclude the fund from the fund search. You can always check the fund search to make sure that the fund you added does not show up.
