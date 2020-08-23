---
layout: pretext
title: Coronavirus Pandemic Loan
short-description: >
  The US Small Business Administration providing business owners with a form to fill out to apply for a pandemic-relief loan.
long-description: >
  The United States Small Business Administration (SBA) provides tools and resources to US-based small businesses. One of the many resources offered by the SBA are loans. During the COVID-19 pandemic, the government authorized loans to support small businesses suffering during the pandemic. There was a lot of confusion surrounding the program since it was created in a matter of a few weeks. This email seeks to capitalize on the confusion and needs of small business owners (and their finance department) by providing a fake loan application form for small business owners to fill out and return to the "SBA" (aka the attacker). The form provided asks for personal information like financial information, bank statements, identity information, etc. The form could be sent as an attached document or a link to an online webform. When the victim returns the form to the attacker, they could then use their personal information for other scams. Note that this pretext could be used in other countries; however, the SBA would need to change to the local equivalent.
analysis: >
  This pretext prays on small businesses in an extremely vulnerable financial situation by offering them the allure of additional funding. Also, at the time this pretext was heavily used, there was a lot of confusion surrounding the loan program application process, which aided attackers in tricking victims into providing their info.
goals:
  - info gathering
methods:
  - email
payloads:
  - phishing page
  - doc
  - docx
  - pdf
sample-payloads:
  - payload:
      type: phishing page
      description: An online form requesting victim personal identity and financial information, such as SSNs, EIN, bank routing numbers, business revenue, etc.
  - payload:
      type: doc
      description: A Word document containing a form requesting victim personal identity and financial information, such as SSNs, EIN, bank routing numbers, business revenue, etc. The email should state that in order to apply for loan relief, the victim must attach the completed form in a reply email.
sample-emails:
  - email:
    image: "/coronavirus-pandemic-loan-email1.png"
    source: https://www.bleepingcomputer.com/news/security/cisa-alerts-of-phishing-attack-targeting-sba-loan-relief-accounts/
  - email:
    from: disastercustomerservice@sba.gov
    subject: "Coronavirus Pandemic Loan (COVID-19)"
    body: | 
      Dear {FIRST NAME},

      As you might have heard, the US Federal Government has authorized the Small Business Administration (SBA) to provide small business owners with emergency financial relief during the Coronavirus pandemic. The SBA will provide a select group of US small businesses with up to $300,000 in loans. These loans will automatically convert to grants (meaning you do not have to pay them back), if you do not fire any employees before September. To apply for this loan, please visit the following website and fill out the form completely. 

      Note: Incomplete applications will not be considered.

      Thank you,
      U.S. SBA
tags:
  - authority
  - urgency
  - pandemic
  - coronavirus
  - covid
  - covid-19
  - sba
  - small business administration
  - loan
  - relief
date: August 23, 2020
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
resources:
  - https://www.bleepingcomputer.com/news/security/cisa-alerts-of-phishing-attack-targeting-sba-loan-relief-accounts/
---


