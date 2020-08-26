---
layout: pretext
title: Link Disguised as Attachment
short-description: >
  An email references an attachment; however, the "attachment" is really just CSS hiding a link to a malicious site.
long-description: >
  This one is less pretext and more of a specific tactic, but it deserves its entry. The idea is the attacker emails the target and includes an "attachment" in the email. The email references the attachment in a way that entices the user to double-click the "attachment" to view it. The email is HTML-based and the "attachment" is actually just cleverly coded CSS obfuscating a link. When the victim double-clicks the "attachment", it opens up a web page, which could be used in a drive-by-download, thus avoiding your real attachment triggering any AV scanners in email delivery. The actual email could be about any topic, but should entice the victim to click on the "attachment". A few examples are: signed contracts, invoices, photos, etc.
analysis: >
  Placing a malicious file in a victim's inbox can be extremely difficult with modern AV scanners. This tactic presents an opportunity for attackers to trick victim's into downloading a file onto their computer, without having to worry about secure email gateways catching it.
goals:
  - malware
methods:
  - email
payloads:
  - drive-by-download
sample-payloads:
  - payload:
      type: drive-by-download
      description: User double clicks the fake "attachment", which opens up a browser and auto-downloads some malware. 
sample-emails:
  - email:
    image: "link-disguised-as-attachment-email1.png"
    source: https://twitter.com/troyhunt/status/1296215917932630016
tags:
  - fake attachment
  - attachment
  - pdf
  - css
  - html
  - html email
date: August 26, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
resources:
  - https://twitter.com/troyhunt/status/1296215917932630016
---


