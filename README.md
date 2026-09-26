Topic: Local AI-Based Threat Hunting Agent

Title: Automated Analysis of Penetration Testing Results, Detection Hypothesis Generation, and Security Audit Report Creation

Overview: This project would be an experimental use of a local AI-based agent designed to support threat hunting processes. This agent automatically analyzes penetration testing results, maps them to MITRE ATT&CK, generates hypotheses, produces detection rules "Sigma" (better because convertion ability), and creates security reports. The core idea is to transform traditional pentest output into actionable threat hunting intelligence without relying on cloud AI services — everything runs locally using open-source LLMs (Language Models) and RAG (Generation with database).

Tools & Technologies

Local LLM: Ollama / llama.cpp
RAG: LangChain / LlamaIndex + ChromaDB / FAISS
CTI Platforms: MISP, Shodan, VirusTotal, Maltego
SIEM: Splunk / ELK Stack
Detection Rules: Sigma, KQL, SPL
Adversary Emulation: MITRE CALDERA, Atomic Red Team
Frameworks: MITRE ATT&CK, Cyber Kill Chain, MITRE CAR
Languages: Python 3.10+, Bash
Containerization: Docker, Docker Compose

Why Local LLM + RAG?
Privacy: pentest results, logs, and IOCs never leave the local environment.
Cost: no API fees; runs on a laptop or lab server.
Accuracy: RAG grounds the LLM in up-to-date knowledge bases — MITRE ATT&CK, SigmaHQ, CVE, Atomic Red Team — preventing hallucinations.
Extensibility: new threat intel can be added to the vector DB without retraining the model.

During the preparation of this assignment, the author used DeepSeek (https://chat.deepseek.com) as a generative AI assistant throughout the entire workflow — including brainstorming, code examples, documentation, and text editing. All AI-generated content was reviewed, verified, and adapted by the author, who takes full responsibility for the final work.

This assignment represents a small independent research effort: the dataset was analyzed locally, machine learning metrics were computed, MITRE ATT&CK mapping was performed, and a Sigma detection rule was generated as a proof of concept for the Local AI-Based Threat Hunting Agent project.

Reference: DeepSeek. (2026). DeepSeek [Large language model]. Retrieved from https://chat.deepseek.com
