# penetration-testing-labs
Penetration Testing Lab Reports | Air University — Metasploit, Nmap, CVE exploitation on Metasploitable 2 (Educational purposes only)
# 🔐 Penetration Testing Lab Reports
### Air University, Islamabad — Department of Cyber Security
### Faculty of Computing and Artificial Intelligence

---

## 📋 Overview

This repository contains lab reports for the **Penetration Testing** course. Each lab covers hands-on offensive security techniques using industry-standard tools in a controlled, isolated virtual environment.

> ⚠️ **Disclaimer:** All activities performed in these labs are conducted in an isolated lab environment on intentionally vulnerable machines (Metasploitable 2). This content is strictly for **educational purposes**. Unauthorized use of these techniques on real systems is illegal.

---

## 🗂️ Repository Structure

```
penetration-testing-labs/
│
├── README.md                        ← You are here
│
└── lab-reports/
    └── lab05/
        ├── Lab05_PenetrationTesting_Report.docx   ← Full report with screenshots
        └── screenshots/                            ← Raw screenshot references
```

---

## 📁 Labs

| Lab | Title | Topics Covered | Status |
|-----|-------|---------------|--------|
| Lab 05 | Introduction to Exploitation | Metasploit, Metasploitable 2, CVE exploitation | ✅ Complete |

---

## 🧪 Lab 05 — Introduction to Exploitation (Metasploit & Metasploitable)

### Description
A hands-on penetration testing lab using **Metasploit Framework** against **Metasploitable 2** — a deliberately vulnerable Linux VM designed for security training.

### Environment
| Component | Details |
|-----------|---------|
| Attacker Machine | Kali Linux |
| Target Machine | Metasploitable 2 |
| Network Setup | Host-Only / NAT Adapter (isolated) |
| Tools Used | Metasploit Framework, Nmap, Netcat, Telnet |

### Tasks Summary

| # | Task | CVE / Technique | Marks |
|---|------|----------------|-------|
| 1 | Metasploitable 2 Setup & Network Verification | Network config, ping, curl | 10 |
| 2 | Initial Enumeration with Nmap | `-p-`, `-sC -sV` scans | 10 |
| 3 | Exploiting vsftpd 2.3.4 Backdoor | CVE-2011-2523 (CVSS 10.0) | 15 |
| 4 | SMTP User Enumeration | `smtp_enum` auxiliary module | 10 |
| 5 | Exploiting Samba usermap_script | CVE-2007-2447 (CVSS 10.0) | 15 |
| 6 | Telnet Access via Default Credentials | Default creds, privilege escalation | 10 |
| 7 | Bind Shell via Netcat (Port 1524) | Unauthenticated root bind shell | 10 |
| 8 | Meterpreter Post-Exploitation | In-memory payload, post-exploitation | 10 |
| | **Total** | | **100** |

### Key CVEs Exploited
- **CVE-2011-2523** — vsftpd 2.3.4 backdoor (supply chain attack, CVSS 10.0)
- **CVE-2007-2447** — Samba 3.0.20 `usermap_script` command injection (CVSS 10.0)

---

## 🛠️ Tools & Technologies

![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=flat&logo=kali-linux&logoColor=white)
![Metasploit](https://img.shields.io/badge/Metasploit-2596CD?style=flat&logo=metasploit&logoColor=white)
![Nmap](https://img.shields.io/badge/Nmap-blue?style=flat)
![Netcat](https://img.shields.io/badge/Netcat-black?style=flat)

| Tool | Purpose |
|------|---------|
| **Metasploit Framework** | Exploit execution, payload delivery, post-exploitation |
| **Nmap** | Port scanning, service/version detection |
| **Netcat (nc)** | Direct bind shell connection |
| **Telnet** | Default credential exploitation |

---

## ⚙️ Setup Instructions

### Prerequisites
- VirtualBox or VMware Workstation
- Kali Linux VM
- Metasploitable 2 VM

### Network Configuration (VirtualBox)
```bash
# Kali Linux: Set Adapter 1 as NAT, Adapter 2 as Host-Only
# Metasploitable: Set Adapter 1 as Host-Only

# Verify connectivity from Kali:
ping -c 3 <metasploitable-ip>
curl http://<metasploitable-ip>
```

### Network Configuration (VMware)
```bash
# Both VMs: Set to NAT Adapter
# Metasploitable IP will be on eth0
```

> 🔒 **NEVER expose Metasploitable 2 to the internet or any production network.**

---

## 📸 Screenshots

All task screenshots are embedded in the lab report `.docx` file. Each task includes:
- Terminal output of commands
- Exploit execution results
- Post-exploitation confirmations

---

## 📚 Learning Outcomes

After completing Lab 05, students are able to:
- Set up and configure an isolated penetration testing lab environment
- Perform comprehensive port and service enumeration using Nmap
- Exploit known CVEs using Metasploit Framework modules
- Understand supply chain attacks (vsftpd backdoor, SolarWinds analogy)
- Enumerate valid system users via SMTP VRFY/EXPN commands
- Perform privilege escalation via default credentials
- Differentiate between bind shells and reverse shells
- Use Meterpreter for in-memory post-exploitation

---

## ⚖️ Legal & Ethical Notice

```
This repository is intended SOLELY for educational purposes within an academic setting.
All exploitation techniques documented here were performed on intentionally vulnerable,
isolated virtual machines with explicit authorization.

Performing these techniques on systems without written permission is:
  - Illegal under the Computer Fraud and Abuse Act (CFAA)
  - Illegal under Pakistan's Prevention of Electronic Crimes Act (PECA 2016)
  - A violation of international cybercrime laws

The author assumes NO responsibility for misuse of this material.
```

---

## 👤 Author

| Field | Details |
|-------|---------|
| **Institution** | Air University, Islamabad |
| **Department** | Cyber Security |
| **Course** | Penetration Testing Lab |
| **Lab Engineer** | Bilal Saleem |

---

<p align="center">
  <i>Made for educational purposes only — Air University Cyber Security Department</i>
</p>
