---
title: "linked-vp/issue/51: NGrok setup for local use with indy tails server"
date: 2024-02-29 08:54:34 +0000
author: loneil
categories: ["DIF"]
tags: ["linked-vp"]
permalink: /linked-vp/issue/51/
comments_file: DIF-linked-vp-issue-51_comments
excerpt: >
  1. The AI summaries need to be vetted/reviewed afterwards to make sure they capture the specific actual messages/nuances expressed in the meetings.  2. PLEASE make sure you continue to record and curate the recordings.  Some of the other DID WGs don't do this and a lot is lost - particularly if the minutes don't have a lot of fidelity.  Cheers
---
Using the startup instructions in:
https://github.com/hyperledger/aries-endorser-service?tab=readme-ov-file#running-locally

won't really work as-is any more as Indy Tails Server needs the ngrok auth token as well. And if you use the same auth token in the 2 contexts 
1. Indy Tails Server
2. Endorser Service

You will get the issue about simultaneous ngrok agent sessions

```
from docker-ngrok-endorser-agent container:
2024-02-16 16:16:45 ERROR:  authentication failed: Your account is limited to 1 simultaneous ngrok agent session.
2024-02-16 16:16:45 ERROR:  You can run multiple tunnels on a single agent session using a configuration file.
2024-02-16 16:16:45 ERROR:  To learn more, see https://ngrok.com/docs/secure-tunnels/ngrok-agent/reference/config/
2024-02-16 16:16:45 ERROR:  
2024-02-16 16:16:45 ERROR:  Active ngrok agent sessions in region 'us-cal-1':
2024-02-16 16:16:45 ERROR:    - ts_2cTI2njhg4tmt7Qe1cltNsx3kxT (23.16.82.223)
2024-02-16 16:16:45 ERROR:  
2024-02-16 16:16:45 ERROR:  ERR_NGROK_108
2024-02-16 16:16:45 ERROR:
```

Not sure if we could adjust to have one environment that shares it, or at least need to adjust documentation.