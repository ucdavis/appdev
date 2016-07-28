---
layout: article
title: "Web Application Security Incidences
description: "Brief case studies of web application breaches and their effects."
date: 2016-07-25
category: "owasp"
image:
breadcrumb: Owasp
---

# Web Application Security Incidences
#### 25 July 2016

### MySpace Samy Worm (2005)
One of the earliest cross-site scripting attacks.

Samy Kamkar wants more MySpace friends, so he writes a script to automate friend requests. Whenever someone views his page, they automatically become his friend, and propagate the script (so someone viewing Samy's friend's page _also_ automatically become Samy's friend). Samy's script creates millions of zombie requests to MySpace's servers and takes MySpace off for at least a day.
 
### CardSystems Breach (2005)
CardSystems, a large acquiring and issuing payment processor in the US, becomes the victim of a SQL injection attack against a Payment Authorization Web Application in use by CardSystems' customers. Attackers run queries every four days, dumping the databases, zipping up credit card data, and FTP'ing it to their own IP space (at least 40 million credit cards). 
 
The breach results in heavy FTC fines and CardSystems selling to a third party.

### Rockyou Breach (2009)
Rockyou offers social networking apps (a precursor to Zynga). SQL injection attacks result in the loss of 30 million passwords still available online. Pentesters and security researchers often use this password list (assume attackers also use this data).

### Heartland Payment Systems (2015)
Heartland, the 5th largest payment processor in the US, suffers a breach following a SQL injection attack. Attackers sniff the application/database connection and expose 120 million credit card numbers.

### MENA Card Breaches
Two major banks in the MENA (Middle East) region suffer $65 million in losses following a simple and effective web application breach. The attack revolves around directory brute-forcing and application compromise; they discover the banks running JBoss JMX (popular among banks). `GET` requests require authentication via username and password, but `HEAD` requests do not, granting attackers administrative access. The banks encrypt credit and debit cards, so the attackers find no value there. *However*, the banks do not encrypt prepaid cards. Attackers increase the limits on the prepaid cards to $1,000,000 and duplicate the cards locally, then strike multiple ATM's in a single evening. Losses total $65,000,000.

### Ashley Madison Breach (2015)
Extramarital affairs site fell victim to SQL injection, exposing over 37,000,000 user records. No financial data available, but attackers use the database to blackmail and defraud users. Ashley Madison uses bcrypt for passwords, so attackers cannot retrieve them.

### Product Exploits
Researchers discover exploits and security issues in numerous commercial and open source products, including:
- Oracle
- SAP
- Magento
- JBoss
- WordPress
- elasticsearch
- CISCO 

Many of the vendors can not or do not fix the issues at hand. 
