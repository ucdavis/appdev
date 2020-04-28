---
layout: "sdl"
title: "Define Security Requirements"
practice: "06"
description: "The SDL is typically thought of as assurance activities that help engineers implement “secure features”, in that the features are well engineered with respect to security."
icon: "define-security-requirements"
---
To achieve this, engineers will typically rely on security features, such as cryptography, authentication, logging, and others. In many cases, the selection or implementation of security features has proven to be so complicated that design or implementation choices are likely to result in vulnerabilities. Therefore, it’s crucially important that these are applied consistently and with a thorough understanding of the protection they provide.

During the software design phase, the following security components should be considered:
* Encryption
* Authentication
* Authorization
* Logging
* Legal, regulatory requirements
* Coding standards
* Known threats
* Disaster recovery
* Testability / Correctness
* Data protection, backup, and retention
* Service availability and reliability
* Vendor/upstream security practices and reliability
* Requirements specified in IS-3 or by the Information Security Office

Some of the above security components may be required as part of a software package’s IS-3 Protection or Availability levels.

Regardless of software development methodology, developers and development teams are encouraged to explicitly incorporate the above into their design phases, e.g. agile teams can require all user stories include discussion and documentation of any underlying security concerns and how the team intends to mitigate those as part of the architecture of the story.

In addition, developers are encouraged to consider how their designs may be compromised even after taking the above practices into account, and use any insights gathered to define their own security design practices to be consistently applied to all projects.

The need to consider security and privacy is a fundamental aspect of developing highly secure applications and systems and regardless of development methodology being used, security requirements must be continually updated to reflect changes in required functionality and changes to the threat landscape. Obviously, the optimal time to define the security requirements is during the initial design and planning stages as this allows development teams to integrate security in ways that minimize disruption. Factors that influence security requirements include (but are not limited to) the legal and industry requirements, internal standards and coding practices, review of previous incidents, and known threats. These requirements should be tracked through either a work-tracking system or through telemetry derived from the engineering pipeline.

Depending on the data and regulatory requirements for your unit, your applications may be subject to many types of security requirements. At a minimum, you should evaluate your application to ensure compliance with any applicable sections of IS-3 <https://policy.ucop.edu/doc/7000543/BFB-IS-3​>. The UC Davis Data Sensitivity Guide (<​https://cloud.ucdavis.edu/data-types-list​>) can also help developers identify the laws and regulations that apply to the types of data used by their application, but teams should also consult with subject matter experts. The National Institute of Standards and Technology (NIST) provides a large number of cybersecurity publications and standards <https://www.nist.gov/publications/search?term_node_tid_depth%5B%5D=248731​>.
