---
layout: pretext
title: LinkedIn Invitation Waiting
short-description: >
  Reminder email from LinkedIn stating that someone sent the target an invitation to connect 7 days ago and they never accepted.
long-description: >
  When you invite a user to connect with you on LinkedIn, an email immediately sends to the user requesting they accept your invitation. If that user does not "ignore" or "accept" your invitation within 7 days, LinkedIn sends a reminder email to the user. You'll need to choose a user that is trying to connect with the target. You could select someone at random or someone famous in the industry that they might not know. Either way, review their LinkedIn profile page to ensure they're not already connected to them. When you're crafting the email, just copy/paste the html from an existing invitation reminder to your own personal LinkedIn account. Also, consider which email(s) a user has connected to LinkedIn. For example, I am positive I do not have my work email connected to LinkedIn, so if I receive a message to that email, I'll know it's spam. Conversely, if you send it to the email I use for LinkedIn, I'll be much less suspcious. Finally, every link in the email should point to a phishing page to capture user credentials for LinkedIn.
analysis: >
  This is a good opportunity to phish someone for two reasons. First, targets are unlikely to remember every person who tried to connect with them 7 days ago, either due to the time that passed or volume of invitations. As a result, when the reminder email comes in, they'll likely take it to be geniune, or at least not suspicious. Second, the email literally says "{USER}'s invitation is waiting your response" and "{USER} invited you to connect 7 days ago." LinkedIn uses this language on purpose to guilt trip users into taking an action on outstanding invitations. We can benefit from the hours of UX testing LinkedIn has done on their email copy and use their exact email to conduct a credential harvesting campaign.
goals:
  - cred harvest
methods:
  - email
payloads:
  - drive-by-download
  - phishing page
sample-payloads:
  - payload:
      type: phishing page
      description: Use a tool like Evilgnx2 to circumvent multi-factor authentication and hijack the user's LinkedIn session.
sample-emails:
  - email:
    image: "linkedin-invitation-waiting-email1.png"
    source: https://twitter.com/joeleonjr
tags:
  - linkedin
  - professional
  - networking
  - social media
  - invitation
  - connection
  - network
  - evilgnx2
date: August 25, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
---


