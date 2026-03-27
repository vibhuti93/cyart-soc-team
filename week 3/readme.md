# PROJECT: SOC WORKFLOW SIMULATION & PRACTICAL APPLICATION
# AUTHOR: Vibhuti Kumar
# DATE: March 27, 2026

================================================================================
1. PROJECT OVERVIEW
================================================================================
This project is an end-to-end Incident Response simulation designed to mirror 
real-world Security Operations Center (SOC) workflows. The simulation follows 
the lifecycle of a cyberattack—from initial exploitation to forensic 
preservation and final executive reporting.

Key phases include:
- Attack Simulation (Metasploit / Samba Usermap Script)
- Detection & Triage (SIEM Alerts & MITRE ATT&CK Mapping)
- Containment & Escalation (iptables blocking & TheHive Ticket creation)
- Reporting (Technical Analysis & Executive Briefings)

================================================================================
2. CORE OBJECTIVES & DELIVERABLES
================================================================================
The project is documented across six (6) specialized PDF reports:

1. Advanced_Log_Analysis_Report.pdf
   - Log correlation of failed logins (Event ID 4625) with data egress.
   - Anomaly detection rule configuration in Elastic Security.

2. Threat_Intelligence_Integration_Report.pdf
   - Automated alert enrichment using AlienVault OTX.
   - Proactive threat hunting for MITRE T1078 (Valid Accounts).

3. Incident_Escalation_and_Workflows.pdf
   - SITREP (Situation Report) drafting for unauthorized access.
   - Formal Tier 2 escalation summaries and SOAR automation logic.

4. Alert_Triage_and_IOC_Validation.pdf
   - Prioritizing alerts by CVSS scores and mapping to MITRE Tactics.
   - OSINT validation of malicious file hashes via VirusTotal.

5. Evidence_Preservation_and_Chain_of_Custody.pdf
   - Volatile data collection (netstat) from compromised hosts.
   - Forensic integrity hashing (SHA-256) of memory dumps.

6. Capstone_SOC_Simulation_Final_Report.pdf
   - Full technical timeline of the Samba exploitation (CVE-2007-2447).
   - Evidence of successful containment via iptables.
   - Non-technical executive briefing.

================================================================================
3. TECHNICAL STACK & TOOLS USED
================================================================================
- Attacker Machine: Kali Linux 2025.4
- Target Machine: Metasploitable 2
- SIEM Platforms: Elastic Cloud / Wazuh Cloud
- Threat Intel: VirusTotal / AlienVault OTX
- Forensic Tools: Velociraptor / sha256sum
- Attack Tools: Metasploit Framework / Hydra

================================================================================
4. PRACTICAL EXECUTION SUMMARY
================================================================================
- ATTACK: Exploited 'usermap_script' on port 139/445 to gain root shell.
- LOGS: Generated failed SSH authentication logs using Hydra brute-force.
- CONTAINMENT: Executed 'sudo iptables -A INPUT -s 10.0.2.15 -j DROP' on target.
- INTEGRITY: Verified evidence using SHA-256: e3b0c44298fc1c149afbf4c8...
- VALIDATION: Confirmed malicious indicators via 69/71 vendor detection rate.

================================================================================
5. STATUS: PROJECT COMPLETED
================================================================================
All practical objectives have been met and documented with technical 
screenshots and forensic evidence.
