# ICS Security Assessment & Protection Roadmap

[![GitHub Pages](https://img.shields.io/badge/Pages-Enabled-brightgreen)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Markdown Lint](https://github.com/prince-savaliya/ics-security-assessment/actions/workflows/markdownlint.yml/badge.svg)](https://github.com/prince-savaliya/ics-security-assessment/actions/workflows/markdownlint.yml)

> A defence‑in‑depth security assessment of an Industrial Control System (ICS) network.

---

## 🚀 Project Highlights

- **Comprehensive ICS Risk Mapping:** Aligns findings against MITRE ATT&CK ICS® framework.
- **Interactive Network Diagrams:** Editable Draw.io files and exports.
- **Step-by-Step Remediation Playbook:** Detailed fixes, configurations, and runbooks.
- **Ready-to-Use Scripts:** Custom Nmap NSE scripts for Siemens S7 device enumeration.
- **Professional Documentation:** Full PDF report, slide deck, and asset inventory.

---

## 🌐 Network Topology Diagram

A high-resolution network topology is available in PDF format:

![image](https://github.com/user-attachments/assets/77533587-4cc7-462a-9350-802dedcfd32b)


[📄 Download the network topology diagram (PDF)](diagrams/COJ_OT-Network_segmented.pdf)
---

## 📖 Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
- [Assessment Methodology](#assessment-methodology)
- [Key Findings](#key-findings)
- [Remediation Playbook](#remediation-playbook)
- [Repository Structure](#repository-structure)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 📖 Overview

Industrial control systems often run on legacy protocols and flat networks, enabling lateral movement and potential process disruption. This repository delivers a four-phase security analysis—discovery, enumeration, risk mapping, and mitigation—for a Siemens-based OT environment.

---

## 🛠 Getting Started

1. **Clone the repository**  
   ```bash
   git clone https://github.com/prince-savaliya/ics-security-assessment.git
   cd ics-security-assessment
   ```

2. **Explore the full report**  
   - `docs/ICS_Assessment_Report.pdf` – Detailed findings, raw outputs, and diagrams.

3. **View Network Diagrams**  
   - `diagrams/COJ_OT-Network_segmented.drawio` – Editable in [draw.io](https://app.diagrams.net).

4. **Run Discovery Scripts**  
   ```bash
   nmap -sn -iL reports/Asset_Inventory_Network_Segmentation.xlsx -oG nmap_results.gnmap
   nmap --script nmap-scripts/nmap_NSE_Links.txt -p 102,80 <target_subnet>
   ```

---

## 🔍 Assessment Methodology

1. **Layer-2 Discovery** – ARP/Netdiscover scans  
2. **Ping Sweep & Port Scanning** – Nmap host/service enumeration  
3. **Protocol Probing** – Siemens S7 NSE scripts  
4. **Risk Mapping** – MITRE ATT&CK ICS® alignment

---

## ⚠️ Key Findings

- **Flat Network Architecture:** Single VLAN, no segmentation.  
- **Unmanaged Remote Access:** VPN router in production zone.  
- **Public PLC Webserver:** Siemens S7-1500 CPU state change risk.  
- **Open HMI Ports:** Web interface without strong authentication.  

> See full details in `docs/ICS_Assessment_Report.pdf`.

---

## 📚 Remediation Playbook

Detailed remediation steps are available in `playbooks/remediation_playbook.md`, covering:

- Network segmentation & firewall rules  
- Secure VPN setup & account management  
- PLC & HMI hardening best practices  
- Monitoring & patch management cadence

---

## 📂 Repository Structure

```
├── .github/              # CI workflows & configs
├── docs/                 # Full PDF report
├── diagrams/             # Draw.io network diagrams
├── nmap-scripts/         # Custom NSE scripts
├── playbooks/            # Remediation runbooks
├── reports/              # Asset inventory & segmentation
├── slides/               # Presentation deck
├── notes/                # Supplementary notes & raw command sheets
├── .gitignore            # Files to ignore in Git
├── LICENSE               # Project license
└── README.md             # Project overview
```

---

## 🤝 Contributing

Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 📜 License

This project is licensed under the MIT License – see [LICENSE](LICENSE) for details.

---

## 📬 Contact

*Prince Savaliya*  
- LinkedIn: https://www.linkedin.com/in/prince-savaliya  
- Email: prince@example.com  
