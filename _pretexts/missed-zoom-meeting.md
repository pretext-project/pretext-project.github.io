---
layout: pretext

title: Missed Zoom Meeting

short-description: >
  Zoom users receive an email stating they missed a meeting and are provided a link to view the missed meeting information.

long-description: >
  Zoom users receive an offical-looking, automated, HTML-based email from Zoom or their Zoom account administrator stating they missed a meeting. In the email, Zoom provides the victim a link to learn about the meeting they missed. This link goes to a phishing page designed to capture the user's Zoom credentials. 

analysis: >
  Missing a work meeting that you did not know about is likely to cause stress and will prompt you to immediately look into what you missed. You don't want to give your boss a reason to get upset with you!

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
      description: Fake Zoom login page designed to capture user credentials.

sample-emails:
  - email:
    image: "missed-zoom-meeting-email1.png"
    source: https://www.proofpoint.com/us/threat-insight/post/remote-video-conferencing-themes-credential-theft-and-malware-threats
    
tags:
  - missing out
  - missed meeting
  - teleconference
  - zoom
  - intrigue
  - guilt
 
date: August 28, 2020

contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr

resources:
  - https://www.proofpoint.com/us/threat-insight/post/remote-video-conferencing-themes-credential-theft-and-malware-threats
---