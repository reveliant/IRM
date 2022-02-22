---
title: Identification
weight: 2
objective: Detect the incident, determine its scope, and involve the appropriate parties.
---
Usual channels of detection are:

- Webpage monitoring: The content of a web page has been altered. The new content is either very discreet (an “iframe” injection for example) or obvious (*“You have been 0wn3d by xxx”*)
- User: users call or notification from employees about problems they noticed while browsing the website.
- Security checks with tools such as Google SafeBrowsing

Verify the defacement and detect its origin:

- Check files with static content (in particular, check the modification dates, hash signature).
- Check mashup content providers.
- Check link presents in the web page (src, meta, css, script, …).
- Check log files.
- Scan the databases for malicious content.

**The source code of the suspicious page must be analysed carefully** to identify the problem clearly. In particular, **be sure the problem is on a web server belonging to the company** and not on a web content located outside your infrastructure, like commercial banners from a third party.
