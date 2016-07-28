---
layout: article
title: "Security Training Overview"
description: "A brief overview of the we45 Security Training."
date: 2016-07-25
category: "owasp"
image:
breadcrumb: Owasp
---

# we45 Security Training
#### 25 July 2016

## Overview
we45 primarily offers penetration testing services; in the course of security audits they discover clients tend to have the same issues across the board—which pretty closely coincide with the OWASP Top 10.

### Who is Abhay Bhargav?
- CTO of we45
- CISSP, GWAPT, CISA, ISO-27001CA, CPA, OCTAVE implementer
- Co-author of _Secure Java for Web Application Development_ (stopped using Java after writing this book)
- Author of _PCI Compliance: A Definitive Guide_
- Performed over 300 security assessments (to-date) for companies in over 10 distinct geographies
- Specializes in Web Application Security and Security Testing
- Trainer and Workshop Lead for we45 Security Training Workshops

### Program Expectations
Address everyone's needs in a room full of developers of varying skill levels. We utilize the same concepts and  approaches regardless of [modern] language. Focus on vulnerabilities and their consequences (especially financially). Trainees should understand attack families and the effects of those attacks (e.g., cross-site scripting may lead to browser-based malware, man-in-the-browser attacks, etc.). Real-world attackers _chain_ their attacks. 

## Everything is an App!
Very few static web pages remain (almost everything runs as or within the confines of an application: WordPress, Jekyll, etc.) We do not use thick clients anymore.

Everything revolves around microservices and web services; services consume API's (e.g., Internet of Things/IoT and mobile). AJAX and jQuery offer user-centric design (and new attack vectors). 

As criminal enterprise see the value of exploiting web applications, malicious agents have greater budgets as well as talent acquisition and outreach. The amount of money spent to engage in criminal activity makes security professionals' jobs much more difficult; _security literally cannot keep up with technology_. Take NoSQL as an example: NoSQL databases make analytics and search much easier than traditional relational databases. However, NoSQL databases do not ship with secure defaults, and lack of available information along with poor documentation make NoSQL databases easy targets. Most system administrators do not know how to secure their NoSQL databases.

### Rise of the Web Service
JavaScript often runs both the front and back ends of modern applications. 

Cloud infrastructure makes deploying applications a breeze. Services like AWS, Digital Ocean, and Azure allow users to virtualize a server in minutes (instead of waiting hours or days for your system administrator to deploy a server, you can have one almost immediately; this also means you can have a working server _without understanding the underlying technology_—or its security implications).

**JSON** becomes the dominant data interchange standard for Web 2.0, API, and mobile applications. JSON requires less overhead and less developer effort to parse than XML.

**AJAX** offers the standard for rich Internet applications.

**REST** surpasses SOAP as the standard protocol for API's (SOAP still has widespread usage among enterprise software). In an HTTP-based stack, REST reigns supreme.

### The Age of Mobile Applications
Mobile applications leverage Web 2.0 technology and heavily depend on web sockets (i.e., HTTP) and web services. If someone exploits a service "down the line," an attacker can [potentially] similarly exploit any application relying on that service (we saw this with Heartbleed). 

From personal experience, Bhargav sees 8 in 10 apps relying on web services suffer serious issues; primarily access control flaws (authentication _and_ authorization), injection flaws, and data access flaws. This leads to an increase in security impact for apps relying on API's and web services. 
