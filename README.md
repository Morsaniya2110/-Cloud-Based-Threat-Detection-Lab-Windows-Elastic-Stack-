## Cloud-Based Threat Detection Lab (Windows + Elastic Stack)

## Overview
This lab project demonstrates how a **cloud-hosted SIEM (Security Information and Event Management)** environment can be used to detect and respond to cyber threats in real time.  
It integrates **Elastic Cloud**, a **Windows 10 endpoint**, and **custom Sigma detection rules** to simulate enterprise-grade monitoring and alerting.

## Objectives
- Centralize security log collection in a **scalable cloud platform**.
- Detect high-risk behaviors using **custom-built Sigma rules**.
- Visualize security events in **Kibana dashboards**.
- Validate detection capability through **real-world attack simulation**.
---
## Technology Stack
- **Windows 10 VM** – Endpoint generating security telemetry.
- **Sysmon** – Advanced Windows logging for detailed process and network events.
- **Elastic Agent** – Secure log forwarding to Elastic Cloud.
- **Elastic Cloud** – Centralized log storage, search, and analysis.
- **Sigma Rules** – Detection patterns for suspicious activities.
- **Kibana** – Data visualization and dashboard creation.
- **Gmail Alerts** – Email notifications for triggered detections.
---
## 📂 Architecture & Workflow
![Lab Architecture](docs/screenshots/Cloud%20Threat%20Detection(Flowchart).png)

1. **Event Collection** – Sysmon captures system activity on the Windows VM.
2. **Log Forwarding** – Elastic Agent securely transmits logs to Elastic Cloud.
3. **Threat Detection** – Sigma rules evaluate logs for malicious indicators.
4. **Visualization** – Kibana displays real-time graphs and event timelines.
5. **Alerting** – Triggered detections send an automated Gmail notification.
---
## 🎯 Detection Test – Mimikatz Credential Dumping
As part of the lab validation, the **Mimikatz** tool was executed on the Windows VM to simulate credential theft.

**Outcome:**
- Logs showed process execution consistent with credential dumping.
- Custom Sigma rule matched and triggered.
- Alert appeared in Kibana in near real time.
- Automated Gmail notification sent to designated incident inbox.

**Result:** Detection pipeline worked end-to-end, confirming the rule’s effectiveness.
---
## 📊 Capabilities Demonstrated
- SIEM log ingestion, correlation, and storage in the cloud.
- Custom detection engineering with Sigma.
- Dashboard creation for security operations visibility.
- Integration of automated alerting into cloud-based workflows.
- Practical blue team skills aligned with enterprise SOC practices.

