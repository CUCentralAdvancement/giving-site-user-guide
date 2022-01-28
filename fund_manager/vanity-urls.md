# Vanity URLs

Vanity URLs allow a shorter, more human-readable URL to redirect to another page on the Giving website or another 
service Central Advancement uses.

It is important to remember the two most important parts of using a "hyperlink" on the internet when discussing the 
Venity URL feature:

- **Link text:** This describes the link, i.e. Users click "Fund Me" and are sent to the URL "https://giving.cu.edu/fund-me"
- **Link URL:** The location where users are sent after clicking. You can use the URL for link text, but it is better to
  describe the link semantically for better accessibility.

## Purpose

To better explain the purpose of using a Vanity URL, let's use the most common example: providing users a shorter 
link to send them to a fund or landing page. 

The Vanity URL contains two parts:

- **Source:** The Short URL, e.g. https://giving.cu.edu/fund-me
- **Destination:** The URL where users will be redirected to, e.g. https://giving.cu.edu/fund/a-rather-long-fund-name

Freddie the Fund Manager needs to send donors a communication for an upcoming campaign related to the "A Rather Long 
Name for a Fund". The fund name and URL are non-negotiable, so Freddie requests a Vanity URL via the Digital 
Marketing team's WorkFront account. He thinks the shorter name will look better in the email he sends out and the 
print piece mailed to potential donors.

Users receive communications in an email, click the Vanity URL link and are redirected to the fund's page at a 
longer URL. The https://giving.cu.edu/fund-me text is used for the link text and URL, and Freddie requested a Vanity 
URL since the longer URL didn't fit as nicely into his email template.

Users also receive the link printed on a card, and some of them actually type in the URL to a browser. 
Most mail users; however, do not type in the URL leaving Freddie flummoxed wondering how he can increase conversions 

## Not A Good Purpose

As you can see from the example above, there are a couple of issues with using Vanity URLs in print and on the web.

For his email campaign, Freddie could have used link text to better describe the link to his targeted audience AND 
he could use A/B testing in the process to figure out what phrasing made users more likely to click his links: 
information than can help everyone who are using email marketing at CU.

For his print campaign, not many people followed the link because they didn't feel like typing in a URL in 2022. 
Freddie could have used a QR code to link to the same fund page, increase adoption, and not have to submit a request 
for a Vanity URL.

## When to Use Vanity URLs

As time goes on and people adopt QR code readers, there are fewer and fewer legitimate use cases for Vanity URLs. 
99% of the time using link text in an email/webpage or a QR code for print can suffice and use the system-generated 
URLs on the Giving website.

The documentation will be updated with suggested use cases when they are found.

Suggested Use Cases:
- ...still trying to find one...

## Current Problems

There are several current problems with the Vanity URL implementation.

### Bad Links

When users request Vanity URLs they often have no training on SEO and the web. This results in requests with less 
than ideal URLs, e.g. https://giving.cu.edu/TheFundIWantToSee. It is generally bad practice to:

- use capital letters in the URL
- not separate words with dashes
- use 

The improved URL would be: https://giving.cu.edu/see-this-fund. It doesn't include capital letters, uses dashes to 
delineate words, and drops extraneous words not relevant to semantically describing content at the URL.

### Routing 

Vanity URLs create an SEO and routing problem for the Giving website. Every other route on the Giving site is 
system-generated or something a user puts into a menu. Each section of the website has rules for what can go inside 
that path.

- /fund/{slug} - The fund pages where {slug} is the fund title sluggified.
- /about-us/{page-title} - Pages Advancement staff created and put under the "About Us" menu.

However, Vanity URLs have no rules as to where they are taking you. If someone creates a Vanity URL for 
"/campaigns/the-best-one", and we want to add a "Campaign Feature" that loads webpages at "/campaigns/
{campaign-title}" then it becomes tricky to handle a campaign called "The Best One".

However, if the Vanity URLs existed on a different domain than https://giving.cu.edu, they won't conflict with any 
system-generated pages. If the user instead requested "https://giveto.cu.edu/campaigns/the-best-one", it wouldn't 
conflict with "https://giving.cu.edu/campaigns/the-best-one".

For these reasons, it is recommended to use a separate (sub)domain name for a link shortener service. 

### Outdated 

Outdated, unused Vanity URLs also become a problem, and most of them are only useful for a limited time during a 
targeted campaign time period.

## Current Process

To request a Vanity URL, you should fill out the request form located at:

This requires access to use WorkFront. You can request access here:

You can only request for the Vanity URL to send users to certain services the university controls. Allowing 
requestors to link to anything on the internet is dangerous and detrimental to CU branding efforts. 

Types of donation locations accepted:

- Giving website
- Cvent
- Campus website
- Community Funded
- Marketing Cloud page

## Future State of Vanity URLs

The Vanity URL will consist of four parts:

- **Type:** This is akin to a "tags" field and used to group the URLs into categories. It will likely consist of where 
  the link is redirecting to.
- **Source:** The Short URL, e.g. https://giving.cu.edu/fund-me
- **Destination:** The URL where users will be redirected to, e.g. https://giving.cu.edu/fund/a-rather-long-fund-name
- **Owner:** The email of the requester. This is used for communication about the status of the Vanity URL
- **Expiration:** After this date, the Vanity URL will expire. The owner will be emailed one week before the 
  expiration date with options to continue using the URL.



