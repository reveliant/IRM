---
title: Identification
weight: 2
objective: Detect the incident, determine its scope, and involve the appropriate parties.
---
### Analyze the attack

- Understand the logical flow of the DDoS attack and identify the infrastructure components affected by it.
- Understand if you are the target of the attack or a collateral victim
- Review the load and log files of servers, routers, firewalls, applications, and other affected infrastructure.
- Identify what aspects of the DDoS traffic differentiate it from benign traffic
  - Source IP addresses, AS, etc
  - Destination ports
  - URLs
  - Protocols flags
  
  Network analysis tools can be used to review the traffic
  -> Tcpdump, Tshark, Snort, Argus, Ntop, Aguri, MRTG

- If possible, create a NIDS signature to focus to differentiate between benign and malicious traffic.

### Involve internal and external actors

- Contact your internal teams to learn about their visibility into the attack.
- Contact your ISP to ask for help. Be specific about the traffic you’d like to control:
  - Network blocks involved
  - Source IP addresses
  - Protocols
- Notify your company’s executive and legal teams.

### Check the background

- Find out whether the company received an extortion demand as a precursor to the attack.
- Search if anyone would have any interest into threatening your company
  - Competitors
  - Ideologically-motivated groups (hacktivists)
  - Former employees
