---
title: Containment
weight: 3
objective: Mitigate the attack effects on the neighbouring IT resources.
---
If the issue is considered as strategic (sensitive resources access), a specific crisis management cell should be activated.

Depending on the criticality of the impacted resources, the following steps can be performed and monitored:

- Disconnect the compromised area from the network.
- Isolate the source of the attack. Disconnect the affected computer(s) in order to perform further investigation.
- Find acceptable mitigation measures for the business-critical traffic in agreement with the business line managers.
- Terminate unwanted connections or processes on affected machines.
- Use firewall/IPS rules to block the attack.
- Use IDS rules to match with this malicious behaviour and inform technical staff on new events.
- Apply ad hoc actions in case of strategic issue:
  - Block exfiltration destination or remote location on Internet filters ;
  - Restrict strategic file servers to reject connections from the compromised computer;
  - Select what kind of files can be lost / stolen and restrict the access for confidential files;
  - Create fake documents with watermarking that could be use as a proof of theft;
  - Notify targeted business users about what must be done and what is forbidden;
  - Configure logging capabilities in verbose mode on targeted environment and store them in a remote secure server.
