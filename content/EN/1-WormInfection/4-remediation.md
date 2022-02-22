---
title: Remediation
weight: 4
---

### Identify

Identify tools and remediation methods.
The following resources should be considered:

- Vendor fixes (Microsoft, Oracle, etc.)
- Antivirus signature database
- External support contacts
- Security websites

Define a disinfection process. The process has to be validated by an external structure, like your CERT for example.

### Test

Test the disinfection process and make sure that it properly works without damaging any service.

### Deploy

Deploy the disinfection tools. Several options can be used:

- Windows WSUS
- GPO
- Antivirus signature deployment
- Manual disinfection

**Warning**: some worms can block some of the remediation deployment methods. If so, a workaround has to be found.

Remediation progress should be monitored by the crisis cell.
