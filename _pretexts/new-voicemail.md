---
layout: pretext

title: New Voicemail

short-description: >
  Phone service sends an email stating the user has a new voicemail.

long-description: >
  Services like Google Voice email their users when they receive a new voicemail. Often, the email contains a transcribed preview of the voicemail as well as a link to listen to it. In this pretext, send an email that states the target missed a phone call and include a link to the audio file. Consider adding a transcribed preview of the voicemail with something intriguing and relevant to the target. Attackers could attempt to further personalize the email by identifying which VoIP provider the company uses and copying the legitimate email design that service sends to users. There's a few ways to do this, including checking job postings for IT or support staff, or by calling an actual employee's voicemail and attempting to login. Often times when you login to a voicemail system, it will say what brand VoIP the company uses. The payload could be varied, but generally include phishing pages for credential harvesting or drive-by-download attacks.

analysis: >
  Attackers take advantage of natural human curiosity in this pretext. While we all hate scam calls from unknown numbers, if you get a call from an unknown number and the voicemail seems intriguing, you might want to listen to it.
  
goals: 
  - malware
  - cred harvest
  
methods:
  - email

payloads:
  - click-once
  - phishing page
  - hta
  - drive-by-download

sample-payloads:
  - payload:
      type: drive-by-download
      description: User heads to the page to listen to their new voicemail and gets hit by malware via a drive-by-download.
  - payload:
      type: phishing page
      description: User is required to sign into their gmail or O365 account prior to listening to the voicemail.

sample-emails:
  - email:
    image: "new-voicemail-email1.png"
    source: https://www.mcafee.com/blogs/other-blogs/mcafee-labs/office-365-users-targeted-by-voicemail-scam-pages/
  - email:
    image: "new-voicemail-email2.png"
    source: https://www.greathorn.com/blog-phishing-emails-explained-new-voicemail-message-attack-vector/
    
tags:
  - intrigue
  - surprise
  - voicemail
  - message

date: August 27, 2020

contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr

resources:
  - https://www.greathorn.com/blog-phishing-emails-explained-new-voicemail-message-attack-vector/
  - https://www.mcafee.com/blogs/other-blogs/mcafee-labs/office-365-users-targeted-by-voicemail-scam-pages/
  - https://www.mailguard.com.au/blog/warning-new-voicemail-email-alert-delivers-phishing-attack
---
