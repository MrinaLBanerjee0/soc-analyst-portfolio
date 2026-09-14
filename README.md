# Hello, I'm Mrinal

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mrinal_Banerjee-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mrinal00/)

## About Me

I'm an aspiring SOC Analyst building hands-on experience through evidence-backed security labs. My focus is security monitoring, Windows and Active Directory telemetry, SIEM investigation, threat hunting, detection validation, and incident analysis.

I learn by building environments, generating controlled security activity, investigating the resulting telemetry, documenting what the evidence proves, and being explicit about limitations.

## Recruiter Snapshot

- **SIEM:** Elastic Security / ELK, Splunk Enterprise
- **Windows & Identity:** Active Directory, Windows Security Events, Kerberos, PowerShell Script Block Logging, Sysmon
- **Investigation:** alert triage, event correlation, process-tree analysis, IOC/hash enrichment, threat hunting
- **Detection:** custom detection validation, false-positive analysis, rule tuning and retesting
- **Infrastructure:** Microsoft Azure, Windows Server, Windows 11, Ubuntu/Linux, VirtualBox
- **Case workflow:** basic Elastic-to-osTicket ticket automation

## Projects

### 1. [Azure ELK Security Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab)

An evidence-backed SOC lab built in Microsoft Azure using Elastic Security.

- Built a multi-VM Azure lab and centralized Windows and Linux telemetry in Elastic
- Used Elastic Agent / Fleet, Sysmon, Microsoft Defender telemetry, Windows Security logs, and Linux SSH/system logs
- Validated custom SSH and Windows failed-logon detections with controlled activity
- Investigated alerts through raw-event, source, user, and host pivots
- Created Kibana monitoring visualizations and basic Elastic-to-osTicket ticket automation
- Documented architecture, evidence boundaries, investigation findings, exported artifacts, and limitations
- Configured Mythic HTTP profile and an Apollo payload, but **did not prove an active Mythic callback**

**Evidence:** [Project README](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) · [Investigation Report](https://github.com/MrinaLBanerjee0/azure-elk-security-lab/blob/main/SOC-INVESTIGATION-REPORT.md) · [Evidence Index](https://github.com/MrinaLBanerjee0/azure-elk-security-lab/tree/main/evidence)

---

### 2. [Enterprise Active Directory + Splunk SOC Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab)

A Windows domain and Splunk SOC lab focused on investigation, correlation, threat hunting, and detection tuning.

- Built `corp.soclab.test` with Windows Server 2022 AD DS/DNS, two Windows 11 domain workstations, and a dedicated Splunk server
- Forwarded Windows Security, Application/System, Sysmon, and PowerShell Operational telemetry to Splunk
- Investigated a controlled Sep 10 activity sequence involving PowerShell `4104`, AD group changes `4728/4729`, workstation logons `4624`, and Kerberos `4768/4769`
- Correlated workstation and domain-controller evidence instead of treating alerts as conclusions
- Performed process-tree analysis and SHA-256 enrichment during a separate controlled validation
- Tuned DET-001 and DET-003 from v1 to v2 after identifying a benign keyword false positive and noisy cross-host correlation logic
- Kept DET-002 at v1 because the detection condition worked correctly and did not require tuning
- Performed an independent threat hunt and documented what was and was not visible in the collected telemetry
- Preserved an inline evidence gallery, incident report, tuning report, SPL files, and evidence limitations

**Evidence:** [Project README](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) · [Incident Investigation](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/sep10-incident-investigation.md) · [Detection Tuning Report](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/detection-tuning-report.md) · [Visual Evidence Gallery](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/evidence/README.md)

> **SPL learning boundary:** the Splunk searches in Project 2 were implemented, tested, debugged, tuned, and retested as part of guided learning. I do not present them as independently authored from scratch.

## Skills by Evidence

| Skill | Evidence |
|---|---|
| SIEM monitoring & log analysis | [Azure ELK Security Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) · [AD + Splunk SOC Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) |
| Alert investigation & event correlation | [Azure investigation](https://github.com/MrinaLBanerjee0/azure-elk-security-lab/blob/main/SOC-INVESTIGATION-REPORT.md) · [Splunk incident investigation](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/sep10-incident-investigation.md) |
| Windows / Active Directory telemetry | [AD + Splunk SOC Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) |
| Sysmon & PowerShell logging | [Azure ELK Security Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) · [AD + Splunk SOC Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) |
| Kerberos analysis | [AD + Splunk incident investigation](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/sep10-incident-investigation.md) |
| Detection validation & tuning | [Splunk detection tuning report](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/detection-tuning-report.md) |
| Threat hunting | [AD + Splunk SOC Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) |
| Azure networking & telemetry collection | [Azure ELK Security Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) |
| Basic case-management automation | [Azure ELK Security Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) |

## Tools & Technologies

**SIEM / Analytics:** Splunk Enterprise, Elasticsearch, Kibana, Elastic Security  
**Windows / Identity:** Active Directory Domain Services, DNS, Windows Security Events, Kerberos, PowerShell, Sysmon, Microsoft Defender  
**Collection:** Splunk Universal Forwarder, Elastic Agent, Fleet  
**Infrastructure:** Microsoft Azure, VirtualBox, Windows Server 2022, Windows 11, Ubuntu/Linux  
**Investigation / Validation:** VirusTotal, event correlation, process-tree analysis, controlled security testing  
**Case Management:** osTicket

## Certification

- **Google Cybersecurity Professional Certificate** — [Verify on Credly](https://www.credly.com/badges/d6d8c2c7-87e4-4646-9b22-9763c1c8437d/public_url)

## Current Goal

I am seeking a SOC Trainee / Tier 1 SOC Analyst opportunity where I can apply my lab-based investigation experience, continue improving my SPL/KQL and networking skills, and grow through real security operations work.
