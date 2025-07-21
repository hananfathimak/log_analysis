# SOC Log Analysis & Alerting Project

This project simulates the role of a SOC (Security Operations Center) analyst by analyzing sample Windows and Linux log files to detect suspicious events such as brute-force attacks, privilege escalation, and password changes. All findings are mapped to the MITRE ATT&CK framework to reflect real-world threat detection.

---

## 1. Project Objectives
- Analyze Windows Event Logs (.evtx) and Linux Authentication Logs (auth.log).
- Detect suspicious activities such as failed logins, brute-force attempts, and unauthorized sudo commands.
- Assign severity levels (High/Medium/Low) to findings.
- Map events to MITRE ATT&CK tactics and techniques.

---

## 2. Key Findings
- **Windows:** Event ID 4794 – Attempt to set the Directory Services Restore Mode (DSRM) administrator password.
- **Linux:** 
  - Multiple failed SSH logins from 192.168.1.10 (brute-force attempt).
  - Failed root login from external IP 203.0.113.5.
  - Sudo command by user `mary` editing `/etc/hosts`.

---

## 3. MITRE ATT&CK Mapping
| # | Event | MITRE Tactic | MITRE Technique (ID) |
|---|-------|--------------|----------------------|
| 1 | Windows Event ID 4794 | Persistence / Privilege Escalation | T1098 – Account Manipulation |
| 2 | Linux failed SSH logins | Initial Access | T1110 – Brute Force |
| 3 | Failed root login | Initial Access | T1078 – Valid Accounts |
| 4 | mary sudo command | Privilege Escalation | T1548 – Abuse Elevation Control Mechanism |

---

## 4. Project Files
- **/logs/** – Sample Windows and Linux log files.
- **/screenshots/** – Evidence of suspicious events (Windows Event Viewer & Linux auth.log).
- **/report/** – Final report (PDF) with detailed findings and screenshots.

---

## 5. Tools Used
- Windows Event Viewer
- Text Editor / VS Code for Linux logs
- MITRE ATT&CK Framework

---

## 6. Conclusion
This project demonstrates practical SOC analyst skills in log analysis, threat detection, severity assignment, and MITRE ATT&CK mapping.

---

**Author:** Hanan Fathima K
