---
title: Containment
weight: 3
objective: Mitigate the attack’s effects on the targeted environment.
---
- **Backup all data** stored on the web server for forensic purposes and evidence collecting. The best practice here if applicable is to make a complete bit-by-bit copy of the hard-disk containing the web server. This will be helpful to recover deleted files.
- **Check your network architecture map. Verify that the vulnerability exploited by the attacker is not located somewhere else** :

  - Check the system on which the web server is running,
  - Check other services running on that machine,
  - Check the connections to other systems, which might be compromised.

If the source of the attack is another system on the network, disconnect it if possible physically and investigate on it.

**Try to find evidences of every action of the attacker**:

- **Find out how the attacker got into the system in the first place and fix it**:

  - Web component vulnerability allowing write access: fix the vulnerability by applying editor’s fix.
  - Open public folder: fix the bug.
  - SQL weakness allowing injection: correct the code.
  - Mashup components: cut mashup feed.
  - Administrative modification by physical access: modify the access rights.

- **If required (complex issue and very important web server), deploy a temporary web server**, up to date with its applications. It should offer the same content than the compromised web server or at least show another legitimate content such as “Temporary unavailable”. The best is to display a temporary static content, containing only HTML code. This prevents another infection in case the attacker has used vulnerability in the legitimate PHP/ASP/CGI/PL/etc. code.
