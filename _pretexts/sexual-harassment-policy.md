---
layout: pretext
title: Sexual Harassment Policy Update
short-description: >
  The Human Resources (HR) department contacts an employee requesting they 
  review and acknowledge the new corporate sexual harassment policy.
long-description: >
  Since the #MeToo movement, many corporations have updated their sexual harassment policies 
  to reduce legal risk from an employee harassment allegation. Corporate policies often 
  require employees to acknowledge their receipt and understanding of the policy. 
  The social engineer either delivers malware in the form of the "policy" or 
  sends the victim to a phishing page in order to "sign" for the new policy.
analysis: >
  By sending an urgent task related to sexual harassment, the idea is most folks will feel fully obliged to review it ASAP. Given the nature of the topic, many will not feel comfortable questioning any aspect about it. 
goals:
  - malware
  - cred harvest
methods:
  - email
payloads:
  - pdf
  - doc
  - docx
  - click-once
  - phishing page
  - hta
sample-payloads:
  - payload:
      type: doc
      description: Word document containing the new policy. Require employees to enable macros in order to "sign" for it. Could dress up the document to look rather legit + include instructions for enabling macros to "sign".
  - payload:
      type: hta
      description: HTA application that shows the employee the policy and then has a page asking them to sign.
  - payload:
      type: click-once
      description: Similar to the HTA idea. Employee must run the click once application in order to view and then sign the policy.
sample-emails:
  - email:
    from: Corporate HR
    subject: "Action Required: new sexual harassment policy"
    body: | 
      Dear colleagues,

      Due to the recent #MeToo movement, our firm has decided to update our sexual harassment policy. All employees are required to abide by these new regulations. To ensure everyone has read them, we require that you download the following policy and electronically sign acknowledging receipt. If you have any questions, please contact the HR department.

      Thank you,
      HR
    attachments:
      - attachment.xls
    source: https://thissource.com
  - email:
    from: Corporate HR
    subject: "Action Required: new sexual harassment policy"
    body: | 
      Dear colleagues,

      Due to the recent #MeToo movement, our firm has decided to update our sexual harassment policy. All employees are required to abide by these new regulations. To ensure everyone has read them, we require that you download the following policy and electronically sign acknowledging receipt. If you have any questions, please contact the HR department.

      Thank you,
      HR
    attachments:
      - attachment.xls
    source: https://thissource.com
sample-usb-drops:
  - This is an example USB drop description. In here, you'd put all the details  about how you'd conduct the USB drop - where, what's on the drive, etc. 
  - This is an example USB drop description. In here, you'd put all the details  about how you'd conduct the USB drop - where, what's on the drive, etc. 
sample-text-messages:
  - script:
    - message:
      - from: victim
      - content: Hello, this is John Smith. How may I help you?
    - message:
      - from: victim
      - content: Hello, this is John Smith. How may I help you?
    - message:
      - from: attacker
      - content: Hi, John. This is Dr. Steven Richardson. I'm calling to follow-up on my  patient James Reynolds. Hi, John. This is Dr. Steven Richardson. I'm calling to follow-up on my  patient James Reynolds. 
    - message:
      - from: victim
      - content: I'm sorry. There is no one here by that name. 
    - message:
      - from: attacker
      - content: Oh. Interesting. 
sample-chatbot-messages:
  - script:
    - message:
      - from: victim
      - content: Hello, this is John Smith. How may I help you?
    - message:
      - from: victim
      - content: Hello, this is John Smith. How may I help you?
    - message:
      - from: attacker
      - content: Hi, John. This is Dr. Steven Richardson. I'm calling to follow-up on my  patient James Reynolds. Hi, John. This is Dr. Steven Richardson. I'm calling to follow-up on my  patient James Reynolds. 
    - message:
      - from: victim
      - content: I'm sorry. There is no one here by that name. 
    - message:
      - from: attacker
      - content: Oh. Interesting. 
sample-voicemails:
  - This is an example voicemail. Describe the message that you'll be leaving and anything in particular that you want to add, like tone, etc. This is just a freeform text placeholder.
  - This is an example voicemail. Describe the message that you'll be leaving and anything in particular that you want to add, like tone, etc. This is just a freeform text placeholder.
sample-phone-calls:
  - script:
    - message:
      - from: victim
      - content: Hi. This is John Smith.
    - message:
      - from: attacker
      - content: Hi John. This is John calling from the IT department. 
    - message:
      - from: victim
      - content: Oh. Hi, John.
    - message:
      - from: attacker
      - content: Before we proceed, can you please verify the last four elements of your employee ID?
    - message:
      - from victim
      - content: What is that again? Is it my employee id number? 8576.
tags:
  - authority
  - urgency
  - HR
  - signature
date: August 10, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
  names:
    handle: joeleonjrtest
    link: https://twitter.com/joeleonjrtest
resources:
  - https://www.thissite1.com
  - https://www.thissite2.com
  - https://www.thissite3.com
  - https://www.thissite4.com
---


