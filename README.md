# Hi, I'm Shu(Shubham) Raturi
<a href="https://www.linkedin.com/in/shubham-raturi-797229288/"><img src="https://img.shields.io/badge/-LinkedIn-0072b1?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>

I'm a cybersecurity student (BTech) in Calgary. Most of what I know comes from building and running things myself. My home network has been online for over a year without breaking, and a POS system I set up for a local business has been handling real orders every day for the past 6 months.

I hold CompTIA Security+ and I'm now working toward my CCNA. Long term I want to end up in security engineering or detection work.

---

## Projects

### Point-of-Sale Deployment (6+ months in production)
I set up a full POS system for a local restaurant. Bought a custom POS terminal from China, got Debian running on it after some trouble, and deployed Odoo 19 on top. I wrote custom Odoo modules to improve the order workflow: the server asks the customer for their phone number, the system looks them up and matches the name (or prompts to create one), then shows pickup times in 15 minute slots so the customer knows when their order is ready. I also ran the cable for the receipt printers (Epson TM-m30III) to the kitchen and the counter. The whole thing gets backed up every night at 4 AM with a custom script to Proxmox Backup Server in my homelab, over Tailscale, so nothing is exposed to the internet.

### Daily Sales Tracker (9+ months of daily runs)
A pipeline that tracks the same restaurant's sales through the day. It scrapes order data from SkipTheDishes, Uber Eats and DoorDash, pulls transactions from the Clover and Wix payment APIs, and uploads everything to a Google Sheet on a daily schedule. The delivery app numbers use an estimated 30% commission since getting fee data through their APIs would have taken too long to set up, so those are close but not exact. I note that because it matters when you read the numbers.

### Wazuh SIEM Lab (writeup in progress)
I'm running Wazuh in my homelab to monitor my network: the OPNsense firewall reports in through both an agent and syslog, plus agents on my Windows desktop and my Arch Linux laptop. So far I've triaged real alerts, including scanning noise hitting my WAN and a rootcheck false positive on FreeBSD's EFI partition. At one point the active response feature blocked my own PC after I tested failed logins against the firewall, which locked me out of my own GUI. That one taught me a lot. Writeup coming soon.

### [Private Mail Server with Malware Detection](https://github.com/AlbedoAi/Mail-Server)
A self-hosted mail server built with open source tools that scans incoming mail for malware. Writeup is in the repo.

### Home Network (1+ year uptime)
OPNsense running on a Dell OptiPlex 3050, with my ISP router in bridge mode. Three VLANs (trusted LAN, wireless, homelab) across a managed TP-Link switch. Proxmox hosts AdGuard for DNS filtering, Arcane for managing containers, and Proxmox Backup Server. This is the network everything else above runs on. [Old homelab repo here](https://github.com/AlbedoAi/home-lab). I'm redoing some of the VLAN layout right now and will post an updated writeup after.

### Business Website
Designed and built a website for a local business.

---

## Other Projects
- [Python scripting and automation](https://github.com/AlbedoAi/Python-Projects)
- [IoT projects with Raspberry Pi Pico W and AWS](https://github.com/AlbedoAi/picoWProjects)

## Skills

**Security and networking:** OPNsense/pf firewall administration, VLAN segmentation, Wazuh (deployment and alert triage), Tailscale/WireGuard, Wireshark, Nmap, Nessus, Burp Suite, Metasploit

**Systems:** Linux (Debian, Arch), Windows, Proxmox VE, Proxmox Backup Server, Docker

**Development and automation:** Python, Bash, web scraping, REST APIs (Clover, Wix), Odoo module development, Git

## Certifications

<a href="https://www.credly.com/badges/7bb8d88f-194d-4211-b0ad-d0df59047c05/public_url"><img src="https://images.credly.com/size/680x680/images/80d8a06a-c384-42bf-ad36-db81bce5adce/blob" width="120" alt="CompTIA Security+ badge" /></a>

- CompTIA Security+ (earned 2026, [verify on Credly](https://www.credly.com/badges/7bb8d88f-194d-4211-b0ad-d0df59047c05/public_url))
- Cisco CCNA (in progress)

---

You can reach me on [LinkedIn](REDACTED) or open an issue on any repo.
