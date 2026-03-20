# SOC Analyst Practical Assessment

### Project Overview
This repository contains the final deliverables for a comprehensive Security Operations Center (SOC) practical assessment. It demonstrates the ability to execute end-to-end incident response, from initial SIEM alert triage to deep-dive forensic evidence preservation and executive reporting.

### Included Deliverables
*  Alert Management & Triage:** Demonstrates alert prioritization (CVSS scoring), MITRE ATT&CK mapping, and OSINT validation using VirusTotal for a highly malicious WannaCry file hash.

*  Incident Response Documentation:** Outlines a 7-step Phishing SOP and a detailed Post-Mortem summary following a simulated server breach.

*  Evidence Preservation:** Contains cryptographic chain-of-custody hashes (SHA256) and volatile network data captures (`ss -antp`) taken directly from the compromised Linux endpoint.

* Capstone Incident Report:** An executive-level technical timeline and stakeholder briefing documenting the complete lifecycle of a critical VSFTPD v2.3.4 backdoor exploitation.

### Tools & Technologies Utilized
* **Virtualization & Attack Simulation:** Kali Linux, Metasploitable2, VirtualBox
* **Exploitation Framework:** Metasploit Framework (`msfconsole`)
* **Forensics & Command Line:** Linux CLI, `ss`, `dd`, `sha256sum`
* **Threat Intelligence:** VirusTotal, CVSS Framework, MITRE ATT&CK

*Prepared and submitted by: Vibhuti Kumar*
