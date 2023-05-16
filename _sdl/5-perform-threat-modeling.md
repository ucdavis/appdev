---
layout: "sdl"
title: "Perform Threat Modeling"
practice: "05"
description: "Threat modeling can be used to identify areas where applications need to be protected."
icon: "perform-threat-modeling"
---
Threat modeling can be applied at the component, application, or system level. It is a practice that allows development teams to consider, document, and (importantly) discuss the security implications of designs in the context of their planned operational environment and in a structured fashion.

Threat models typically start with an abstraction of the system, such as a data flow diagram or process flow diagram. From this understanding of the system, weaknesses in the system are identified. Potential threats are cataloged. The vulnerabilities are then prioritized for remediation.
Applying a structured approach to threat scenarios helps a team more effectively and less expensively identify security vulnerabilities, determine risks from those threats, and then make security feature selections and establish appropriate mitigations.

There are many established methods to perform threat modeling. A few well documented methods are listed below. There is quite a bit of flexibility in choosing a threat modeling technique and no one technique is ideal for every environment. One should choose the best technique for the system that is being modeled. For those unsure of where to start, STRIDE is a good approach to begin with since it is practical for many scenarios.

## STRIDE
The STRIDE methodology name serves as a mnemonic for security threats in six categories: spoofing, tampering, repudiation, information disclosure, denial of service, and elevation of privilege. The methodology involves four phases: diagram, identify threats, mitigate, and validate. STRIDE is a well established methodology produced by Microsoft. It is a good technique for both beginners and experts of threat modeling. STRIDE includes two variants called STRIDE-per-Element and STRIDE-per-Interaction which may be used to produce a stronger model. The four phases of STRIDE are summarized below.

## Diagram
Like many threat models, one starts with a data flow diagram which illustrates the assets involved and the data flow between them. One then identifies the trust boundaries, also referred to as the attack surface, between the assets for identifying possible threats.

## Identify Threats
Threat types are identified on each trust boundary. For example, spoofing and repudiation are two threat categories that are commonly identified for external entity element types. Knowing what threat categories commonly apply to an element type simplifies the process of identifying threats for that element. From the threat categories, one produces a specific list of threats to the system. For example, if spoofing is identified as a threat category for an identity provider, the threat may be potential credential stuffing. Once the threats are identified, they are ordered by severity so that they can be prioritized.

## Mitigate
Once a list of threats have been identified, one identifies mitigation strategies for each threat. For example, if the threat on a trust boundary is spoofing, a mitigation technique could be to require multi-factor authentication on that element. Mitigations would be prioritized and planned on a roadmap. Note that no system is without threats and it is impossible to mitigate all of them. The approach would be to address the most critical threats and the low hanging fruit first, going down the list by priority.

## Validate
The final phase in STRIDE is validation. In this phase, one ensures that the model is complete and accurate. Perhaps elements are missing from the data flow diagram or it is missing key interfaces. Have all the threats been identified? Have test cases been written for each threat? After identifying the missing components of the model, one goes back to the first phase, diagramming,​ to begin the modelling cycle again.

## PASTA
PASTA (Process for Attack Simulation and Threat Analysis) is a risk-centric threat modeling framework. It defines seven stages in threat modeling: define objectives, define technical scope, application decomposition, threat analysis, vulnerability and weaknesses analysis, attack modeling, and risk analysis.

## LINDDUN
LINDDUN is a mnemonic for linkability, identifiability, nonrepudiation, detectability, disclosure of information, unawareness, and noncompliance. LINDDUN has a stronger focus on privacy concerns and may be an appropriate modeling technique to use where privacy is more of a concern. Like the other techniques it provides clear steps to define the threats and mitigate them. The steps in LINDDUN include: define data flow diagram (DFD), map privacy threats to DFD elements, identify threat scenarios, prioritize threats, elicit mitigation strategies, and select privacy enhancing technologies (PETs). LINDDUN has a slightly higher learning curve than STRIDE so it may be preferable for beginner threat modelers to start with the STRIDE model.

## ATTACK TREES
Attack trees are an older and well established technique for threat modeling. This method works well as a supplement to other modeling techniques such as STRIDE, PASTA, or LINDDUN. They are often easier to produce. However, on their own, attack trees may not provide as complete of a methodology as some of the others. In this methodology, one starts with a root

node that represents a component that prompts the analysis, or a threat to the system. From the root node, subnodes are created that represent what can go wrong for that node. Additional subnodes describe in more detail how an attack may occur.
References
* <https://insights.sei.cmu.edu/sei_blog/2018/12/threat-modeling-12-available-methods.html>
* <https://www.amazon.com/Threat-Modeling-Designing-Adam-Shostack/dp/1118809998>
* <http://securesoftware.blogspot.com/2012/09/rebooting-software-security.html>
* <https://www.linddun.org>
