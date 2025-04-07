## 🧪 Lab Scenario Summary

This lab simulates an insider threat scenario within a corporate network environment. An employee in a sensitive department, recently placed on a Performance Improvement Plan (PIP), has exhibited concerning behavior. Management has flagged this employee as a potential risk for data exfiltration or malicious insider activity.

You have been assigned as a security analyst to investigate this individual’s recent activities using Microsoft Defender for Endpoint (MDE). Your focus will be to analyze file events, network activity, and process execution on the employee’s assigned workstation: **`resend7393-vm`**.

---

## 📌 Lab Objectives

| Objective ID | Description                                                                   |
|--------------|-------------------------------------------------------------------------------|
| OBJ-01       | Review recent file activity on the employee’s corporate device               |
| OBJ-02       | Identify any access or modification of sensitive/proprietary files           |
| OBJ-03       | Correlate file operations with outbound network connections (exfil attempts) |
| OBJ-04       | Detect any suspicious use of PowerShell, scripting tools, or archiving apps  |
| OBJ-05       | Summarize findings and provide mitigation recommendations                    |

---

## 📁 Repository Contents

| File Name                                           | Description                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| `Report_Findings.txt`				| Investigation results structured using MITRE ATT&CK				|
| `Investigation.txt`				     | Core KQL queries used during investigation				|
| `exfiltratedataps1.md`                                        | Summary of malicious PowerShell script                         |
| `TotalEmployeeDeviceFileEvents.csv`                | Full export of file event logs for the target device                       |
| `EmployeeDeviceFileEventsInvestigation.csv`        | Focused file activity timeline for user/device `resend7393-vm`             |
| `EmployeeDeviceFileEventsAndDeviceNetworkEventsInvestigation.csv` | Correlated file + network event dataset for deeper investigation     |


---

## 🛠️ Tools Used

- Microsoft Defender for Endpoint (MDE)
- Microsoft Sentinel (Log Analytics Workspace)
- Kusto Query Language (KQL)

