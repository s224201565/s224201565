# Hi, I'm Singalakha Nguluzane 👋

**Network Engineer | Cybersecurity Postgraduate | Rugby Player**

I'm a network engineer based in Gqeberha, South Africa, currently pursuing a Postgraduate Diploma in Cybersecurity at Nelson Mandela University. I build, secure, and automate networks — and I'm expanding into cloud engineering and DevOps.

## Education

- 🎓 **Postgraduate Diploma in Cybersecurity** — Nelson Mandela University *(2026 – present)*
- 🎓 **Advanced Diploma in Information Technology** — Nelson Mandela University *(2025)*
- 🎓 **Diploma in IT (Communication Networks)** — Nelson Mandela University *(2022 – 2024)*

## Certifications

- Cisco Certified Network Associate (CCNA) — Enterprise Networking, Security & Automation
- CCNAv7 — Introduction to Networks
- Cisco Certified Network Associate — Cyber Ops
- Cisco — Introduction to Cybersecurity

## Technical skills

| Area | Tools & Technologies |
|------|---------------------|
| **Networking** | Cisco IOS, VLANs, OSPF, HSRP, STP, EtherChannel, ACLs, NAT, VPNs, firewalls |
| **Cybersecurity** | Penetration testing, vulnerability assessment, exploitation & privilege escalation, OSINT, incident analysis, security frameworks & compliance, Kali Linux |
| **Automation** | Ansible, Python, C# |
| **Cloud & DevOps** | Docker, Terraform, AWS, CI/CD |
| **Tools** | Nmap, Metasploit, Burp Suite, Wireshark, Packet Tracer, GNS3, Git |

## Current research

🔐 **Securing Image Provenance Through Lightweight Cryptography and Hardware-Based Identity at the Image Sensor Level**

## Beyond the keyboard

🏉 Rugby player for **Madibaz** (Nelson Mandela University) and part-time high school rugby coach.

## Languages

English · isiXhosa · isiZulu

## Get in touch

- 📍 Gqeberha, South Africa
- 🎓 Nelson Mandela University

---

## Featured projects

> A read-only showcase of my work. Browse the folders below to view each project.

### 🖧 Germany Network — Enterprise campus network
🔗 **[View repository](https://github.com/s224201565/Germany-Network)**

A three-tier campus network (access, distribution, core) built in Cisco Packet Tracer with full
redundancy: VLANs and VTP, OSPF routing, HSRP first-hop redundancy, Rapid PVST+ spanning tree,
DHCP, NAT/PAT, ACLs, port security, SSH, and Cisco CME telephony. Includes the live Packet Tracer
project, all device configurations, an RFC design document, and an Ansible automation project.

### 🎟️ Ticketing System — House party ticketing app
🔗 **[Live demo](https://s224201565.github.io/s224201565/ticketing-system/)** · 📂 [`ticketing-system/`](ticketing-system/)

A single-page web app for running a guest list: create a party, issue a QR-coded ticket per guest,
share it, and check it at the door with a live camera scanner. Built in plain HTML, CSS, and
JavaScript, with a neon dark theme and a mobile-first layout. Handles valid, used, and cancelled
tickets.

### 🛡️ ITAI402 — Practical security coursework
🔒 *Full evidence (screenshots + walkthrough) available privately on request*

Hands-on offensive-security labs, performed only in controlled lab environments or against public,
authorised testing targets (e.g. `scanme.nmap.org`, `testphp.vulnweb.com`) — never against systems
I do not own or lack permission to test. The work spans the full methodology from reconnaissance to
reporting:

| Area | What I did | Tools |
|---|---|---|
| Reconnaissance & OSINT | Passive information gathering and automated OSINT footprinting | SpiderFoot, page source review, `robots.txt`, Wayback Machine, Google dorking |
| Network enumeration | Host discovery, full-port SYN stealth scanning, service/version detection | Nmap (`-sn`, `-sS`, `-sV`, `-p-`) |
| Vulnerability assessment | Web-app scanning (MD5 hash disclosure, CSRF, missing security headers — CWE) and service-layer CVE identification (vsftpd, Samba, distccd) | OWASP ZAP, Nmap NSE `vuln`, Greenbone/OpenVAS |
| Web application security | SQL injection, reflected XSS, CSRF with a crafted form | SQLMap, browser dev tools |
| Request interception & tampering | Proxying, intercept, Repeater, Base64 decoding, IDOR/auth testing | Burp Suite |
| Wireless security | WPA2 4-way handshake capture and offline dictionary cracking | Wireshark, Aircrack-ng |
| Exploitation | Gained a root session via two backdoors — vsftpd 2.3.4 bind shell (CVE-2011-2523) and Samba `usermap_script` (CVE-2007-2447) | Metasploit, Meterpreter |
| Privilege escalation | Escalated from an unprivileged SSH user (`uid=1000`) to root (`euid=0`) by abusing a misconfigured SUID binary (`nmap --interactive`) | SUID exploitation, Linux CLI |
| Credential access | Extracted `/etc/shadow` and `/etc/passwd`; identified weak MD5-crypt hashing suited to offline cracking | John the Ripper, Hashcat |
| Persistence | Created a hidden backdoor user with shell access to survive patching of the original vector | `useradd`, `openssl passwd` |
| Exfiltration & anti-forensics | Concealed data inside a JPEG (AES-128) to exfiltrate past traffic inspection | Steghide |
| Log analysis & forensics | `auth.log` review, Samba log correlation, Cyber Kill Chain mapping and attacker-artefact identification | Linux CLI (`grep`, `awk`) |

Includes a step-by-step penetration test of an isolated Metasploitable 2 lab VM, a formally assessed
practical exam (Samba exploitation, Greenbone vulnerability scan, log analysis and Kill Chain
mapping), and a 48-page portfolio of evidence. The materials are kept in a private repository and
shared with reviewers on request.
