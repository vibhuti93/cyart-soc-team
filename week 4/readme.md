# SOC CAPSTONE PROJECT: INCIDENT RESPONSE AND ADVERSARY EMULATION
**Project Identifier:** CYART-SOC-2026-CAP  
**Analyst:** VIBHUTI KUMAR 
**Date:** April 6, 2026  

---

## 1. EXECUTIVE SUMMARY
This project documents the comprehensive lifecycle of a Security Operations Center (SOC) response to a critical infrastructure breach. The incident involved the exploitation of a legacy Samba service (CVE-2007-2447) on a Metasploitable2 target. The scope of work encompasses proactive threat hunting, automated response orchestration (SOAR), root cause analysis (RCA), digital forensics, and adversary emulation. The primary objective was to validate detection engineering and minimize adversary dwell time through structured incident response phases.

---

## 2. TECHNICAL INFRASTRUCTURE
The following security stack and environments were utilized to facilitate the project:

* **SIEM/XDR:** Wazuh Manager and Agent (v4.x)
* **Network IDS:** Snort
* **Adversary Emulation:** MITRE Caldera Framework
* **Threat Intelligence:** LevelBlue Labs / AlienVault OTX
* **Forensic Tools:** SHA-256 Hashing, Velociraptor, Terminal Logging
* **Attack Platforms:** Kali Linux, Metasploit Framework (MSF)
* **Target Environment:** Metasploitable2 (Linux 2.6.x)

---

## 3. PORTFOLIO DIRECTORY (THE 8 DELIVERABLES)
The project documentation is organized into eight distinct reports, each addressing a specialized domain of cybersecurity operations.

### DOCUMENT 01: THREAT HUNTING REPORT
* **Focus:** Proactive identification of administrative privilege escalation (Event ID 4672).
* **Methodology:** SIEM log analysis cross-referenced with threat intelligence pulses.

### DOCUMENT 02: SOAR PLAYBOOK SUMMARY
* **Focus:** Automation of containment workflows.
* **Methodology:** Integration of Wazuh Level 7 anomaly triggers with automated network isolation.

### DOCUMENT 03: POST-INCIDENT ANALYSIS
* **Focus:** Root Cause Analysis (RCA).
* **Methodology:** Application of the "5 Whys" and Ishikawa Diagram to identify systemic failures.

### DOCUMENT 04: ALERT TRIAGE VALIDATION
* **Focus:** True Positive (TP) versus False Positive (FP) verification.
* **Methodology:** Forensic validation of root-level privilege escalation following service exploitation.

### DOCUMENT 05: EVIDENCE CHAIN OF CUSTODY
* **Focus:** Forensic integrity and legal admissibility.
* **Methodology:** Generation of timestamped SHA-256 cryptographic hashes for authentication logs.

### DOCUMENT 06: ADVERSARY EMULATION REPORT
* **Focus:** Defense validation using MITRE ATT&CK TTPs.
* **Methodology:** Execution of automated discovery operations (T1033, T1087) via MITRE Caldera.

### DOCUMENT 07: SECURITY METRICS AND EXECUTIVE REPORTING
* **Focus:** High-level Key Performance Indicators (KPIs).
* **Methodology:** Visualization of SOC efficiency metrics, including MTTD and MTTR.

### DOCUMENT 08: FINAL CAPSTONE INCIDENT REPORT
* **Focus:** Comprehensive technical and executive summary.
* **Methodology:** Unified report covering the incident lifecycle from detection to strategic remediation.

---

## 4. INCIDENT PERFORMANCE METRICS
* **Mean Time to Detect (MTTD):** 15 Minutes
* **Mean Time to Respond (MTTR):** 5 Minutes
* **Detection Rate (Critical Exploitation):** 100%
* **Forensic Integrity Verification:** Validated via SHA-256

---

## 5. LAB CONFIGURATION AND COMPLIANCE
All activities were conducted within a sandboxed, virtualized environment. Network isolation was maintained throughout the exploitation and containment phases to prevent cross-contamination. This project adheres to ethical hacking standards and NIST 800-61 Rev. 2 incident handling guidelines.

---
**[END OF DOCUMENT]**