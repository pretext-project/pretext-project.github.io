---
layout: pretext
title: Conference Speaker
short-description: >
  A new industry conference is looking for speakers/panelists about a topic related to the target's job/expertise.
long-description: >
  The attacker creates an entire fake industry conference centered around the target's area of expertise or job title. The attacker then contacts the target, via email or phone, and invites them to participate on a panel or as a speaker. You'll need to conduct sufficient research on the individual to ensure that they would feel qualified enough to speak to a particular topic, so make sure they have sufficient professional experience in that field. It needs to be plausible that they'd be asked to speak, or at least that someone might think they could. This pretext relies heavily on playing to our victim's ego, so be sure to string in little sayings like 'your insight', 'you came highly recommended', 'top of the field', etc. Create a conference website and then the payload could be via document about the conference sent over email or website-based.
analysis: >
  This pretext plays to the target's ego. The best target is probably someone with a lot of career aspirations that hasn't been recognized yet. 
goals:
  - malware
methods:
  - email
  - phone
payloads:
  - drive-by-download
  - phishing page
  - doc
  - docx
  - pdf
  - hta
sample-payloads:
  - payload:
      type: hta
      description: Fake calendar scheduling HTA to schedule time with the victim to discuss the panel you want them to participate on.
  - payload:
      type: drive-by-download
      description: User tries to visit the conference website. This requires building a legitimate looking conference website. Shouldn't be too difficult though, since there are tons of templates out there.
  - payload:
      type: pdf
      description: A malicious PDF file with the fake panel information.
sample-emails:
  - email:
    from: "{FAKE CONFERENCE NAME} Conference"
    subject: "panelist for new {INDUSTRY} conference"
    body: | 
      Hi {FIRST NAME} -

      The new {CONFERENCE NAME} conference seeks to bring together industry experts and academics to {CONFERENCE PURPOSE}. 

      We're in the process of putting together conference panels and thought the panel on {TOPIC RELATED TO VICTIM} might be of interest. Are you open to discussing being a panelist at our conference?

      Please let us know as soon as possible.
      \-Conference Organizers
    attachments:
      - panel.pdf
tags:
  - intrigue
  - ego
  - conference
  - speaker
  - panelist
  - speech
date: August 26, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
resources:
  - https://www.wix.com/website/templates/html/events/conferences-meetups
---


