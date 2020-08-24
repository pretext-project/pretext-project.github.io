---
layout: pretext
title: Salary Renegotiation Process
short-description: >
  The Human Resources (HR) department is conducting salary renegotiation conversations and needs employees to both acknowledge the renegotiation process and sign up for a time slot to discuss their salary.
long-description: >
  The Human Resources (HR) department at a medium-large organization is changing the salary renegotiation process. All employees must acknowledge the new process and if interested in raising their salary, schedule a time to meet with HR. There are multiple opportunities for attackers to capture credentials or execute malware on a target's computer. An attacker could redirect users to a phishing page with a VPN or O365 portal and capture credentials before a victim can navigate to the new process document or schedule a meeting. Alternatively, a malicious PDF file or HTA application could be used for acknowledging the new process or to schedule a salary renegotiation meeting. A spin on this pretext is emailing as if you were a third-party salary renegotiation consulting company working on behalf of the target. 
analysis: >
  We go to work to make money. If your company is offering an opportunity to make more money, you'll likely take it. One downside is this could cause quite a stir in the office, which means employees will be more likely to discuss this email with others. The more a phishing email is discussed, the more likely it is to get caught, so that's definitely a downside of this pretext.
goals:
  - malware
  - cred harvest
methods:
  - email
payloads:
  - drive-by-download
  - phishing page
  - pdf
  - doc
  - docx
  - hta
  - ics
sample-payloads:
  - payload:
      type: phishing page
      description: Fake VPN or email portal login page to capture credentials prior to letting employees view the new salary renegotiation process information or book a meeting to discuss salary.
  - payload:
      type: pdf
      description: Users are sent a PDF file with the salary renegotiation process information and are asked to sign the file and return it.
sample-emails:
  - email:
    from: HR (Human Resources)
    subject: "Salary Renegotiations"
    body: | 
      Dear {FIRST NAME},

      The Department of Human Resources has amended the salary renegotiation process. In order to quality for a pay raise, all interested employees, must schedule a one-on-one meeting with a member of the HR staff. The particular HR salary staff member assigned to work with you on salary negotiations will email you separately.

      Prior to scheduling a meeting with your HR liaison, please review the attached PDF document outlining the new salary renegotiation process. Failure to review the file will disqualify you from petitioning for a pay raise this quarter.

      Thank you,
      HR
    attachments:
      - new-salary-renegotiation-process.pdf
  - email:
    from: The Salary Consulting Company
    subject: "{COMPANY NAME} Salary Renegotiations"
    body: | 
      Dear {FIRST NAME},

      The Department of Human Resources at {COMPANY NAME} recently contracted our company to oversee the corporate salary renegotiation process. While managers can still petition HR for a pay raise for their direct reports, individuals wishing to make their case for an increase in salary, must first present their application to our team. 

      If you're interested in discussing a pay raise, please book a time on one of our team member's calendars, located here. 

      Thank you,
      The Salary Consulting Company

tags:
  - intrigue
  - salary
  - money
  - negotiation
  - calendar
  - meeting
  - schedule
date: August 24, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
---


