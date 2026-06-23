# Credential Dumping Investigation (T1003.003)

# Overview

In this project, I investigated **MITRE ATT&CK T1003.003 (NTDS Credential Dumping)** using **Splunk Enterprise** and a Windows Domain Controller attack dataset.

## What is T1003.003?

T1003.003 is a credential dumping technique where an attacker tries to obtain a copy of the **NTDS.dit** file from a Windows Domain Controller. This file stores Active Directory information, including password hashes for users, computers, and service accounts.

If an attacker gains access to this file, they may be able to extract credentials, move laterally through the network, and potentially compromise the entire Active Directory environment.

## Project Goal

The goal of this project was to learn how to detect and investigate T1003.003 attacks using Splunk. I analyzed multiple Windows log sources to understand what this attack looks like and how it can be detected.

During the investigation, I looked for suspicious process creation events, PowerShell activity, credential dumping behavior, and signs of unauthorized access to the NTDS.dit file.

## Data Sources

The following logs and files were used in this investigation:

- `4688_windows-security.log`
- `crowdstrike_falcon.log`
- `windows-powershell.log`
- `windows-sec-events.log`
- `windows-security.log`
- `windows-sysmon.log`
- `windows-system.log`


---

### Splunk Attack Data
https://github.com/splunk/attack_data

---

## Investigations

I broke my project into 4 investigations. Each folder below shows exactly how that step went, what I looked for, what I found, and how it pushed me to the next phase.

01-Security-Logs-Investigation  
02-Sysmon-Process-Analysis  
03-PowerShell-Activity  
04-NTDS-Dumping-Behavior  

Each section contains:
- Splunk queries
- Observations
- Findings
- Indicators of Compromise (IOCs)
- Conclusion

---

## Environment

- Splunk Enterprise (running locally on Mac)
- Windows Security Logs
- Sysmon Logs
- PowerShell Logs
- System Logs
- CrowdStrike Falcon logs

---

## Data Sources

### Splunk Attack Data
https://github.com/splunk/attack_data

Used curated attack datasets for SOC analysis and detection practice.

---

### Attack Dataset via Git LFS

git lfs pull --include=datasets/attack_techniques/T1003.003/atomic_red_team/




---

## Tools Used

- Splunk Enterprise
- SPL queries
- Sysmon
- Windows Event Logs
- PowerShell logs
