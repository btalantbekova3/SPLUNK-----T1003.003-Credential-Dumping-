# Credential Dumping Investigation (T1003.003)

## Overview
This project investigates credential dumping activity using Splunk Enterprise and Windows DC real attack datasets.

The goal isto detect suspicious behavior related to NTDS and system credential access using multiple Windows log sources.

---

### Splunk Attack Data
https://github.com/splunk/attack_data

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

## Objective

- Detect credential dumping activity
- Analyze suspicious process behavior
- Identify NTDS / LSASS access patterns
- Correlate activity across multiple logs

---

## Investigations

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

## Tools Used

- Splunk Enterprise
- SPL queries
- Sysmon
- Windows Event Logs
- PowerShell logs
