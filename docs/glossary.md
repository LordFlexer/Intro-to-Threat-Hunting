CTI & Threat Hunting Glossary

This glossary contains key terms related to Cyber Threat Intelligence (CTI), Threat Hunting, Detection Engineering, and the AI technologies used in this project. It serves as a foundational reference

CTI (Cyber Threat Intelligence): Evidence-based knowledge about existing threats, including context, mechanisms, indicators, and implications, used to inform decisions. Source: Recorded Future.

IOC (Indicator of Compromise): Forensic artifacts such as IP addresses, file hashes, or domains that indicate a system or network has been breached. Source: NIST.

IOA (Indicator of Attack): Behavioral patterns or actions that indicate an attack is in progress, regardless of the specific tools used. Source: SANS.

TTP (Tactics, Techniques, and Procedures): The behavior of an adversary. Tactics explain why, techniques explain how, and procedures explain the specific implementation. Source: MITRE ATT&CK.

APT (Advanced Persistent Threat): A prolonged and targeted cyberattack in which an intruder gains access to a network and remains undetected for an extended period. Source: NIST.

Threat Hunting: The proactive and iterative process of searching through networks and datasets to detect and isolate advanced threats that evade existing security solutions. Source: Chad Maurice.

Hunting Hypothesis: A testable statement based on threat intelligence or TTPs that guides a threat hunt. For example, if an attacker uses T1059.001, we will see PowerShell with encoded commands. Source: Practical Threat Hunting.

Cyber Kill Chain: A framework developed by Lockheed Martin that describes the stages of a cyberattack, from Reconnaissance to Actions on Objectives. Source: Lockheed Martin.

MITRE ATT&CK: A globally accessible knowledge base of adversary tactics and techniques based on real-world observations. Source: MITRE.

MITRE CAR: Cyber Analytics Repository, a knowledge base of analytics developed by MITRE based on the ATT&CK adversary model. Source: MITRE.

Adversary Emulation: The process of mimicking the behavior and TTPs of a specific threat actor to test an organization's defenses. Source: MITRE Engenuity.

Atomic Red Team: A library of simple, highly portable tests mapped to the MITRE ATT&CK framework, used to validate detection capabilities. Source: Red Canary.

OSINT (Open-Source Intelligence): Intelligence collected from publicly available sources such as social media, public databases, and websites. Source: Michael Bazzell.


Tools and Platforms

MISP: Malware Information Sharing Platform, an open-source threat intelligence platform for sharing, storing, and correlating IOCs. Source: MISP Project.

SIEM: Security Information and Event Management, a system that aggregates and analyzes log data from across an organization to detect security threats. Source: Gartner.

EDR: Endpoint Detection and Response, security software that continuously monitors endpoints and responds to threats. Source: Gartner.

Sysmon: A Windows system service and device driver that logs system activity to the Windows Event Log, providing detailed telemetry for threat hunting. Source: Microsoft.

Shodan: A search engine for Internet-connected devices, allowing users to discover exposed services and vulnerabilities. Source: Shodan.

VirusTotal: A free online service that analyzes files and URLs for viruses, worms, trojans, and other kinds of malicious content. Source: VirusTotal.

Maltego: A software used for open-source intelligence and forensic investigations, allowing users to visualize relationships between data points. Source: Maltego.

MITRE CALDERA: An automated adversary emulation system that performs post-compromise adversarial behavior. Source: MITRE.

STIX/TAXII: Structured Threat Information Expression (language) and Trusted Automated Exchange of Intelligence Information (protocol) for sharing CTI. Source: OASIS.

Detection Engineering

Detection Rule: A formalized logic statement that identifies specific malicious or suspicious activity within telemetry. Source: Megan Roddie.

Sigma: A generic, open-source, vendor-agnostic signature format for log events, often called Snort for logs. Source: SigmaHQ.

KQL: Kusto Query Language, used in Microsoft Sentinel and Defender XDR for querying and detecting threats. Source: Microsoft.

SPL: Search Processing Language, the query language used in Splunk for searching and analyzing machine data. Source: Splunk.

False Positive: A detection rule triggering an alert for legitimate activity. Source: NIST.

False Negative: A detection rule failing to trigger an alert for malicious activity. Source: NIST.

Telemetry: The collection of data from remote or inaccessible sources and its transmission to a central system for monitoring and analysis. Source: SANS.

Coverage: The extent to which detection rules map to and catch specific ATT&CK techniques. Source: MITRE.

AI, LLM and RAG

LLM (Large Language Model): A neural network trained on massive amounts of text to understand and generate human-like text, such as Llama 3 or Mistral. Source: OpenAI.

Open-Source LLM: A language model whose weights and architecture are publicly released, allowing it to be run locally and privately. Source: Meta AI.

RAG (Retrieval-Augmented Generation): A technique that combines an LLM with a retrieval system, such as a vector database, to ground the model's responses in factual, up-to-date documents. Source: LangChain.

Embedding: A numerical vector representation of text that captures its semantic meaning, used for similarity search. Source: Sentence-Transformers.

Vector Database: A specialized database that stores and queries embeddings, such as ChromaDB, FAISS, or Qdrant. Source: Pinecone.

Ollama: A tool that allows users to easily download, run, and manage open-source LLMs locally. Source: Ollama.

ChromaDB: An open-source vector database designed for building AI applications with embeddings. Source: Chroma.

LangChain: A framework for developing applications powered by language models, often used to build RAG pipelines. Source: LangChain.

Hallucination: When an LLM generates incorrect, fabricated, or nonsensical information that is not grounded in its training data or provided context. Source: IBM.

Prompt: The input text provided to an LLM to guide its output. Source: OpenAI.

Data Sources and Pentesting

Penetration Testing (Pentest): An authorized simulated cyberattack on a computer system, performed to evaluate the security of the system. Source: NIST.

Nmap: A network scanner used to discover hosts and services on a computer network. Source: Nmap.org.

Nessus: A proprietary vulnerability scanner used to identify vulnerabilities, misconfigurations, and missing patches. Source: Tenable.

Burp Suite: A web application security testing tool used for scanning and exploiting web vulnerabilities. Source: PortSwigger.

CloudTrail: An AWS service that logs API calls made in an AWS account, used for auditing and threat hunting in cloud environments. Source: AWS.
DeepSeek (2026) was used as a generative AI tool to assist
