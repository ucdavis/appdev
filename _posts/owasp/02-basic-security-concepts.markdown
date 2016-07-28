---
layout: article
title: "Basic Security Concepts"
description: "Basic security concepts, terms, and definitions."
date: 2016-07-25
category: "owasp"
image:
breadcrumb: Owasp
---

# Basic Security Concepts
#### 25 July 2016

## The CIA Triad
- **C**onfidentiality - the state of being secret
- **I**ntegrity - the state of being unmodified by an unauthorized entity
- **A**vailability - the state of being available to authorized individuals

One or more of the CIA triad may pertain to your data, depending on the specific data you deal with. For example, financial and health data require all three (all three items share equal importance). 

## Definitions and Terminology
- **Vulnerability** - any exploitable weakness (e.g. a building not built to code collapses after an earthquake; the failure to build appropriately becomes a vulnerability a natural occurrence exploits)
- **Threat** (or **threat agent**) - an entity able to detect, identify, and exploit a vulnerability
- **Impact** - the extent of the effect a threat poses to a security decision; the security professional must gauge impact to determine the extent of defenses to mount
- **Probability** - the chance your application will undergo a specific attack; the security professional must gauge the probability of a given attack to determine appropriate defensive measures 
- **Threat Modeling** - a secure approach to developing applications, taking into account vulnerabilities, threats, impact, and probability
 
### Vulnerabilities
#### Architecture
Central to the design of the system, these make up some of the most challenging security flaws to correct.
Up until 2009, the BASE24 Credit Switch (for transferring credit and debit card data) only provided for a four-character password without any password lockout. 

Windows 95/98 would allow users to create an account if the user could not remember his/her password.

#### Development
We can fix these flaws if we take the time to refactor components; the difficulty of correcting a given flaw depends on the extent. 

Often this includes failure to validate input, leading to cross-site scripting and SQL injection.

#### Implementation & Deployment
Generally (and comparatively) speaking, implementation and deployment flaws have easy fixes.

Leaving default administrative usernames and passwords. 

Running services you do not understand.

#### Maintenance and Configuration
On occasion, these become the toughest flaws to correct. Many times you do not know and cannot estimate the side effects updating a given library or component results in. Service downtime may mean lost jobs or have a ripple effect on the bottom line. As a system scales up, so do the problems with maintenance and configuration.

Heartbleed and OpenSSL.

#### Common Flaws
- Application Architects fail to design an application to generate security logs (Architecture Vulnerability)
- Developers fail to add in user input validation (Development Vulnerability)
- System Administrator or Developer deploys the application (or, more often, its dependencies) with default credentials (Implementation & Deployment Vulnerability)
- System Administrator does not update the server or application(s) (Maintenance and Configuration Vulnerability)

### Threats
**Threat Actor** - the attacking entity (e.g., hackers, malware, etc.)
**Threat Access** - how the actor reaches the system; physically or remotely (remote is more serious)? 
**Threat Outcome** - which CIA Triad item does the threat fall under?  

### Risks
We define _risks_ as the product of vulnerability, impact, probability, and threat outcome.

The Four T's of Risk Management (or, how to manage risk):
1. **Treat**: mitigating the threat (e.g., block injection attacks)
2. **Terminate**: remove the feature or service, or hand it over to a third party (e.g., process credit card data through Stripe)
3. **Transfer**: insure your risk through an insurance agency
4. **Tolerate**: when you can neither fix nor terminate the risk, you may decide to simply accept it (e.g., 100,000,000 credit cards in a database without encryption)
 
### Controls
How can we alleviate risk?

#### Preventive Controls
Developers and security professionals overuse and overly trust preventive measures. Preventive controls aim to block an attacker or "keep the bad guys out," but overwhelmingly fail against issues like ransomware.

Examples include passwords and cryptography.

#### Detective Controls
Developers overwhelmingly fail to implement these controls. System Administrators often provide detective tools at their levels, but many applications fail to log what someone does that leads to a breach.   

Examples include logs, security cameras, and IDS.

#### Corrective Controls
Actions taken to rectify or stop an attack.

Examples include backups and system audits.

#### Defense-in-Depth
We can treat defense like an onion, avoiding a single point of failure.

1. Physical Security
    a. Security Guards
    b. CCTV
2. Network Security
    a. IDS
    b. Firewall
3. Operating System Security
    a. OS Hardening
    b. File Integrity Checks
4. Application and Database Security
    a. Web Application Firewall
    b. Input Validation

_**We cannot avoid attacks; we aim to dissuade attackers so they move onto a softer target.**_
