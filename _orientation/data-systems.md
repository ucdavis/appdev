---
layout: page
title: Data Systems on Campus
---

Though not everything on campus is centralized, there are a few key systems in use. You'll find full schema information for many of them at [datadictionary.ucdavis.edu](http://datadictionary.ucdavis.edu/).

 * **[Banner](https://sis.ucdavis.edu/)**: a 'SIS' (student information system) implementation, used by this and
 other campuses both inside and outside the UC organization. It stores class schedules,
 instructor workloads, and grades. It is provided by a company called Ellucian and
 operates on top of the Oracle RDMS.  
 For direct database query access, [fill out this form](https://sis.ucdavis.edu/access/secure/D048BannerAccessRequest.pdf).

 * **[PPS](http://afs.ucdavis.edu/systems/pps/index.html)**: the current payroll system at UCD. Access is fairly restricted for
 obvious reasons. PPS contains information about an individual's appointments (note: it is
 possible that an employee is paid from more than one funding source and may have
 multiple appointments).

 * **[KFS](http://afs.ucdavis.edu/systems/kuali/)**: As the current financial system at UCD, basically any time money is moved to, from, or around campus, KFS is involved. KFS stands for Kuali Financial System and you will occasionally hear it referred to as just "Kuali." Another common term you'll still see is "FIS" which is still being used widely to refer to the same thing.  
 [Visit the KFS direct access page](http://afs.ucdavis.edu/systems/fis/direct-access.html) for good information on gaining access as well as setting up a database connection.

 * **[LDAP](http://middleware.ucdavis.edu/ldap.php)**: located at ldap.ucdavis.edu, LDAP is one of the central repositories of
 student, staff, and faculty information. It contains names, contact information, and
 appointment (who works where) information. It supports both unauthenticated and authenticated queries, the latter providing access to additional information.

 * **IAM**: (Identity & Access Management) a relatively new system (as of 2015) aimed at providing a single source
 of information about individuals on campus. It connects with PPS, Banner, and
 other systems to compose a single view on contact information, appointments, and
 other commonly needed information about a person.

 * **[DaFIS/Kuali](http://afs.ucdavis.edu/systems/fis/)**: DaFIS and Kuali are both financial systems used at the University, the former being in the process of retirement.

 * **[CAS](https://ucdavis.jira.com/wiki/display/IETP/UC+Davis+CAS+Service)**: an open source authentication system, CAS allows for multi-site access
 and a central repository for providing user accounts. *Most secure websites on campus
 use CAS and do not manage logins by themselves.*

 * **[CANVAS](https://login.canvas.ucdavis.edu)**: Canvas is an open source LMS (learning management system) used by UC Davis. It replaces the older LMS SmartSite.

 * **[Shibboleth](https://ucdavis.jira.com/wiki/display/IETP/Shibboleth+for+SSO+at+UC+Davis)**: Shibboleth uses the widely deployed and industry standard SAML protocol, and its strengths lie in secure, federated authentication and authorization, maintaining privacy when necessary. Generally, if colleagues outside UC Davis use your website, or might in the future, then you should consider using Shibboleth for your application's authentication.

 * **Campus Data Warehouse**: an Oracle repository of information including
 census snapshots for courses (enrollment and wait list counts, etc.)

 * **ICMS**: a list of all courses approved to be taught at UCD, housed in an Oracle
 database.

 * **[LMS](http://lms.ucdavis.edu)**: a Learning Management System used by faculty and staff to register for various types of training.

 * **EDMS**: an electronic document management system, used by HR, Accounting
 & Finances, and other units.

 * **Mothra**: an older system which maintains account permits for every individual
 associated with UC Davis.

 * **uConnect**: previously called XEDA, this is a campus-wide, managed Active Directory
 instance. It is synchronized with Outlook 365.

 * **Outlook 365**: Microsoft's online office suite, it is a popular mail and calendar solution on campus. It is synchronized with Outlook 365.

 * **Sympa**: located at lists.ucdavis.edu, Sympa is an e-mail list system. It can be
 configured directly or use remote data sources for its membership lists. It is the
 recommended way to host a mailing list on campus.

 * **ServiceNow**: primarily used for support tickets, ServiceNow is a relatively
 recent addition to the UCD campus (~2015) and allows for multiple departments to escalate
 issues to each other.
