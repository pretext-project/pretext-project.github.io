---
layout: pretext

title: WebEx Security Vulnerability

short-description: >
  WebEx users and account administrators receive an email stating WebEx has a critical security vulnerability and requires immediate action.

long-description: >
  WebEx users and account administrators receive an email from "WebEx" with details of a new critical CVE (Common Vulnerabilities and Exposures) security flaw that requires immediate patching. The email is HTML-based and mimics the actual Cisco Security Advisory format (see link in the resources section below). In fact, attackers could use an actual security advisory in the email. The email also contains a link to review / fix the security vulnerability that requires users to first log into WebEx, thus providing the attacker an opportunity to harvest credentials. 

analysis: >
  Cybersecurity is top of mind for many employees and IT administrators, especially in the age of large-scale remote working. Given all of the attention Zoom received in the spring of 2020 for Zoombombing, it would be reasonable to believe employees would pay extra attention to another teleconferencing service that might have security issues.

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
      description: Fake WebEx or Cisco VPN login page designed to capture user credentials.

sample-emails:
  - email:
    image: "webex-security-vuln-email1.png"
    source: https://www.proofpoint.com/us/threat-insight/post/remote-video-conferencing-themes-credential-theft-and-malware-threats
    
tags:
  - security
  - cve
  - security vulnerability
  - cybersecurity
  - it security
  - information security
  - urgency
  - information technology
  - it
  - webex
  - cisco
  - teleconference
 
date: August 28, 2020

contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr

resources:
  - https://www.proofpoint.com/us/threat-insight/post/remote-video-conferencing-themes-credential-theft-and-malware-threats
  - https://tools.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-asaftd-ro-path-KJuQhB86
---