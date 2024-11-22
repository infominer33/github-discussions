---
title: "acapy/issue/2998: Regression: Error if anoncreds extra is not installed"
date: 2024-05-29 15:37:28 +0000
author: dbluhm
categories: ["OWF"]
tags: ["acapy"]
permalink: /acapy/issue/2998/
comments_file: OWF-acapy-issue-2998_comments
---

[_https://github.com/openwallet-foundation/acapy/issues/2998_](https://github.com/openwallet-foundation/acapy/issues/2998)

I happened to discover that not installing the anoncreds extra causes a failure on startup of ACA-Py:

```
holder_1  | Traceback (most recent call last):
holder_1  |   File "/usr/src/app/.venv/bin/aca-py", line 8, in <module>
holder_1  |     sys.exit(script_main())
holder_1  |   File "/usr/src/app/.venv/lib/python3.10/site-packages/aries_cloudagent/__main__.py", line 69, in script_main
holder_1  |     main(sys.argv)
holder_1  |   File "/usr/src/app/.venv/lib/python3.10/site-packages/aries_cloudagent/__main__.py", line 75, in main
holder_1  |     run(args)
holder_1  |   File "/usr/src/app/.venv/lib/python3.10/site-packages/aries_cloudagent/__main__.py", line 64, in run
holder_1  |     run_command(command, args)
holder_1  |   File "/usr/src/app/.venv/lib/python3.10/site-packages/aries_cloudagent/commands/__init__.py", line 37, in run_command
holder_1  |     module = load_command(command) or load_command("help")
holder_1  |   File "/usr/src/app/.venv/lib/python3.10/site-packages/aries_cloudagent/commands/__init__.py", line 32, in load_command
holder_1  |     return import_module(module_path)
holder_1  |   File "/usr/local/lib/python3.10/importlib/__init__.py", line 126, in import_module
holder_1  |     return _bootstrap._gcd_import(name[level:], package, level)
holder_1  |   File "<frozen importlib._bootstrap>", line 1050, in _gcd_import
holder_1  |   File "<frozen importlib._bootstrap>", line 1027, in _find_and_load
holder_1  |   File "<frozen importlib._bootstrap>", line 1006, in _find_and_load_unlocked
holder_1  |   File "<frozen importlib._bootstrap>", line 688, in _load_unlocked
holder_1  |   File "<frozen importlib._bootstrap_external>", line 883, in exec_module
holder_1  |   File "<frozen importlib._bootstrap>", line 241, in _call_with_frames_removed
holder_1  |   File "/usr/src/app/.venv/lib/python3.10/site-packages/aries_cloudagent/commands/start.py", line 16, in <module>
holder_1  |     from ..core.conductor import Conductor
holder_1  |   File "/usr/src/app/.venv/lib/python3.10/site-packages/aries_cloudagent/core/conductor.py", line 20, in <module>
holder_1  |     from ..admin.server import AdminResponder, AdminServer
holder_1  |   File "/usr/src/app/.venv/lib/python3.10/site-packages/aries_cloudagent/admin/server.py", line 39, in <module>
holder_1  |     from ..wallet.anoncreds_upgrade import check_upgrade_completion_loop
holder_1  |   File "/usr/src/app/.venv/lib/python3.10/site-packages/aries_cloudagent/wallet/anoncreds_upgrade.py", line 8, in <module>
holder_1  |     from anoncreds import (
holder_1  | ModuleNotFoundError: No module named 'anoncreds'
```

@jamshale This looks related to the upgrade endpoints -- I think we need to have a conditional import to ensure we can use ACA-Py without the anoncreds extra installed