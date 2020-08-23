---
layout: pretext
title: Web Browser Check
short-description: >
  The IT department requires employees to run software to check their web
  browsers for newly discovered vulnerabilities.
long-description: >
  The IT department sends an employee an email stating that in recent weeks security researchers have found several new vulnerabilities targeting web browsers like Chrome, Firefox and Internet Explorer. In order to ensure the employee is browsing from an updated and secure web browser, they need to scan their web browser using the provided software. If their web browser is out of date, the software will inform the IT department. When the employee runs the software, it will display a progress bar, so they believe something is happening. Meanwhile, the browser check software (most likely an HTA or click-once application) will inject the malware. After the target is compromised, the application will state that their browser is up-to-date and not vulnerable. The best employees to target for this campaign are new employees or less computer-literate employees that might not understand how IT operates.
analysis: >
  This type of pretext relies on the recipient not understanding how IT operates. This would probably not work on a developer or an engineer. An intern, a salesperson or an employee in a non-technical role would be a good fit for this pretext.  
goals:
  - malware
methods:
  - email
payloads:
  - click-once
  - hta
sample-payloads:
  - payload:
      type: hta
      description: HTA application that displays text like "Currently checking your web browser" with a progress bar. Once the progress bar finishes, change the screen to say something like "Your computer passed the browser check. Please close out of this window." Check out the HTA payload example in the "resources" section.
  - payload:
      type: click-once
      description: Similar to the HTA idea.
sample-emails:
  - email:
    from: IT Department
    subject: "Action Required: web browser check"
    body: | 
      Dear {FIRST NAME},

      In recent weeks, researchers have found several bugs in major web browsers, like Chrome, Firefox and Internet Explorer. Your browser should be up-to-date, since we take care of updates from the IT department. However, some of these bugs are quite serious and we need to be sure that every staff member's web browser is updated. Attached, you'll find a file that will check your browser's version and inform us if you need to be patched. Please run this application at your earliest convenience. It shouldn't take more than 30 seconds.

      Thank you,
      <IT Director's name>
    attachments:
      - browser-check.hta
tags:
  - authority
  - urgency
  - IT
  - information technology
  - web browser
  - browser
  - vulnerability
date: August 23, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
resources:
  - https://github.com/t3ntman/Social-Engineering-Payloads/blob/master/Browser-Check/browsercheck.hta
  - https://github.com/t3ntman/Social-Engineering-Payloads/tree/master/Browser-Check
  - https://github.com/t3ntman/BrowserCheck
---


