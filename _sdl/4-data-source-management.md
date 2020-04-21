---
layout: "sdl"
title: "Data Source Management"
practice: "4"
description: "Application data may be consumed from and published to many data sources including dedicated on-premises databases, third-party cloud-hosted web services, and more."
icon: "data-source-management"
---
Data source management is complementary to the concerns to data security, including protection of access credentials, accessing data sources in a secure fashion, verifying the identity of the third-party data source, and ensuring the data source is highly available.

## Data Source Secrets Management
Protecting the credentials used to access data sources is critical. Even if an application’s code is secure, attacks can still access and manipulate data if data source credentials are not well-protected.

Data source credentials should be stored securely using high-quality secret managers or keychains. Credentials owned by an organization should be stored securely using a service such as LastPass or Thycotic.

Data source credentials should never be included in the source code nor compiled artifacts. Secrets required by an application should be provided by the operating environment utilizing a known secure method appropriate to the programming language, framework, and hosting solution. Examples include container environment variables, application server arguments, or separate, on-disk credentials which are loaded at run-time.

## SSL for Privacy and Identity Verification
All data sources, whether traditional web servers, directory servers, web services, or others should be accessed using SSL.

SSL usage should be configured to both ensure data is encrypted in transit and that the identity of the data source is verified to avoid man-in-the-middle attacks such as hostile database servers via DNS poisoning.

Invalid or expired SSL certificates should not be trusted.

## Data Availability
When possible, data sources should be accessed using approved CNAMEs or cluster hostnames, not using the specific hostname of a node in the data source cluster. This ensures the benefits of a clustered database are properly realized and helps to ensure data source availability.
