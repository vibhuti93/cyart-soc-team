# FOUNDATIONAL SOC DEPLOYMENT: WEEKLY TASK REPORT 01
**Project Identifier:** CYART-SOC-W01-2026  
**Analyst:** VIBHUTI KUMAR  
**Original Submission Date:** March 13, 2026  
**Submission Status:** This document was originally delivered via direct correspondence and has been added to this repository for archival purposes.

---

## 1. MISSION OBJECTIVE
[cite_start]The primary goal of this foundational phase was to establish a functional Security Operations Center (SOC) environment capable of proactive detection, analysis, and response[cite: 6]. [cite_start]The scope included deploying a centralized SIEM architecture, establishing log collection pipelines, utilizing vulnerability scanners, and simulating attacks to capture actionable network forensics[cite: 7, 8].

---

## 2. TARGET ARCHITECTURE
The simulation environment was constructed within a controlled virtual machine network:
* [cite_start]**Host Environment:** Kali Linux (SOC Analyst / SIEM Deployment)[cite: 11].
* [cite_start]**Target Environment:** Metasploitable 2 (10.0.2.x)[cite: 12].
* [cite_start]**Forensics Interface:** Local Loopback (127.0.0.1)[cite: 13].

---

## 3. TECHNICAL METHODOLOGY & TOOLSET
[cite_start]The deployment was guided by the NIST SP 800-61 Incident Response framework and the CIA triad[cite: 15]. The following tools were utilized:
* [cite_start]**SIEM Orchestration:** Docker-Compose for the Wazuh XDR/SIEM stack[cite: 17].
* [cite_start]**Vulnerability Management:** Nessus Essentials[cite: 18].
* [cite_start]**Endpoint Forensics:** SQLite3 CLI[cite: 19].
* [cite_start]**Simulation:** THC-Hydra for SSH dictionary attacks[cite: 20].

---

## 4. CORE TASK SUMMARIES

### 4.1 VULNERABILITY ASSESSMENT
[cite_start]A comprehensive scan identified multiple Critical (CVSS 10.0) vulnerabilities on the target host[cite: 24, 29]. Specific vectors included:
* [cite_start]UnrealIRCd Backdoor (Port 6667)[cite: 29].
* [cite_start]Bind Shell Backdoor (Port 1524) allowing unauthenticated remote code execution[cite: 29].

### 4.2 INTRUSION DETECTION (SNORT)
[cite_start]Snort IDS was initialized with custom rules to establish a baseline for network-level threat detection[cite: 208, 213]. Validated rules included:
* [cite_start]**ICMP Detection:** Tracking ping requests on the local loopback interface[cite: 241].
* [cite_start]**HTTP Detection:** Identifying requests to known malicious domains[cite: 213].

### 4.3 LOG PIPELINE MANAGEMENT
[cite_start]Established a normalized log collection pipeline using Logstash and Fluentd[cite: 280, 281].
* [cite_start]**Logstash:** Configured for Apache log normalization and JSON output generation[cite: 309].
* [cite_start]**Fluentd:** Verified via synthetic alert ingestion and REST API POST requests[cite: 283, 346].

### 4.4 ENDPOINT & BROWSER FORENSICS
[cite_start]Conducted localized artifact hunting using the sqlite3 CLI to query the Firefox `places.sqlite` database[cite: 349]. [cite_start]The analysis identified anomalous navigation to local administrative ports (5601, 9392)[cite: 350].

### 4.5 SIEM DEPLOYMENT (WAZUH)
[cite_start]The Wazuh XDR/SIEM stack was successfully orchestrated via Docker-Compose[cite: 412]. Technical resolutions included:
* [cite_start]**Kernel Tuning:** Modifying `vm.max_map_count` to 262144 for Indexer stability[cite: 414].
* [cite_start]**Credential Desynchronization:** Identifying and resolving secret mismatches between the Indexer and Dashboard containers via environment variable extraction[cite: 611, 634].

---

## 5. INCIDENT RESPONSE SIMULATION (NIST SP 800-61)
[cite_start]The report concludes with a critical severity incident simulation involving a Bind Shell backdoor and a high-volume SSH brute-force attack[cite: 613, 617].
* [cite_start]**Containment:** Isolated the Metasploitable host from the primary NAT network to prevent lateral movement[cite: 618].
* [cite_start]**Eradication:** Recommended service termination and SSH hardening (disabling root login, implementing key-based auth)[cite: 619, 620].

---
**[END OF README]**