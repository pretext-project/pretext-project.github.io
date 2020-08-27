---
layout: pretext

title: Updated Terms of Service

short-description: >
  Users are required to accept the updated terms of service in order to continue using a service. 

long-description: >
  A service used by the victim sends them an email stating that the terms of service and/or privacy policy has been updated. In order to continue using the service (that part is key), the user must accept the updated legalese. The email contains a link to "accept" the updated policies, but it lands them on a login page for the service. This is a chance to capture credentials. Once the user enters their creds, you could do a few different things including just redirecting them to the the actual terms / policies pages. Or you could just redirect them to a simple page saying "Thank you for accepting the updated terms of service and privacy policy. To view the policies, please click here."

analysis: >
  As long as the attacker references a service commonly used by the victim, then they might be compelled to accept the updated policies so that they can keep using the service. In this case, the prospect of not being able to continue using the service as normal is the main driver to convince them to take action.

goals: 
  - cred harvest

methods:
  - email

payloads:
  - phishing page

sample-payloads:
  - payload:
      type: phishing page
      description: Before the user can navigate to the terms of service page, they need to login to the service. If this is Office 365, we can use evilginx2 to capture their credentials for Microsoft. Evilginx2 could also be used for other services like Twitter, LinkedIn, etc.

sample-emails:
  - email:
    from: "{SOME SERVICE THE VICTIM USES}"
    subject: "Action Required: accept updated terms of service"
    body: | 
      We recently updated our Terms of Service and Privacy Policies. In order to continue using {SERVICE NAME}, you must review and accept our terms of service. 

      If you have any questions about the changes made to our policies, please reply to this email.

      Thank you,
      {SERVICE} Legal

  - email:
    image: "udpated-terms-of-service-email1.png"
    source: https://www.greathorn.com/blog-terms-of-service-phishing-attack-is-the-latest-to-target-o365-users/
    
tags:
  - terms
  - terms of service
  - tos
  - updated
  - policies
  - privacy policy
  - HR
  - human Resources
  - office 365
  - o365
  
#Date: Please use Month DD, YYYY format.  
date: August 27, 2020

#Contributors: add your name and twitter or github handle like below
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
     
resources:
  - https://www.greathorn.com/blog-terms-of-service-phishing-attack-is-the-latest-to-target-o365-users/
  - https://github.com/kgretzky/evilginx2
---