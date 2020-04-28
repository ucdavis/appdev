---
layout: "sdl"
title: "Implement a code review process"
practice: "12"
icon: "code-review"
---
Documentation, policies, and controls are most effective if they are consistently
implemented and reviewed. As code and configurations change it is understandable that
developers and engineers might forget or misunderstand security requirements. Time
pressures or other stress factors may encourage short cuts or bad practices. Developing a
system that provides an opportunity for multiple people to evaluate and examine changes
prior to deployment can mitigate this risk. The best process review implementations will be
mandatory, auditable, and intrinsically embedded in the development lifecycle.

## Security Code Review Process
A security code review process ensures that code security controls are in place by using the
inspection of another software developer, typically a senior developer.

Security code reviews are often technology-assisted processes. A version control system
such as GitHub or BitBucket can implement controls requiring code entering a production
system receive explicit approval from one or more teammates.

The security code review process is typically performed as a continuous process throughout
the development phase of the software lifecycle.

## Static Analysis vs. Manual Analysis
Static application security testing (SAST) tools can be helpful in quickly identifying potential
security vulnerabilities. They are not, however, a replacement for manual analysis. SAST
tools often requiring configuration to identify portions of code and may identify a large
number of false positives. Only a human can fully understand the context of a particular
vulnerability to understand the severity and urgency of potential security flaws.

It is important to use SAST tools as an aid in a manual analysis process, not as a
replacement for one.

# Appendix A: Secure Software Development Practices
## Utilize Version Control
Store code in a source control system. Tag/label all production code releases so they can
be referenced and extracted at any time. Externalize all configuration secrets outside of
source control so your code repository does not contain private information.

## Use a Secrets Manager to External Sensitive Configuration
Certificates, passwords, and other sensitive materials are needed when a software
application is deployed. By using a Secrets Manager, these materials can be kept out of
potentially insecure locations such as the source code itself, operating system environment
variables, or plain-text files on the deployment system.

The particular practices used will vary from technology to technology, but one should be
able to deploy and run an application where all secrets are wired in securely.

This practice also supports separating out secrets between production, test, and
development environments, allowing the number of individuals with access to privileged
information to be kept at a minimum.

[SRK: Proposal for different sections within this secure software dev practices section,
additions by CMT]
* Testing (incl. unit tests)
* Continuous Integration (stretch goal?)
* Logging
* Secure Development (OWASP 10)
* Authentication?
* Deployment
* Archiving releases
* Secrets Management
* Automated dependency vulnerability scans