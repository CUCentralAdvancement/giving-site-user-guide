---
layout: default
title: Fund Pages
parent: Content Editors
nav_order: 1
---


# Fund Pages

Funds are requested by campus partners via Workfront request forms. You can read about that process 
and considerations in [the Web Requester documentation on funds](web_requester/fund-pages.md).

For this documentation, we will only go over the process of adding/editing a fund on the Giving site 
once a WF request comes in to add the fund to the site.

## Adding a Fund

1. [Go to WorkFront](https://universityofcolorado.my.workfront.com/requests/content-dashboard__5cc1f24e003cc55938884ff5fdbf4220), 
  view the submission, and copy the allocation code.
2. Search for allocation code in [All Funds Lookup](https://giving.cu.edu/all-funds-lookup?status=All&field_fund_active_value=All&field_fund_allocation_code_value=&combine=)
     1. If found, then make sure the fund is active, and respond to requester that the fund is already on the site 
        with the fund's URL.
     2. If not found, proceed.
4. Download the CSV file from https://giving.cu.edu/admin/config/services/fund-sync
5. Check for the allocation code in the CSV output `cmd + f`.
   1. If no code found, tell the requester the fund is not in Advance...should also send them some email address or 
      link to contact. Resume step one once the requester confirms the fund is in Advance.
   1. If code found, proceed.
6. Copy information into a new fund: https://giving.cu.edu/node/add/donation and follow [fund field instructions](#fund-fields).

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
