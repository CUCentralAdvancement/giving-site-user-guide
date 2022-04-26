# Vanity URLs

A Vanity URL (VURL) allows a shorter, more human-readable URL to redirect to another page on the Giving website or
another service Central Advancement uses. Instead of site visitors having to type in a longer URL, they can type in 
a more meaningful sequence of characters resulting in a better user experience.

To create and use a Vanity URL, it is important to remember the two most important parts of using a "hyperlink" on the
internet.

- **Link text:** This describes the link, i.e. Users click "Fund Me" and are sent to the
  URL "https://giving.cu.edu/fund-me"
- **Link URL:** The location where users are sent after clicking. You can use the URL for link text, but it is better to
  describe the link semantically for better accessibility.

## Purpose

To better explain the purpose of using a Vanity URL, let's use the most common requester example: providing users a 
shorter link
to send them to a fund or landing page.

The Vanity URL contains two parts:

- **Source:** The Short URL, e.g. https://giving.cu.edu/fund-me
- **Destination:** The URL where users will be redirected to, e.g. https://giving.cu.edu/fund/a-rather-long-fund-name

Winona the Web Requester needs to send donors a communication for an upcoming campaign related to the "A Rather
Long Name for a Fund" fund. The fund name and system generated URL are non-negotiable, so Winona requests a Vanity URL
via the Digital Marketing team's WorkFront account. She thinks the shorter name will look better in the email she sends
out and the print piece mailed to potential donors.

Users receive communications in an email, click the Vanity URL link and are redirected to the fund's page at a longer
URL. The https://giving.cu.edu/fund-me text is used for the link text and URL, and Winona requested a Vanity URL since
the longer URL didn't fit as nicely into her email template.

Users also receive the link printed on a card, and some of them actually type in the URL to a browser. Most mail users;
however, do not type in the URL leaving Winona flummoxed wondering how she can increase her conversions.

## Not A Good Purpose

As you can see from the example above, there are a couple of issues with using Vanity URLs in print and on the web.

For her email campaign, Winona could have used link text to better describe the link to her targeted audience, and she
could use A/B testing in the process to figure out what phrasing made users more likely to click her links:
information than helps everyone to perform email marketing at CU.

For example, Winona decides to resend the email to people who didn't open the original send, but she splits the targeted
emails between users seeing different link text. One group is asked
to ["Join the team and donate now"](https://giving.cu.edu), and the other group is asked
to ["Donate Now"](https://giving.cu.edu). Based on the click tracking results, Winona will keep exploring link text
choices and expand her segmentation to whole content blocks eventually.

For her print campaign, not many people followed the link because they didn't feel like typing in a URL when they are
more used to scanning QR codes. Winona could have used a QR code to link to the same fund page, increase adoption, and
not have to submit a request for a Vanity URL.

For example, for an upcoming event Winona decides to generate a QR code and distribute it to event organizers to print
on various materials. Throughout the course of the event, guests are presented with the QR code alongside marketing
content and Winona sees more traffic to his fund's donation page compared with the times she's printed out short URLs
and pasted them on marketing materials.

## When to Use Vanity URLs

As time goes on and people adopt QR code readers, there are fewer and fewer legitimate use cases for Vanity URLs. 99% of
the time using link text in an email/webpage or a QR code for print can suffice, and you can still use the 
system-generated URLs created by the Giving website hidden behind the QR code or link text.

However, sometimes a service won't allow users to create link text for links, and that is a case when Vanity URLs can be
useful. For example, you want to paste a URL into a social media post and the service shows the whole URL for link text.
If using a Vanity URL improves readability and UX of the posting, then it is a good place to request a Vanity URL.

Current Valid Uses:

1. **Crowdfunding/CommunityFunded URLs**. The CommunityFunded application does not allow for short URLs to be made, 
   so it is okay to request a VURL for crowdfunding campaigns.
2. **Social media**. Oftentimes, long links break the character limits and shorter URLs are needed to post a link in
   content.
3. **Events and word-of-mouth**. Sometimes, people need to speak the URL to an audience and having people remember long
   strings of characters does not work well. In these cases, it is much better to use a VURL someone can speak to at
   an event.

If you'd like to discuss usage of Vanity URLs and how you can improve your use of them, please email `giving@cu.edu`
with "Vanity URL Help Request" in the subject line.

## Current Problems

There are several current problems with the Vanity URL implementation we are working to improve upon.

### Bad Links

When users request Vanity URLs they often have no training on SEO and the web. This results in requests with less than
ideal URLs, e.g. https://giving.cu.edu/TheFundIWantToSee. It is generally bad practice to:

- use capital letters in the URL
- not separate words with dashes
- include filler words that don't add to the link's meaning

In the example above, the improved URL would be: https://giving.cu.edu/see-this-fund. It doesn't include capital
letters, uses dashes to delineate words, and drops extraneous words not relevant to semantically describing content at
the URL.

### Routing Collisions

Vanity URLs create a SEO and routing problem for the Giving website. Every other route on the Giving site is
system-generated or something a user puts into a menu. Each section of the website has rules for what can go inside that
path.

- /fund/{slug} - The fund pages where {slug} is the fund title sluggified.
- /about-us/{page-title} - Pages Advancement staff created and put under the "About Us" menu.

However, Vanity URLs have no rules as to where they are taking you. If someone creates a Vanity URL for
"/campaigns/the-best-one", and we want to add a "Campaign Feature" that loads webpages at "/campaigns/ {campaign-title}"
then it becomes tricky to handle a campaign called "The Best One".

However, if the Vanity URLs existed on a different domain than https://giving.cu.edu, they won't conflict with any
system-generated pages. If the user instead requested "https://giveto.cu.edu/campaigns/the-best-one", it wouldn't
conflict with "https://giving.cu.edu/campaigns/the-best-one".

For these reasons, it is recommended to use a separate (sub)domain name for a link shortener service.

### Outdated Links

Outdated, unused Vanity URLs also become a problem, and most of them are only useful for a limited time during a
targeted campaign time period. When the campaign ends, no one requests to remove the Vanity URL and many old, unused
links remain on the Giving site polluting the routing system.

We are currently working on adding an expiration date to all VURLs, but there is no timeline for releasing that update.

## Current Process

To request a Vanity URL, you
should [fill out the request form.](https://universityofcolorado.my.workfront.com/requests?activeTab=tab-new-helpRequest&projectID=5e78b9c9013651dd0db330e625ca787c&path=5e78be160139141988101a91b47abd33,5e7985890198d19da824828650710e5c)

This requires access to use WorkFront. You can request access here: https://giving.cu.edu/workfrontnewuser

To preserve the integrity of ".cu.edu" domains, we are working on a policy that will only allow redirects to a service
the university controls. Allowing requesters to link to anything on the internet is dangerous and detrimental to CU
branding efforts.

Proposed types of donation locations accepted:

- Giving website
- Cvent
- Campus website
- Community Funded
- Marketing Cloud page

## Future State of Vanity URLs

We are working to improve the Vanity URL feature on the Giving website. The proposed future Vanity URL will consist of
four parts:

- **Type:** This is akin to a "tags" field and used to group the URLs into categories. It will likely consist of where
  the link is redirecting to.
- **Source:** The Short URL, e.g. https://giving.cu.edu/fund-me
- **Destination:** The URL where users will be redirected to, e.g. https://giving.cu.edu/fund/a-rather-long-fund-name
- **Owner:** The email of the requester. This is used for communication about the status of the Vanity URL.
- **Expiration:** After this date, the Vanity URL will expire. The owner will be emailed one week before the expiration
  date with options to continue using the URL.
