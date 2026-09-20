Threat Classification

1. Purpose
This document classifies cyber threats relevant to threat hunting and the Local AI-Based Threat Hunting Agent project. It defines threat types, sources of cyber threat intelligence (CTI), and their connection to MITRE ATT&CK and detection engineering.

2. Types of Cyber Threats

By Motivation
Cybercrime (financial gain, ransomware)
Espionage (data theft, intellectual property)
Hacktivism (ideological or political)
Cyberterrorism
Insider threats

By Actor
APT (Advanced Persistent Threat) — e.g., APT29, APT41
Cybercriminals — e.g., LockBit, REvil
Hacktivists — e.g., Anonymous
Insiders — employees, contractors
Script kiddies

By Attack Vector
Social engineering (phishing, pretexting)
Supply chain attacks
Web application attacks
Network attacks
Cloud misconfigurations
Physical attacks

3. CTI Sources

Strategic: Mandiant reports, CrowdStrike Global Threat Report, ENISA Threat Landscape. Provide high-level trends and actor profiles.

Operational: MISP, AlienVault OTX, MITRE ATT&CK. Contain TTPs, campaigns, and malware families.

Tactical: VirusTotal, Shodan, Maltego. Provide concrete IOCs such as hashes, IP addresses, and domains.

4. Relevance to Threat Hunting and This Project

The AI agent analyzes penetration testing results that emulate specific threat actors. By classifying threats, we select relevant actors (e.g., APT29) and map their TTPs to MITRE ATT&CK. The agent then generates hunting hypotheses and detection rules (Sigma, KQL, SPL).

Example: If the threat is classified as APT29 (espionage, supply chain), the agent focuses on techniques such as T1059.001 (PowerShell), T1003 (Credential Dumping), and T1071 (Application Layer Protocol).

5. MITRE ATT&CK Mapping (Example)

Threat Type: APT
Example Actor: APT29
Main ATT&CK Tactics: Initial Access, Persistence, Credential Access, Exfiltration

Threat Type: Ransomware
Example Actor: LockBit
Main ATT&CK Tactics: Initial Access, Impact, Defense Evasion

Threat Type: Insider
Example Actor: 
Main ATT&CK Tactics: Collection, Exfiltration

Threat Type: Hacktivist
Example Actor: Anonymous
Main ATT&CK Tactics: Impact, Initial Access

6. Conclusion

APT and supply chain threats are the most relevant for this project because they involve sophisticated TTPs that require proactive threat hunting and advanced detection engineering.
Deepseek (2026) was used as an AI assistant.
