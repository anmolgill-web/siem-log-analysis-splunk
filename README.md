# Windows Security Log Analysis Using Splunk

## 📌 Project Overview

This project focuses on the collection, analysis, and investigation of Windows security-related logs using Splunk.

The project analyzes Windows Security, System, PowerShell Operational, and Microsoft Defender logs to identify authentication activity, privilege assignments, process execution, account changes, PowerShell activity, and other security-relevant events.

The objective is to understand how Windows event logs can be used by a SOC Analyst to detect, investigate, and correlate potentially suspicious activity.

---

## 🎯 Objectives

- Analyze Windows security-related events using Splunk.
- Investigate successful and failed authentication activity.
- Identify potentially suspicious logon behavior.
- Analyze privileged account activity.
- Investigate process creation events.
- Monitor account creation and account-related changes.
- Analyze PowerShell activity.
- Review system and application-related events.
- Correlate multiple Windows events to build an investigation timeline.
- Develop Splunk searches for security monitoring and investigation.

---

## 🧪 Lab Environment

| Component | Details |
|---|---|
| Operating System | Windows 11 |
| SIEM | Splunk |
| Log Source | Windows Event Logs |
| Analysis Tool | Splunk Search & Reporting |
| Log Collection | Windows Security / System / PowerShell / Defender |

---

## 🏗️ Log Analysis Architecture

```text
┌──────────────────────────┐
│      Windows System      │
│                          │
│ Security Logs            │
│ System Logs              │
│ PowerShell Logs          │
│ Defender Logs            │
└────────────┬─────────────┘
             │
             │ Log Collection
             ▼
┌──────────────────────────┐
│          Splunk          │
│                          │
│ Search & Analysis        │
│ Event Correlation        │
│ Detection                │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│     Investigation        │
│                          │
│ Authentication           │
│ Privileges               │
│ Processes                │
│ PowerShell               │
│ Account Activity         │
└──────────────────────────┘
```

---


# 🎯 Conclusion

This project demonstrates practical analysis of Windows security telemetry using Splunk.

By investigating authentication, privilege, process, PowerShell, and account-related events and correlating them across a timeline, the project demonstrates how a SOC Analyst can use SIEM data to identify potentially suspicious activity and determine whether additional investigation is required.

The project emphasizes **context-based investigation and event correlation** rather than treating individual security events as automatically malicious.




