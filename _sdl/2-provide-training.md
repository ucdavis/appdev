---
layout: sdl
practice: "02"
title: Provide Training
description: Security is everyone’s job. Developers, service engineers, and product managers must understand security basics.
icon: provide-training
---
Developers, service engineers, and product managers must
understand security basics and know how to build security into software and services to
make products more secure while still addressing business needs and delivering value.
Even end users must understand the ramifications of certain activities and the best
practices for maintaining proper data security.

Although security is everyone’s job, it’s important to remember that not everyone needs to
be a security expert nor strive to become a proficient penetration tester. However, ensuring
everyone understands the attacker’s perspective, their goals, and the art of the possible will
help capture the attention of everyone and raise the collective knowledge bar.

Effective training will complement and re-enforce security policies, SDL practices,
standards, and requirements of software security, and be guided by insights derived
through data or newly available technical capabilities. In addition, it is not enough to just
learn about cybersecurity principles and practices at the beginning of a career. New threats,
the rapidly changing technical landscape, and ever more sophisticated attacks require that
knowledge and skills are kept constantly updated. Departments should evaluate the position
descriptions for any role involved in software development to ensure that they address
security training expectations and responsibilities.

# Basic Training - Entire Development Team
A layered approach is recommended for security training. At the most basic level,
development teams should strive to educate their entire team regarding the most critical
application security basics. This includes roles such as developers, testers, technical
supervisors, technical project coordinators and program managers, database developers or
administrators, data analysts, and anyone else involved in the software development
lifecycle or whose area of responsibility includes the safeguarding of data or systems.

A popular example of these basics are the “OWASP Top 10 Most Critical Web Application
Security Risks” (<https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project>)
such as:
1. Injection
2. Broken Authentication
3. Sensitive Data Exposure
4. XML External Entities (XXE)
5. Broken Access Control
6. Security Misconfiguration
7. Cross-Site Scripting (XSS)
8. Insecure Deserialization
9. Using Components with Known Vulnerabilities
10. Insufficient Logging & Monitoring

The OWASP website itself is a good resource for learning more about the Top 10. However,
UC Davis also provides free eCourses on the OWASP concepts through the UC Learning
Center. These include:
* Introduction to OWASP and the Top 10
<https://uc.sumtotal.host/core/pillarRedirect?relyingParty=LM&url=app%2Fmanagement%2FLMS_ActDetails.aspx%3FActivityId%3D236849%26UserMode%3D0>
* OWASP A5 and A1: Security and Injection
<https://uc.sumtotal.host/Core/pillarRedirect?relyingParty=LM&url=core%2Factivitydetails%2FViewActivityDetails%3FActivityId%3D334210%26UserMode%3D0>
* OWASP A4 and A2: Broken Applications
<https://uc.sumtotal.host/Core/pillarRedirect?relyingParty=LM&url=core%2Factivitydetails%2FViewActivityDetails%3FActivityId%3D334209%26UserMode%3D0>
* OWASP A8 and A3: Cross-site Attacks
<https://uc.sumtotal.host/Core/pillarRedirect?relyingParty=LM&url=core%2Factivitydetails%2FViewActivityDetails%3FActivityId%3D333815%26UserMode%3D0>
* OWASP A7 and A6: Leaky and Unprepared Applications
<https://uc.sumtotal.host/Core/pillarRedirect?relyingParty=LM&url=core%2Factivitydetails%2FViewActivityDetails%3FActivityId%3D333914%26UserMode%3D0>
* OWASP A10 and A9: API and Component Attacks
<https://uc.sumtotal.host/Core/pillarRedirect?relyingParty=LM&url=core%2Factivitydetails%2FViewActivityDetails%3FActivityId%3D334276%26UserMode%3D0>

The University of California also provides an opportunity for application development staff to
learn and share more about security through the UC Cybersecurity Summit and the UC
Information Security Symposium. Attending these events is highly encouraged for all staff
involved in application development. There are also a number of free or low cost online
training resources such as LinkedIn Learning (formerly Lynda.com), Udemy, and Cybrary.

# Specialty Training - Developers and Administrators
The next level of security training should focus on the development environment(s) being
used. This can include the coding language itself, the data sources or APIs in use, the
development stack, or the frameworks being used. For example, a .Net development team
might target security training in C#, SQL Server, IIS, ASP.Net, or Entity Frameworks while a
LAMP development team would focus on security training for Apache, MySQL, and PHP.

Specialty training is appropriate for application developers, database administrators, web
and application server administrators, and architects. Individuals involved in QA or Software
Lifecycle tasks may also benefit. Resources for security training in these specialties are
often free and publicly available. However, they often require a dedicated commitment by a
development team to actively seek them out and set aside time for both the initial learning
and refreshment. Development teams should check back often as they strive to stay
up-to-date with the latest security information and releases for their particular
environment(s).

OWASP can provide a starting place with learning resources targeting:
* Popular Programming Languages
* .NET Programming
* Java Programming
* PHP Programming
* Mobile Programming

Many of the most common database applications have published database security best
practices. Usually these can be found on the vendors knowledge base or documentation
site. Here are some examples for recent versions of commonly used databases:
* SQL Server
* Oracle
* MySQL

Web and application servers such as Apache HTTP Server, Tomcat, WebLogic, and IIS
often publish resources describing how best to harden against threats.

When using cloud infrastructure services, teams should avail themselves of the security
training and resources available, such as:
* AWS
* Azure
* Google Cloud

# Advanced Level Training - Architects and Security Specialists
The highest level of security training usually involves a dedicated commitment of time and
financial resources. This training may provide a path towards professional certification or it
may not, however this advanced level education often involves full day or multi-day paid
courses. Development leads, architects, and security specialists should consider this level
of training although, if resources are available, it can be extended to others.

One popular vendor of this level of training is SANS. The Information Security Office can
help facilitate the purchase of SANS On-demand training. They do this through the SANS
Partnership Series program. The SANS Partnership Series is an outreach program created
to provide highly discounted training to support constituencies that have a clear impact on
national security, large numbers of information security practitioners and extreme budget
constraints that limit access to necessary training.

Some security trainings that are recommended for developers through SANS are:
* DEV522: Defending Web Applications Security Essentials
* DEV534: Secure DevOps: A Practical Introduction
* SEC540: Secure DevOps and Cloud Application Security
* DEV541: Secure Coding in Java/JEE: Developing Defensible Applications
* DEV544: Secure Coding in .NET: Developing Defensible Applications
* SEC542: Web App Penetration Testing and Ethical Hacking
* SEC642: Advanced Web App Penetration Testing, Ethical Hacking, and Exploitation
Techniques

At the upper most level of advanced training are the paths to professional certifications.
Achieving and maintaining professional security certifications can help ensure that a
development team has made application development a priority. There are many types of
security certifications, but the ones that focus on application development include:
* CSSLP – Certified Secure Software Lifecycle Professional
* CASE - Certified Application Security Engineer
* GIAC Certifications: Developer

# Creating a Security Training Plan
A security training plan should be part of the Information Security Management Plan of any
development team. This should include the expected minimal level of training required for
each role, the training methods that will be made available, and the frequency of the
training. Keep in mind that some staff may fulfill multiple roles, particularly for smaller
development teams.
Here’s a partial example for a small-to-medium team. A given development team may use
different technology or have other needs. This partial example is just a starting point:
1. All staff on the development team will:

    a. Read/re-read the OWASP Top 10 at least once every 2 years.

2. Application developers will:

    a. Read/re-read the OWASP Top 10 every year.

    b. Review the OWASP Java Programming guidance every year

    c. Attend the UC Cybersecurity Summit or the UC Information Security
Symposium every two years
3. Server administers will:

    a. Read/re-read the OWASP Top 10 every year.

    b. Review the Apache Tomcat hardening guide every year

    c. Review the AWS Security Guidelines every year

    d. Attend the UC Cybersecurity Summit or the UC Information Security
Symposium every two years
4. The lead developer will:

    a. Monitor the OWASP Blog for news of important changes or alerts in the
OWASP information.

    b. Monitor the AWS Security Blog for news of important changes or alerts

    c. Attend the UC Cybersecurity Summit or the UC Information Security
Symposium once a year

    d. Ensure the effective and ongoing security training of the development team. For example, meeting regularly and discussing a specific topic (e.g. cross-site scripting, encryption).
