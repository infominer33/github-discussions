---
title: "acapy/issue/3353: ACA-Py failing to start, gives KeyError: 'pattern'"
date: 2024-11-25 15:25:18 +0000
author: nodlesh
categories: ["OWF"]
tags: ["acapy"]
permalink: /acapy/issue/3353/
comments_file: OWF-acapy-issue-3353_comments
excerpt: >
  The default is the dev universal resolver. So it might be expected to have breaking changes. It's an easy update in acapy. Creating a PR.
---
ACA-py started failing to start in the Interop Test Pipeline over the weekend. This is the error. The pipeline pull from main to build acapy. 
```
2024-11-25 15:13:18,787 acapy_agent.core.plugin_registry ERROR Module doesn't exist: redis_events.v1_0.redis_queue.events
2024-11-25 15:13:19,438 acapy_agent.commands.start ERROR Exception during startup:
Traceback (most recent call last):
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/commands/start.py", line 72, in init
    await startup
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/commands/start.py", line 28, in start_app
    await conductor.setup()
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/core/conductor.py", line 128, in setup
    context = await self.context_builder.build_context()
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/config/default_context.py", line 78, in build_context
    await self.load_plugins(context)
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/config/default_context.py", line 183, in load_plugins
    await plugin_registry.init_context(context)
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/core/plugin_registry.py", line 207, in init_context
    await plugin.setup(context)
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/resolver/__init__.py", line 62, in setup
    await universal_resolver.setup(context)
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/resolver/default/universal.py", line 66, in setup
    supported_did_regex = await self._get_supported_did_regex()
                          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/resolver/default/universal.py", line 115, in _get_supported_did_regex
    return _compile_supported_did_regex(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/resolver/default/universal.py", line 24, in _compile_supported_did_regex
    for pattern in patterns
                   ^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/acapy_agent/resolver/default/universal.py", line 116, in <genexpr>
    driver["http"]["pattern"] for driver in props.values()
    ~~~~~~~~~~~~~~^^^^^^^^^^^
KeyError: 'pattern'

Shutting down
```