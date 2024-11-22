---
title: "acapy/pr/3332: :sparkles: Add TRACE log level and improve logging in core components"
date: 2024-11-07 15:18:36 +0000
author: ff137
categories: ["OWF"]
tags: ["acapy"]
permalink: /acapy/pr/3332/
comments_file: OWF-acapy-pr-3332_comments
---

[_https://github.com/openwallet-foundation/acapy/pull/3332_](https://github.com/openwallet-foundation/acapy/pull/3332)

:construction: WIP

List of changes:
- Implements a new, custom log level called TRACE (not included in python logger by default)
- Expands logging within core and config components: Conductor, PluginRegistry, and DefaultContextBuilder
- Replaces (almost) all print statements with info logs
- General improvement of some code for readability / maintainability (mainly in the PluginRegistry)
- Includes unit test coverage 

Comparison of start up logs before and after to be included.

Partially resolves #3202