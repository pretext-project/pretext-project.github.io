---
layout: pretext
title: Citrix ShareFile
short-description: >
  The target's corporate Citrix ShareFile service emails them a link to a malicious file.
long-description: >
  Lots of corporations use file shares, such as Citrix ShareFile. In this pretext, an attacker spoofs an email from the target company's Citrix ShareFile service to an employee. The email is sent from a generic role-based email address, like "docs@company.com". In the email, the attacker shares a link to an enticing file, such as "Sales Memorandum" or "Salary Renegotiation Process". The email could identify a colleague that shared the file with them or exclude that information. When the victim clicks on the link, it takes them to a phishing site where the attacker could harvest credentials or conduct a drive-by-download attack. Alternatively, it could be a direct download of an office file containing macros. We recommend sending an HTML-based email that looks very similar to an official Citrix ShareFile email. Please see the resources at the end of the page for email design.
analysis: >
  When you receive an email with a file that you plausibly could expect or a file that seems to contain juicy information, an employee might click on the link to view the file without conducting sufficient due diligence.
goals:
  - malware
  - cred harvest
methods:
  - email
payloads:
  - drive-by-download
  - phishing page
  - doc
  - docx
  - xls
  - xlsx
  - ppt
  - pptx
sample-payloads:
  - payload:
      type: phishing page
      description: Fake Citrix ShareFile login portal or fake VPN login portal asking target for their credentials. If used with a tool like Evilgnx2, you could also circumvent multi-factor authentication and hijack their session.
  - payload:
      type: drive-by-download
      description: User tries to visit the juicy or interesting link and instead hits a page that either displays a fake file, or if you want to invest less time, you could send them to a page that says "this file no longer exists", or "you are not authorized to view this file". From there, a drive-by-download attack occurs.
  - payload:
      type: xls
      description: Fake file with XLM (Excel 4.0) macros.
sample-emails:
  - email:
    from: Documents <TARGET DOMAIN NAME>
    subject: "You have an encrypted message"
    body: | 

      Download

      Trouble with the above link? You can copy and paste the following URL into your web browser: <PHISHING PAGE LINK>

      ShareFile is a tool for sending, receiving, and organizing your business files online. It can be used as a password-protected area for sharing information with clients and partners, and it's an easy way to send files that are too large to e-mail.

      Powered by Citrix ShareFile 2020.
  - email:
    image: "citrix-share-file-email1.png"
    source: https://twitter.com/joeleonjr
  - email:
    image: "citrix-share-file-email2.png"
    source: https://support.citrix.com/article/CTX208306
tags:
  - intrigue
  - gossip
  - Citrix
  - File share
  - ShareFile
  - link
date: August 23, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
resources:
  - https://support.citrix.com/article/CTX208306
---


