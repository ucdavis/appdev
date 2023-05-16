---
layout: "sdl"
title: "Manage the Security Risk of Using Third-Party Components"
practice: "11"
icon: "manage-the-security-risk-of-third-party-components"
---

Today, the vast majority of software projects are built using third-party components (both
commercial and open source). When selecting third-party components to use, it’s important
to understand the impact that a security vulnerability in them could have to the security of
the larger system into which they are integrated. Having an accurate inventory of third-party
components and a plan to respond when new vulnerabilities are discovered will go a long
way toward mitigating this risk, but additional validation should be considered, depending on
your organization's risk appetite, the type of components used, and potential impact of a
security vulnerability.

Component Security Management consists of three important processes:

## Inventory Components
The first step of properly managing the use of third-party components is to understand
which components are in use. Even in small organizations, this usually requires automation.
Fortunately, modern agile development practices already rely heavily on automated tooling,
and so are easily adapted to include capabilities in this area.

There are many tools available in this space, including open source tools like [NPM Audit](https://docs.npmjs.com/cli/audit),
[OWASP Dependency Check](https://owasp.org/www-project-dependency-check/), and GitHub’s [Dependabot](https://dependabot.com/). We aren't specifically endorsing
any specific tool or service here, as they each have different strengths and weaknesses;
perform a thorough evaluation before deciding on an inventory solution.

Inventory generation should take place at a natural point in your development lifecycle, such
as during pull-request validation or branch merging, with the inventory results being stored
centrally and accessible to appropriate personnel. Be sure to include enough metadata in
the inventory to identify the application, source repository, version/commit, and other details
from which the inventory was derived.

## Perform Security Analysis
Before incorporating third-party components, they should be validated to ensure they are
free of security vulnerabilities within a reasonable level of effort.

It is critical for every developer to check for public vulnerabilities—ensure the components
do not contain publicly-known vulnerabilities, such as those with reported CVEs or with
vulnerabilities described in other public resources. Additionally, look for projects that are
actively developed and have thriving communities to increase the probability that security
concerns are addressed in a timely manner.

GitHub can perform automated security alerts for third-party components. When utilizing
GitHub for source control, these should always be turned on, and any vulnerability that is
labeled “high” or “critical” should be remediated as soon as possible.
<https://help.github.com/en/articles/about-security-alerts-for-vulnerable-dependencies>

## Keep Components Up to Date
One of the most effective ways to manage security risk related to the use of open source is
to keep components up to date, even in the absence of known vulnerabilities. This can be a
security benefit because security vulnerabilities are often fixed without explicit public
disclosure, and while the engineering cost of doing this isn’t free, benefits extend beyond
security (such as engineering agility, taking advantage of new features and bug fixes).