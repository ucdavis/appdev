---
layout: page_nosidebar
permalink: /orientation/index.html
title: Getting Started
description: 'Beginner documentation for new developers to get up-to-speed on what they should know working at UC Davis. 
It is meant to shortcut to the type
of knowledge one might have had they had been working for the University for a decade or two.'
---

This document tries to accomplish this in a few different ways: describing
the types of developers and "development shops" that exist on campus,
explaining how they do and sometimes don't work together, and answering
common questions about infrastructure such as: Where is dataset X stored? How can I access
it? Where should I be hosting applications? What's the best way to query the data I need to write my application?

If you have any corrections, ideas, or suggestions for this document, please
don't hesitate to get in touch.

{% for post in site.orientation %}
* [{{post.title}}]({{post.url}})
{%- endfor -%}