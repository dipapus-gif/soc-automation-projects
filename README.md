# Automated Malware Triage & Incident Response Pipeline

An automated Security Operations Center (SOC) workflow built using *n8n* running on *Kali Linux*. This pipeline automatically ingests alerts from a SIEM/webhook source, queries threat intelligence platforms, evaluates risk levels, leverages AI for automated threat analysis, and logs incident tickets and reports.

---

## 🚀 Architecture Overview

```text
[Wazuh SIEM / Webhook] ──> [n8n Webhook Trigger] ──> [VirusTotal Hash Check] 
                                                              │
                                                              ▼
[Trello / Incident Ticket] <── [AI Analysis Model] <── [Risk Classification]
