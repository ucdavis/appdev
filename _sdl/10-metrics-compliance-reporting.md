---
layout: "sdl"
title: "Define Metrics and Compliance Reporting"
practice: "10"
icon: "define-metrics-and-compliance-reporting"
---
It is essential to define the minimum acceptable levels of security quality and to hold
engineering teams accountable to meeting that criteria. Defining these early helps a team
understand risks associated with security issues, identify and fix security defects during
development, and apply the standards throughout the entire project. Setting a meaningful
bug bar involves clearly defining the severity thresholds of security vulnerabilities (for
example, all known vulnerabilities discovered with a “critical” or “important” severity rating
must be fixed with a specified time frame) and never relaxing it once it's been set.

In order to track key performance indicators (KPIs) and ensure security tasks are
completed, the work tracking mechanisms (ticketing or intake tool) used by an organization
should allow for security defects and security work items to be clearly labeled as security
and marked with their appropriate security severity. This allows for accurate tracking and
reporting of security work.

## Identifying Compliance Requirements
All developed applications should have a minimum baseline for security. Development
teams worldwide should be familiar with these security standards. However, there are many
layers of additional security requirements specific to application development at UC Davis.
These can include departmental and campus requirements, system-wide security
standards, federal and state laws, and environmental best practices. Navigating these
overlapping requirements can sometimes be challenging.

The first step in identifying the required security metrics for an application is to identify the
rules and regulations that govern it. UCOP has released a number of documents that can
help categorize rules that apply to applications based on the type of data that is used.
These include:
* [IS-3 Electronic Information Security Policy](https://policy.ucop.edu/doc/7000543/BFB-IS-3)
* [UC Protection Level Classification Guide](https://security.ucop.edu/files/documents/uc-protection-level-classification-guide.pdf)
* [UC Availability Level Classification Guide](https://security.ucop.edu/files/documents/uc-availability-level-classification-guide.pdf)

In addition, the Information Security Office maintains a Data Sensitivity Guide at
<https://cloud.ucdavis.edu/> that can help identify the applicable laws that apply to the various
data types. These laws should be reviewed carefully, including references to security
standards such as NIST.

Finally, the development team should coordinate with the appropriate compliance officer,
cybersecurity executive, or Unit Information Security Lead to determine if there are special
rules, regulations, or best practices required for the application or the data involved. If the
application is using data owned by another department or agency it is appropriate and
recommended that the development team review all security and privacy controls with the
data owner.

## Defining Security Metrics
The applicable IS-3 and NIST standards will describe the security controls required. Any
additional mandated compliance needs will add to these controls. In some cases the
controls themselves will have built in metrics (for example a defined complexity level for
passwords). In other cases, the controls will need specific metrics defined in order to be
properly implemented. These metrics can vary wildly depending on the available resources,
technical skills, and perceived risk.

For example, a metric might describe the mandated OS patching level for a data
management tool. Those patching requirements would be based on a thorough review of
IS-3 and other security policies. For example P3 or P4 level data requiring patching every
90 days (or have compensating controls applied) IS-3 §12.6. Development teams should
work with their data owners, the Unit Information Security Lead, and their internal security
specialists to review the applicable security policies and regulations.

These metrics should be recorded with the security controls documentation, It may also be
helpful to record the decision making process and the factors that were considered when
defining the metrics. This will make future reviews easier.

Here’s a non-exhaustive list of some example security metrics:
* Critical and high level vulnerabilities found by the campus Security Center scans
must be remediated within 7 days
* Medium level vulnerabilities found by the campus Security Center scans must be
remediated within 30 days
* Production servers must be patched with the latest critical updates within 7 days
* Production servers must be patched with the latest security updates within 45 days
* Permission for off-boarded staff must be revoked within 24 hours
* Application-level permissions must be reviewed every 6 months
* Database- and server-level permissions must be reviewed annually
* Application code must be reviewed by at least 2 developers prior to deployment
* Application logs must be reviewed every two months
* Third party libraries imported into applications must be reviewed at least every 30
days for vulnerabilities.

## Monitoring and Reporting
Security metrics are only valuable when they are recorded and reviewed. Development
teams should implement a mechanism for recording both the metrics standards themselves
and the validation results that show the metrics are being met. For example, if a metric has
been defined that mandates an audit of application permissions should be performed every
six months, there should be a record of those audits describing:
* The dates and times
* Who performed the audit
* The findings (if any)
* The remediations (if any)

Where feasible, automated results will be desired. Removing the opportunity for human
error or forgetfulness is beneficial for a secure system. The development team’s incident
response plan should describe the reporting paths for any unusual or concerning findings,
however even negative findings or innocuous results may be reportable depending on the
rules and regulations attached to the application.

Executive level reports are useful for reporting high level compliance metrics to the Unit
Head, the UCD ISO, or auditor. These are reports that provide general statistics on
compliance without getting into the weeds of every detail. This is useful to those who have a
lot of reports and documents to go through. For example, an executive level report may say
that all critical severity vulnerabilities were remediated < 7 days for the last year, all high
severity were remediated within 30 days, etc. It may also report on how many vulnerabilities
are currently present.