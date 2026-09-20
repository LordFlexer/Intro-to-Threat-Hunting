Data Sources

Purpose
This document defines the data sources used in the Local AI-Based Threat Hunting Agent project. It explains what data is collected, in what format, what artifacts are extracted, and how each source maps to MITRE ATT&CK tactics. These sources feed the AI agent for hypothesis generation, detection rule creation, and security audit reporting.

Types of Data Sources

Pentest tool outputs: Nmap, Nessus, Burp Suite, Metasploit
Endpoint telemetry: Sysmon, Windows Event Log, EDR
Network telemetry: Firewall logs, IDS/IPS, NetFlow
Cloud logs: AWS CloudTrail, Azure Activity Log, GCP Audit Logs
Threat intelligence platforms: MISP, VirusTotal, Shodan, AlienVault OTX

Data Source Mapping

Source: Nmap
Format: XML
Artifacts: open ports, running services, OS fingerprint
ATT&CK Tactics: Reconnaissance, Initial Access

Source: Nessus
Format: .nessus
Artifacts: vulnerabilities, CVE IDs, misconfigurations
ATT&CK Tactics: Initial Access, Exploitation

Source: Burp Suite
Format: XML, JSON
Artifacts: web vulnerabilities, request/response data
ATT&CK Tactics: Initial Access, Execution

Source: Metasploit
Format: XML, JSON, database export
Artifacts: exploited vulnerabilities, payloads, sessions
ATT&CK Tactics: Execution, Persistence, Privilege Escalation

Source: Sysmon
Format: EVTX
Artifacts: process creation, network connections, file changes
ATT&CK Tactics: Execution, Persistence, Credential Access, Defense Evasion

Source: Windows Event Log
Format: EVTX
Artifacts: logon events, process creation, account changes
ATT&CK Tactics: Credential Access, Lateral Movement, Persistence

Source: CloudTrail
Format: JSON
Artifacts: API calls, user identities, resource changes
ATT&CK Tactics: Persistence, Privilege Escalation, Exfiltration

Source: MISP
Format: STIX, JSON, CSV
Artifacts: IOCs (IPs, domains, hashes), TTPs, threat actor profiles
ATT&CK Tactics: All

Source: VirusTotal
Format: JSON, CSV
Artifacts: file hashes, domains, IPs, detection ratios
ATT&CK Tactics: All

Source: Shodan
Format: JSON
Artifacts: exposed services, open ports, banners
ATT&CK Tactics: Reconnaissance

How These Sources Feed the AI Agent

The agent parses pentest tool outputs to extract findings such as vulnerabilities, open ports, and exploited services.
It enriches these findings with ATT&CK techniques using a RAG pipeline over MITRE ATT&CK.
It correlates findings with endpoint and network telemetry to generate threat hunting hypotheses.
It uses MISP and VirusTotal IOCs for validation and to generate detection rules in Sigma, KQL, and SPL.

Data Collection Process

Step 1: Run pentest tools (Nmap, Nessus, Burp) and export results in XML/JSON.
Step 2: Import IOCs from VirusTotal and Shodan into MISP.
Step 3: Normalize and deduplicate IOCs using the script scripts/normalize_iocs.py.
Step 4: Ingest endpoint and network logs into a SIEM (Splunk or ELK).
Step 5: Store structured data in a unified JSON format for the AI agent.

References

MITRE ATT&CK: https://attack.mitre.org
MISP Project: https://www.misp-project.org
NIST SP 800-61: Computer Security Incident Handling Guide
Splunk Documentation: https://docs.splunk.com
Microsoft Sysmon: https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon
