---
title: Containment
weight: 3
---

The following actions should be performed and monitored by the crisis management cell:

1. Disconnect the infected area from the Internet.
2. Isolate the infected area. Disconnect it from any network.
3. If business-critical traffic cannot be disconnected, allow it after ensuring that it cannot be an infection vector or find validated circumventions techniques.
4. Neutralize the propagation vectors. A propagation vector can be anything from network traffic to software flaw. Relevant countermeasures have to be applied (patch, traffic blocking, disable devices, etc.)
   For example, the following techniques can be used:

   - Patch deployment tools (WSUS),
   - Windows GPO,
   - Firewall rules,
   - Operational procedures.

5. Repeat steps 2 to 4 on each sub-area of the infected area until the worm stops spreading. If possible, monitor the infection using analysis tools (antivirus console, server logs, support calls).

The spreading of the worm must be monitored.

### Mobile devices

Make sure that no laptop, PDA or mobile storage can be used as a propagation vector by the worm. If possible, block all their connections.

Ask end-users to follow directives precisely.

At the end of this step, the infection should be contained.
