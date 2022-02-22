---
title: Containment
weight: 3
---
If the machine is considered critical for your company’s business activity and can’t be disconnected, backup all important data in case the hacker notices you’re investigating and starts deleting files. Also make a copy of the system’s memory for further analysis. (use tools such as Memoryze,win32dd etc.)

If the machine is not considered critical for your company and can be disconnected, shut the machine down the hard way, removing its power plug. If it is a laptop with a battery on, just push the “off” button for some seconds until the computer switches off.

Offline investigations should be started right away if the live analysis didn’t give any result, but the system should still be considered compromised.

**Make a physical copy** (bit by bit) of the whole hard disk on an external storage support, using *EnCase*, *X-Ways*, or similar forensic tool (`dd`, `ddrescue` etc.).

**Try to find evidences of every action of the hacker:**

- **Find all files used by the attacker**, including deleted files (use your forensic tools) and see what has been done with it or at least their functionality, in order to evaluate the threat.
- **Check all files accessed recently**.
- Inspect network shares to see if the malware has spread through it.
- More generally, try to **find how the attacker got into the system**. All leads should be considered. If no computer proof of the intrusion is found, never forget it could come from a physical access or a complicity/stealing of information from an employee.
- Apply fixes when applicable (operating system and applications), in case the attacker used a known vulnerability
