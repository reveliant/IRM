---
title: Containment
weight: 3
---
- Backup all important data from the compromised machine, if possible using a bit-by-bit physical copy of the whole hard disk on an external support. Also make a copy of the memory (RAM) of the system, which will be investigated if necessary.

If the machine is not considered critical for the company and can be disconnected, shut the machine down the hard way, removing its power plug. If it is a laptop with a battery on, just push the “off” button for some seconds until the computer switches off.

Offline investigations should be started right away if the identification step didn’t give any result, but the system is still suspected of being compromised.

**Try to find evidences of every action of the hacker: (using forensic tools like Sleuth Kit/Autopsy for example)**

- **Find all files used by the attacker**, including deleted files and see what has been done with them or at least their functionality to evaluate the threat.
- **Check all files accessed recently**.
- **Check log files**.
- More generally, try to **find how the attacker got into the system**. All leads should be considered. If no computer proof of the intrusion is found, never forget it could come from an insider.
- Apply fixes when applicable, to prevent the same kind of intrusion, in case the attacker used a known fixed vulnerability
