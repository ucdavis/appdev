---
layout: sdl
practice: "3"
title: Perform Application Security Testing
description: Application Security Testing (AST) encompases a broad range of scanning methodologies for finding vulnerabilities within applications.
icon: perform-application-security-testing
---
In general, this includes Static AST (SAST), Dynamic AST (DAST), Interactive AST (IAST), Mobile AST (MAST), and Software Composition Analysis (SCA). AST may also include other methodologies as the practice evolves over time.

##AST
AST provides the ability to scan applications for vulnerabilities at various stages of the SDLC. There is no one size fits all solution. Development teams should consider their development methodology (e.g. agile, waterfall), the frequency of deployments, and the technologies used (e.g. mobile devices, open source software) to decide on the proper AST tool(s) and scanning frequency. For example, a department that uses open source libraries should use an appropriate SCA tool to scan for vulnerabilities in open source libraries. A department that develops mobile apps should use an appropriate MAST tool. IAST may not be effective in an SDLC that does not yet incorporate functional or end-to-end testing.
The use of AST should be incorporated into the department’s SDLC to ensure that scanning and remediation of findings are performed before new code is deployed to production or other public facing environment. Below are summaries of common AST methods.

##SAST
SAST ​technology analyzes an application's source, bytecode or binary code for security vulnerabilities typically at the programming and/or testing software life cycle (SLC) phases. Analyzing the source code prior to compilation provides a highly scalable method of security code review and helps ensure that secure coding policies are being followed. SAST is typically integrated into the commit pipeline to identify vulnerabilities each time the software is built or packaged. However, some offerings integrate into the developer environment to spot certain flaws such as the existence of unsafe or other banned functions and replace those with safer alternatives as the developer is actively coding.

##DAST
DAST ​technology analyzes applications in their dynamic, running state during testing or operational phases. It simulates attacks against an application (typically web-enabled applications and services), analyzes the application's reactions and, thus, determines whether it is vulnerable. DAST is performed on the running application, making it suitable for scanning an application after it has been deployed to a development, QA, or production environment.

##IAST
IAST technology combines elements of SAST and DAST simultaneously. It is typically implemented as an agent in the test runtime environment (for example, instrumenting the Java Virtual Machine [JVM] or .NET CLR) that observes operation or attacks and identifies vulnerabilities. IAST requires attack simulations from outside sources in order to detect vulnerabilities. IAST may be used in coordination with a DAST tool to crawl a web application and simulate attacks in a deployed application. This is referred to as Active IAST. Passive IAST can be used earlier in the SDLC by leveraging functional tests or end-to-end tests to trigger IAST for collecting security findings during application testing.

##MAST
Mobile AST performs SAST, DAST, IAST and/or behavioral analysis on byte or binary code to identify vulnerabilities in mobile applications.

##SCA
SCA identifies open-source and third-party libraries in applications and their known security vulnerabilities. SCA typically provides recommendations for upgrading to specific component versions.
Note that the IS-3 policy details specific requirements for scanning resources classified at protection level 3 or higher, or availability level 3 or higher. Please refer to Section 12.6 of the IS-3 policy for these requirements and additional scanning requirements.
The UC Davis ISO is providing AST capabilities via its application security program. This includes an ​enterprise license of X​ for departments that onboard to the program. Although this program should satisfy the application scanning requirements of most departments, UC Davis departments represent a diverse range of missions, technologies, and methodologies. Each department should be appropriately evaluated for proper AST tool selection.
