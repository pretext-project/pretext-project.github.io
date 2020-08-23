---
layout: pretext
title: Intern Meeting with CEO
short-description: >
  As part of an internship, the CEO will speak with each intern for 30 minutes. Interns need to sign up for a time to meet with the CEO.
long-description: >
  The CEO's office reaches out to an intern offering them a 30 minute conversation with the CEO as part of their internship. To set up the meeting, interns need to fill out a form with the questions they want to ask the CEO as well as pick a time that works with the CEO's schedule. The online form and/or calendar application could be a cred harvesting or malware attack. Be careful not to lead the interns on too long, since preparing for an actual meeting with the CEO would likely cause them great stress and take up a ton of their time. The best payloads would be one that doesn't not actually schedule a meeting with the CEO, but rather just says something like "Oh, sorry. {CEO} is no longer available to meet then."
analysis: >
  This is a classic authority/power play. Any legitimate-seeming communication coming from the CEO's office, especially one that involves them interacting with the CEO, will likely quickly grab an intern's attention and interest. Since it's the CEO's office, the intern will be unlikely to question the legitimacy of the communication. Also, consider that while interns might make an easy target, their access will probably not be that great.
goals:
  - malware
  - cred harvest
methods:
  - email
  - phone
payloads:
  - drive-by-download
  - phishing page
  - hta
  - doc
  - docx
sample-payloads:
  - payload:
      type: phishing page
      description: Figure out what VPN or email software the company uses. Clone the login portal and direct interns to that page prior to "selecting a time to meet with the CEO".
  - payload:
      type: hta
      description: Create an HTA application that allows an intern to schedule a time to meet with the CEO. To reduce suspicion, the application should actually work. But since we don't want to ruin the intern's day by having them prepare for a meeting that will not occur, we should make all selections return "Sorry. This person is no long available during that time slot."
sample-emails:
  - email:
    from: Documents <TARGET DOMAIN NAME>
    subject: "Intern Meeting with CEO"
    body: | 
      Hi {FIRST NAME} - This is {CEO ASST NAME} from {CEO'S NAME} office. Each year we always try our best to schedule time on {CEO's NAME} calendar to meet with our interns. We don't have time to meet with everyone, but {CEO} would like to meet with you. Attached, you'll find a calendar scheduling application. Please double-click it and follow the instructions to set up a call. Please don't share this application with any other interns, since not everyone will receive the same invitation.

      {CEO} looks forward to meeting with you.

      Thank you,
      {CEO ASST NAME}
sample-phone-calls:
  - script:
    - message:
      - from: victim
      - content: Hello?
    - message:
      - from: attacker 
      - content: Hi, {INTERN}, this is {CEO's ASSISTANT}. I'm {CEO's NAME} assistant. How are you?
    - message:
      - from: victim
      - content: I'm good. Thank you. How can I help you?
    - message:
      - from: attacker
      - content: Good. Each year we always try our best to schedule time on {CEO's NAME} calendar to meet with our interns. We don't have time to meet with everyone, but {CEO} would like to meet with you. Is that of interest?
    - message:
      - from: victim
      - content: Yes. Of course.
    - message:
      - from: attacker
      - content: Great. I'm going to give you a URL to navigate to, to schedule a meeting on his/her calendar. Are you ready? That URL is....{PHISHING URL}. Please follow the instructions on that page and schedule time with {CEO's NAME}. Also, just so you know, not every intern will be offered this opportunity, so please don't share this with everyone. If you have any questions, please let me know.
tags:
  - authority
  - importance
  - CEO
  - intern
  - internship
  - calendar app
  - meeting
  - schedule meeting
date: August 23, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
resources:
---


