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
  sends the victim to a phishing page in order to "sign" to view the new policy.
analysis: >
  By sending an urgent task from HR related to sexual harassment, most recipients will feel  obliged to review it quickly. Given the nature of the topic, many will not feel comfortable questioning any aspect about it.
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
      description: Word document containing the new policy. Require employees to enable macros in order to "sign" for it. Don't forget to dress up the document to look legitimate. 
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

      Due to the recent #MeToo movement, our firm has decided to update our sexual harassment policy. All employees are required to abide by these new regulations. To ensure everyone has read them, we require that you download the following policy and electronically sign to acknowledge receipt. If you have any questions, please contact the HR department.

      Thank you,
      HR
    attachments:
      - attachment.hta
tags:
  - authority
  - urgency
  - HR
  - human resources
  - signature
date: August 23, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
resources:
  - https://github.com/t3ntman/Social-Engineering-Payloads/tree/master/Sexual-Harassment-Policy-Update
---


