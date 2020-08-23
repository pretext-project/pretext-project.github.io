# Contribution Guidelines

First, thanks for helping out. This is a community-driven project. The more pretexts folks like you contribute, the more valuable this resource will be for everyone.

## Instructions

Pretext Project is based on [Jekyll](https://jekyllrb.com/), a static blog site generator. All of the pretexts are located in the /\_pretexts/ subfolder. When we deploy the Prext Project site with new updates, Jekyll parses through all of the pretexts and generates a complete static website. This makes life easier since we don't need to rely on a database backend. 

When you want to contribute a new pretext, please create a .md file based on the format listed below. 

```
---
#Don't change this value
layout: pretext

title: New Pretext Name

short-description: >
  This should be a short one or two lines briefly summarizing the pretext.
  Leave the details for the long description.

long-description: >
  This is where you can get wordy. This is your time to fully document the pretext.
  What are the types of targets? What does someone need to know in order to use this pretext 
  on a social engineering engagement? When does it not work?

analysis: >
  Where the long-description field is used to describe the pretext, the analysis section explains 
  why the pretext is effective. What pyschological principles are you drawing on? When will this most 
  pretext most likely work? Etc.
  
#There are 5 goals the pretext could be used for. The 5 are listed below. Only list the relevant one(s) for your pretext.
# - malware - goal is to get the user to execute malware on their system
# - cred harvest - goal is to capture a user's credentials on a phishing page
# - info gather - we're just trying to gather information about a company / individual / their computer
# - acct takeover - goal is takeover a user's account, maybe that's an email account, VPN access, etc.
# - funds transfer - also called business email compromise; goal is to transfer funds from a target to your account
# ... have more ideas, feel free to make a pull request

goals: 
  - malware
  - cred harvest
  
#Methods = Communication Methods. There are 6 methods the pretext can be used for. Only list the relevant one(s) for your pretext.
# - email 
# - phone - two-way phone-based conversation; aka vishing
# - voicemail - no interaction with user over the phone
# - chatbot - online ecommerce-style chatbots
# - sms - text messages
# - usb drop - dropping a USB device near a target's physical location and hoping they plug it in

methods:
  - email
  
#Payloads. There's a lot here. Only list the relevant one(s) for your pretext.
# - doc
# - docx
# - xls
# - xlsx
# - ppt
# - pptx
# - pdf
# - hta
# - exe
# - bat
# - zip (not just .zip files, but generally any compressed file)
# - xss - situations when you want to deliver a payload via XSS or take advantage of an XSS
# - csrf - situations when you want to take advantage of a CSRF that you discovered
# - click-once
# - phishing page - likely one of the most popular options; refers to any page that mimicks a legitimate page
# - ole
# - drive-by-download 
# - usb drop - when the payload lives on a usb for use with a usb drop; you could combine this with other payloads
# - cloud hosted file - when you want to host a malicious file on a cloud service like dropbox and induce victim to get file from there

payloads:
  - doc
  - docx
  - click-once
  - phishing page
  - hta

#Sample Payloads: this is where you provide a detailed explanation of your vision for a payload. Only 3 per pretext (at the moment).
# The "type" field should correspond exactly to one payload type (mentioned above)
# The "description" field is free form. No embedded images. Only text.

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

#Sample Emails: This is where you can add an example email for the pretext. Add as many as you'd like.
# To create a new email, follow the structure below. Note that the "body" section retains all new lines and formatting. Also, the attachments
# section is just for show and doesn't actually attach a file. If in your pretext, you envision sending an attachment, then provide a name + extension for it, 
# this way it'll feel more real. Also, if you'd like to provide a source for the email, feel free.

# To add an image, please add it to the /assets/img/pretext-images/ directory. Name the file using the name of this pretext. For example, an image of an email for the pretext saved as "sample-pretext.html", could be called "sample-pretext-email1.png". Save that in the pretext-images file and provide the filename to the "image" attribute below.

sample-emails:
  - email:
    from: Corporate HR
    subject: "Action Required: new pretexts"
    body: | 
      Dear colleagues,

      This is the format that our emails will appear on the pretext page. It's rather simple, but it gets the job done. If you have any questions, please contact the HR department.

      Thank you,
      HR
    attachments:
      - attachment.xls
    source: https://thissource.com

  - email:
    image: "sample-pretext-image.png"
    source: https://source.com
    
#Sample USB Drops: Pleases just jot down the details of what think the USB drop looks like, how it works, etc. Pretty simple.    
    
sample-usb-drops:
  - This is an example USB drop description. In here, you'd put all the details  about how you'd conduct the USB drop - where, what's on the drive, etc. 
 
#Sample Text Messages: The text message section is broken down by "message". Within each "message", you need to specify who the message is "from" (either 
# "victim" or "attacker") and what the message is about "content". 

sample-text-messages:
  - script:
    - message:
      - from: victim
      - content: Hello, this is John Smith. How may I help you?
    - message:
      - from: attacker
      - content: Hi, John. This is Dr. Steven Richardson. I'm calling to follow-up. 
    - message:
      - from: victim
      - content: I'm sorry. I think you have the wrong number. 
    - message:
      - from: attacker
      - content: Oh. Interesting. Is this not John Smith?

#Sample Chatbot Messages: The chatbot message section is broken down by "message". Within each "message", you need to specify who the message is "from" (either 
# "victim" or "attacker") and what the message is about "content".
      
sample-chatbot-messages:
  - script:
    - message:
      - from: victim
      - content: Hello, welcome to ABC inc. How can I help you?
    - message:
      - from: victim
      - content: Hello, welcome to ABC inc. How can I help you?
    - message:
      - from: attacker
      - content: Hi. How do I submit my resume for a new job? 
    - message:
      - from: victim
      - content: Please email us here. 
    - message:
      - from: attacker
      - content: Can I attach it to this chat window?

#Sample Voicemails: straightforward. Just jot down what the voicemail says.

sample-voicemails:
  - This is an example voicemail. Describe the message that you'll be leaving and anything in particular that you want to add, like tone, etc. This is just a freeform text placeholder.
  - This is an example voicemail. Describe the message that you'll be leaving and anything in particular that you want to add, like tone, etc. This is just a freeform text placeholder.

#Sample Phone calls: This is just like the text message and chatbot sections. Again, the "from" field must state either "victim" or "attacker".

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

#Tags:  You can't see them on the homepage table, but when you search against all pretexts, you're also searching against the tags. 
# So please use these as much as you'd like. The search functionality is OK. But help us out and add extra search terms for situations like:
# hr = human resources. Pleae add both "hr" and "human resources".
tags:
  - authority
  - urgency
  - HR
  - human Resources
  - signature
  
#Date: Please use Month DD, YYYY format.  
date: August 10, 2020

#Contributors: add your name and twitter or github handle like below
contributors:
  name:
    handle: joeleonjr
    link: https://twitter.com/joeleonjr
    
#Resources: Want to give someone credit for this pretext idea? Or want to provide some relevant links, like a threat actor using this pretext in the wild?    
resources:
  - https://www.thissite1.com
  - https://www.thissite2.com
  - https://www.thissite3.com
  - https://www.thissite4.com
---
```

You'll notice a lot of the headings and values are lowercase. Please default to lowercase, unless you're adding a freeform value, like the title, description, analysis, sample emails, etc.

When in doubt, please just copy/paste from this sheet. You can remove the comments (lines that start with #).

## Submitting Pretexts

Please submit a pull request adding your .md file to the /\_pretexts/ folder. We'll review ASAP and get it folded into the collection.

## Questions?

If you have any questions at all, please contact [@JoeLeonJr](https://twitter.com/joeleonjr).
