# NETWORKWALKS--GISELLE-B084-WK2-PM1-and-PM5-CYBERSECURITY-LAB-FOOTPRINTING-and-ZENMAP
This is a repository for networkwalks cybersecurity internship showing my work on Footprinting and Zenmap
# NetworkWalks Week 2 Cybersecurity Lab

* **Student:** Giselle Coutinho
* **Batch:** B084
* **Week:** 2

---

## Project Scope
This repository contains the Week 2 practical work completed for the Networkwalks Cybersecurity & Ethical Hacking internship program.

The Week 2 requirement is one elective module + both essential projects. This submission uses:

| Module | Description | Status |
| :--- | :--- | :--- |
| **W2-PM1** | Footprinting with multiple Kali tools | Completed |
| **W2-PM5** | Zenmap based Network Scanning | Completed |
| **W2-PM-FINAL** | Detailed Penetration Testing Report | Completed |

*Note: PM2 (GHDB), PM3 (Maltego), and PM4 (theHarvester) are elective alternatives and are therefore not required for this submission.*

---

## W2-PM1 — Footprinting
Six Kali Linux tools were used against the authorized Networkwalks target (`networkwalks.com`):
1. WHOIS
2. WhatWeb
3. Nslookup
4. Curl
5. Wafw00f
6. DNSRecon

The exercise documented domain registration information, DNS resolution, web technologies, HTTP response headers, WAF detection, and comprehensive DNS enumeration results.

### Key Observations
* **WHOIS** identified the official domain registrar, creation/expiration dates, and active EPP security locks.
* **WhatWeb** fingerprinted the Apache web server, WordPress CMS version, required plugins, Bootstrap, jQuery, Google Tag Manager, contact emails, and secure cookies.
* **Curl** returned `HTTP/2 200` and exposed standard WordPress REST API routes in response headers.
* **Wafw00f** detected **ModSecurity (SpiderLabs)** Web Application Firewall protection.
* **DNSRecon** recorded authoritative name server details, MX records, SPF/TXT records, cPanel autodiscover SRV records, and exposed BIND software versions.

*The complete command outputs and visual evidence are stored under `PM1-Footprinting/`.*

---

## W2-PM5 — Zenmap Network Scanning
Active local discovery was performed over a local wireless network interface from my personal workstation:
* **Scope:** Authorized local subnet assessment (`/24` Class C network)

### Zenmap Configuration
* **Profile:** Ping scan (`-sn`)
* **Addresses scanned:** 256
* **Hosts reported up:** 5 active endpoints (completed in 12.56 seconds)

### Observed Hosts Summary
| Host / Device Role | Discovery Status | Hardware / Vendor Details |
| :--- | :--- | :--- |
| **Default Gateway** | Host Up | Local Router / Gateway |
| **Mobile Endpoint 1** | Host Up | Android Wireless Device |
| **Mobile Endpoint 2** | Host Up | Mobile Wireless Device |
| **Mobile Endpoint 3** | Host Up | Apple iOS Device |
| **Local Workstation** | Host Up | Scanning Host (`localhost`) |

*The Zenmap visual network topology was successfully generated and exported.*
