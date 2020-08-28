---
layout: pretext

title: Medical Test Results

short-description: >
  Victim receives an email from a medical office containing "their" medical analysis results.

long-description: >
  A victim receives an unsolicited email containing medical analysis data from a medical office. In this pretext, the attacker is not sending an email to a victim that they believe is waiting for medical results. Instead, the email is designed to pique the recipient's curiosity to view someone else's medical test results. The actual medical test referenced in the email could vary: Coronavirus, HIV, Blood work, etc. The email contains an attachment with the medical test results; however, that attachment is malware. 

analysis: >
  This would cross a line for ethical hacking purposes. This pretext prays on two things: (1) our natural concern for our health (2) curiosity of information sent to the wrong recipient.

goals: 
  - malware

methods:
  - email

payloads:
  - xls
  - xlsx
  - doc
  - docx
  - pdf

sample-payloads:
  - payload:
      type: xlsx
      description: Microsoft Excel workbook containing fake medical data results and malware via macro.
  - payload:
      type: pdf
      description: Attacker could grab a real medical analysis pdf from a google search and then embed some type of malware.

sample-emails:
  - email:
    image: "medical-test-results-email1.png"
    source: https://www.proofpoint.com/us/corporate-blog/post/attackers-use-fake-hiv-test-results-target-insurance-healthcare-and
    
tags:
  - curiosity
  - medical
  - medical results
  - doctor
  - doctors
  - covid
  - coronavirus
  - test results
  - health
  - health insurance
 
date: August 28, 2020

contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr

resources:
  - https://www.proofpoint.com/us/corporate-blog/post/attackers-use-fake-hiv-test-results-target-insurance-healthcare-and
---