---
title: Identification
weight: 2
---
### General signs of ransomware presence

Several leads might hint that the system could be compromised by ransomware:

- Odd professional emails (often masquerading as invoices) containing attachments are being received
- A ransom message explaining that the documents have been encrypted and asking for money is displayed on user’s desktop

  <figure class="figure text-center w-100">
  <img class="figure-img" width="360" src="cryptowall-ransom-message.jpg" alt="Cryptowall ransome message"/>
  <figcaption class="figure-caption">Figure 1 - Cryptowall ransom message</figcaption>
  </figure>

- People are complaining about their files not being available or corrupted on their computers or their network shares with unusual extensions (.abc, .xyz, .aaa, etc..).
- Numerous files are being modified in a very short period of time on the network shares

### Host based identification

- Look for unusual executable binaries in users’ profiles (`%ALLUSERSPROFILE%` or `%APPDATA%`) and `%SystemDrive%`
- Look for the aforementioned extensions or ransom notes
- Capture a memory image of the computer (if possible)
- Look for unusual processes
- Look for unusual email attachment patterns
- Look for unusual network or web browsing activities; especially connections to Tor or I2P IP, Tor gateways (tor2web, etc) or Bitcoin payment websites

### Network based identification

- Look for connection patterns to Exploit Kits
- Look for connection patterns to ransomware C&C
- Look for unusual network or web browsing activities; especially connections to Tor or I2P IP, Tor gateways (tor2web, etc) or Bitcoin payment websites
- Look for unusual email attachment patterns
