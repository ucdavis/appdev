---
layout: page
title: Recommended Practices
---

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

* **Backup & Disaster Recovery**: To be written.

* **Testing**: To be written.

* **Linting**: To be written.

* **Security scanning**: To be written.