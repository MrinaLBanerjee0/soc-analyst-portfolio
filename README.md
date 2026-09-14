# Hello, I'm Mrinal

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mrinal_Banerjee-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mrinal00/)

## About Me

I'm working toward a SOC Analyst role and most of my learning comes from building labs, breaking things, fixing them, and then investigating the logs to understand what actually happened.

So far I've spent the most time with Elastic, Splunk, Windows, Active Directory, Sysmon, PowerShell logging, Kerberos, and basic incident investigation. I try to keep my project notes tied to what I actually observed instead of making a lab look more impressive than it was.

## What I've worked with

- **SIEM:** Elastic Security / ELK, Splunk Enterprise
- **Windows & identity:** Active Directory, Windows Security Events, Kerberos, PowerShell Script Block Logging, Sysmon
- **Investigation:** alert triage, event correlation, process-tree analysis, hash enrichment, threat hunting
- **Detection:** validation, false-positive review, tuning, and retesting
- **Infrastructure:** Microsoft Azure, Windows Server, Windows 11, Ubuntu/Linux, VirtualBox
- **Case workflow:** basic Elastic-to-osTicket ticket automation

## Projects

### 1. [Azure ELK Security Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab)

This was my first larger SOC lab. I built it in Azure and used Elastic Security to collect and investigate Windows and Linux telemetry.

What I worked on:

- built a multi-VM Azure lab and centralized Windows and Linux logs in Elastic
- used Elastic Agent / Fleet, Sysmon, Microsoft Defender telemetry, Windows Security logs, and Linux SSH/system logs
- tested custom SSH and Windows failed-logon detections with controlled activity
- investigated alerts by going back to the raw events and pivoting on source, user, and host
- built Kibana monitoring visualizations and basic Elastic-to-osTicket ticket automation
- documented the architecture, investigation, exported artifacts, and the gaps I found
- configured a Mythic HTTP profile and Apollo payload, but **I did not prove an active Mythic callback**

[Project README](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) · [Investigation Report](https://github.com/MrinaLBanerjee0/azure-elk-security-lab/blob/main/SOC-INVESTIGATION-REPORT.md) · [Evidence](https://github.com/MrinaLBanerjee0/azure-elk-security-lab/tree/main/evidence)

---

### 2. [Enterprise Active Directory + Splunk SOC Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab)

For this project I wanted more Windows and identity investigation practice, so I built a small domain and sent the Windows telemetry into Splunk.

What I worked on:

- built `corp.soclab.test` with Windows Server 2022 AD DS/DNS, two Windows 11 domain workstations, and a dedicated Splunk server
- forwarded Windows Security, Application/System, Sysmon, and PowerShell Operational logs to Splunk
- investigated a controlled Sep 10 sequence involving PowerShell `4104`, AD group changes `4728/4729`, workstation logons `4624`, and Kerberos `4768/4769`
- correlated workstation events with domain-controller activity instead of treating an alert as the final answer
- practiced process-tree analysis and SHA-256 enrichment during a separate validation
- tuned DET-001 and DET-003 from v1 to v2 after finding a benign keyword false positive and noisy cross-host logic
- kept DET-002 at v1 because it was doing what I intended and I didn't find a real reason to create a v2
- performed a separate threat hunt after the alert investigation
- kept the screenshots, reports, SPL, and known limitations in the repository

[Project README](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) · [Incident Investigation](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/sep10-incident-investigation.md) · [Detection Tuning Report](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/detection-tuning-report.md) · [Evidence Gallery](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/evidence/README.md)

> **SPL note:** I learned and built the Project 2 SPL with guidance. I implemented it in my own lab, tested it against my telemetry, debugged field issues, tuned the rules, and retested them. 

## Skills I can show in the labs

| Skill | Where I used it |
|---|---|
| SIEM monitoring & log analysis | [Azure ELK Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) · [AD + Splunk Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) |
| Alert investigation & event correlation | [Azure investigation](https://github.com/MrinaLBanerjee0/azure-elk-security-lab/blob/main/SOC-INVESTIGATION-REPORT.md) · [Splunk investigation](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/sep10-incident-investigation.md) |
| Windows / Active Directory telemetry | [AD + Splunk Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) |
| Sysmon & PowerShell logging | [Azure ELK Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) · [AD + Splunk Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) |
| Kerberos analysis | [Splunk investigation](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/sep10-incident-investigation.md) |
| Detection validation & tuning | [Detection tuning report](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab/blob/main/investigations/detection-tuning-report.md) |
| Threat hunting | [AD + Splunk Lab](https://github.com/MrinaLBanerjee0/enterprise-ad-splunk-soc-lab) |
| Azure networking & telemetry collection | [Azure ELK Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) |
| Basic ticket automation | [Azure ELK Lab](https://github.com/MrinaLBanerjee0/azure-elk-security-lab) |

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

I'm looking for a SOC Trainee / Tier 1 SOC Analyst opportunity where I can use the investigation skills I've been building in my labs and keep improving my SPL, KQL, networking, and day-to-day SOC workflow.