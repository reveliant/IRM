---
title: Recovery
weight: 5
---
No matter how far the hacker has gone into the system and the knowledge you might have about the compromission, as long as the system has been penetrated, the best practice is **to reinstall the system completely and apply all security fixes**.

In case this solution can’t be applied, you should:

- Change all the system’s accounts passwords, and make your users do so in a secure way: they should use passwords with upper/lower case, special characters, numbers, and at least be 7 characters long.
- Check the integrity of the whole data stored on the system, using MD5 hashes.
- Restore all binaries which could have been changed (Example: `/bin/su`)
