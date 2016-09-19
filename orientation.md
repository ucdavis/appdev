---
layout: page
title: Developer Orientation
permalink: /orientation/
---

Welcome!

The purpose of this document is to help new developers get up-to-speed on what they should know working at
UC Davis. It is meant to shortcut to the type
of knowledge one might have had they had been working for the University for
a decade or two.

This document tries to accomplish this in a few different ways: describing
the types of developers and "development shops" that exist on campus,
explaining how they do and sometimes don't work together, and answering
common questions about infrastructure such as: Where is dataset X stored? How can I access
it? Where should I be hosting applications? What's the best way to query the data I need to write my application?

If you have any corrections, ideas, or suggestions for this document, please
don't hesitate to get in touch.

* [UCD Structure Explained](#ucd-structure-explained)
* [Data Systems on Campus](#data-systems-on-campus)
* [Recommended Practices](#recommended-practices)
* [Languages and Libraries Common at UCD](#languages-and-libraries-common-at-ucd)
* [The Developer Community at UCD](#the-developer-community-at-ucd)
* [Finding Example Source Code](#finding-example-source-code)

## UCD Structure Explained

UC Davis is a public University in the University of California higher education
system chartered by the California State Constitution. It receives funding
from both the State of California, students (via tuition), donors, and through
specific research grants. *A developer position may be a permanent position or
it may be a temporary position funded by a grant.*

UCD is generally thought of as comprising of staff, students (both undergraduate
and graduate), faculty, and researchers. Though some areas of the University
are administered by staff, much of the University's administrative authority
ultimately comes from the faculty via the Academic Senate or from faculty-filled
positions (including the Office of the Chancellor).

The University itself is federated, consisting of colleges, schools, and other
units which receive some dictums from a central authority but retain much
independence in their operation. This allows various units to craft their
methodologies with a fitness suited to their purpose. This does create challenges
in collaboration however, as units are not forced to share code, share development
practices, and so on.

Some of these collaboration challenges are mitigated by SIGs (special interest groups) or other
community instruments which allow like-minded staff and
faculty to come together and share ideas and develop collaborations.

The UCD Developers' SIG is one such group. You can find more about it on our
About page.

## Data Systems on Campus

Though not everything on campus is centralized, there are a few key systems in use:

 * **[Banner](https://sis.ucdavis.edu/)**: a 'SIS' (student information system) implementation, used by this and
 other campuses both inside and outside the UC organization. It stores class schedules,
 instructor workloads, and grades. It is provided by a company called Ellucian and
 operates on top of the Oracle RDMS.  
 For direct database query access, [fill out this form](https://sis.ucdavis.edu/access/secure/D048BannerAccessRequest.pdf).

 * **[LDAP](http://middleware.ucdavis.edu/ldap.php)**: located at ldap.ucdavis.edu, LDAP is one of the central repositories of
 student, staff, and faculty information. It contains names, contact information, and
 appointment (who works where) information.

 * **[PPS](http://afs.ucdavis.edu/systems/pps/index.html)**: the current payroll system at UCD. Access is fairly restricted for
 obvious reasons. PPS contains information about an individual's appointments (note: it is
 possible that an employee is paid from more than one funding source and may have
 multiple appointments).

 * **IAM**: a relatively new system (as of 2015) aimed at providing a single source
 of information about individuals on campus. It connects with PPS, Banner, and
 other systems to compose a single view on contact information, appointments, and
 other commonly needed information about a person.

 * **[CAS](https://ucdavis.jira.com/wiki/display/IETP/UC+Davis+CAS+Service)**: an open source authentication system, CAS allows for multi-site access
 and a central repository for providing user accounts. *Most secure websites on campus
 use CAS and do not manage logins by themselves.*

 * **[Shibboleth](https://ucdavis.jira.com/wiki/display/IETP/Shibboleth+for+SSO+at+UC+Davis)**: Shibboleth uses the widely deployed and industry standard SAML protocol, and its strengths lie in secure, federated authentication and authorization, maintaining privacy when necessary. Generally, if colleagues outside UC Davis use your website, or might in the future, then you should consider using Shibboleth for your application's authentication.

 * **Campus Data Warehouse**: an Oracle repository of information including
 census snapshots for courses (enrollment and wait list counts, etc.)

 * **ICMS**: a list of all courses approved to be taught at UCD, housed in an Oracle
 database.

 * **EDMS**: an electronic document management system, used by HR, Accounting
 & Finances, and other units.

 * **Mothra**: an older system which maintains account permits for every individual
 associated with UC Davis.

 * **uConnect**: previously called XEDA, this is a campus-wide, managed Active Directory
 instance. It is synchronized with Outlook 365.

 * **Sympa**: located at lists.ucdavis.edu, Sympa is an e-mail list system. It can be
 configured directly or use remote data sources for its membership lists. It is the
 recommended way to host a mailing list on campus.

 * **ServiceNow**: primarily used for support tickets, ServiceNow is a relatively
 recent addition to the UCD campus (~2015) and allows for multiple departments to escalate
 issues to each other.

## Recommended Practices

The recommended practices at UCD are not so different from what you might find at
other places of employment, though UCD developers tend to be in smaller groups and
be a bit more isolated than is likely common.

* **Source code revisioning**: git, Subversion, CVS, and Team Foundation Server are all
examples of source code revision systems. They are useful for many reasons: backing
up your source code, enabling you to find differences between two points in development
(very useful for bug hunting), sharing/publishing code (optionally), and in supplying
material for a continuous integration server.

* **Setup, requirements, usage, and technical documentation**: It is critical that you provide a minimum amount of documentation about your project such as how to install and configure your project (setup), what
systems will and won't support your project (requirements), how to use your project
generally (usage), and any needed technical documentation (class maps, ER diagrams, anything
you think is helpful).

* **Issue tracking**: Issue tracking systems help developers keep track of work that is on-going or
needs to be done in the future. This can be integrated with your source code revisioning system to better
tie 'code commits' to the reasons they were performed (e.g. "Fixes bug #34, login page returning HTTP 503").
GitHub, BitBucket, and many other sites offer this functionality. It is always good to document ideas, bugs,
etc., even if you do not know when you will get around to them.

* **Support system (ticketing)**: A good support ticket system provides users with a centralized
location to submit their requests and feedback. It also helps to establish accountability that needed
work will be done. The campus-wide ServiceNow installation is one such system.

* **Continuous integration**: Continuous integration systems usually watch a source code repository,
build the code, run tests, and if tests pass, automatically deploy the code to a staging or production
environment. While this may take some time to set up, it makes the process of future development very
smooth.

* **Code reviews**: If you have other team mates, code reviews can be a helpful practice. Some development
teams mandate code reviews and some merely use them on more complex code. A code review generally ensures
at least two pairs of eyes have seen source code. This helps catch simple bugs, syntax mistakes, ensure
source code comments make sense, and can help developers learn techniques from one another.

* **Testing**: To be written.

* **Linting**: To be written.

* **Security scanning**: To be written.

## Languages and Libraries Common at UCD

UC Davis does not have specific technology stack requirements (languages, frameworks, etc.)
for developing applications. However, there are a few technology stacks commonly found here.
Please understand this is not an authoritative nor exhaustive list and merely serves to
illustrate some technologies for which you may be able to find UCD-specific source code,
camaraderie, etc. for:

 * Java (JSP Servlets, Spring Framework)
 * C# .NET (MVC, ASP.NET)
 * ColdFusion
 * Python (Plone, Django)
 * PHP (WordPress, Zend Framework)
 * Javascript
 * Oracle SQL (stored procedures, views)
 * Linux servers (Ubuntu, RHEL)
 * Windows servers (IIS, domain controllers)
 * Perl, Ruby

## The Developer Community at UCD

As of a survey in March 2016, UCD has an estimated 150 employees who are tasked with writing
source code most of their time. As many as 300 employees may write source code at least some of the time.

Developers have a few ways to find community:

 * The App Dev SIG (this website and its meetings)
 * The App Sec SIG (security focus with support from the UCD CISO office)
 * ucdavis.slack.com (#appdev channel, amongst others)
 * tsp-share mailing list (more IT-focused than developer engineering but good to watch)

## Finding Example Source Code

Often time to solve a problem, you just need to adapt someone else's solution.
There's no shame in doing so: it saves time, teaches you new methods, and is
arguably the way culture and technology evolve.

Besides typical public resources like [Stack Overflow](https://stackoverflow.com),
UCD specific source code can be found at [github.com/ucdavis](https://github.com/ucdavis)
and BitBucket. You should also feel free to ask for example source code from your
colleagues.

Notably, there is the UCD project registry found on this website. It will enable you
to see some projects for whom source code has been published and is cross-referenced by
relevant tags such as whether a project uses CAS, Banner, LDAP, etc. This will help
you find what you're looking for quickly.
