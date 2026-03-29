# Wazuh SIEM Home Lab

A hands-on SIEM deployment built to develop real SOC analyst 
skills — log ingestion, alert triage, custom rule writing, 
and incident investigation.

---

## Lab Architecture

| Component | Details |
|-----------|---------|
| SIEM Manager | Wazuh on Kali Linux |
| Monitored Endpoint | Windows 11 (physical host) |
| Agent | Wazuh Agent 4.x |
| Additional Tool | Sysmon with SwiftOnSecurity config |

---

## What I Built

- Deployed Wazuh manager on Kali Linux and connected 
  Windows 11 as a monitored agent
- Configured Sysmon on Windows 11 for enhanced process 
  and network telemetry
- Simulated seven different attack scenarios and confirmed 
  detection in the Wazuh dashboard
- Configured File Integrity Monitoring on sensitive directories
- Built a SOC overview dashboard with alert trends, 
  severity distribution, and top rule breakdown
- Wrote formal investigation reports for each simulated incident

---

## Incidents Simulated and Detected

| Incident | Windows Event ID | Wazuh Rule | MITRE Technique |
|----------|-----------------|------------|-----------------|
| Brute force login attempts | 4625 | 60204 | T1110 |
| New user account created | 4720 | 60106 | T1136.001 |
| Account added to Administrators | 4732 | 60144 | T1078.001 |
| Firewall disabled | 2003 | - | T1562.004 |
| Suspicious process execution | Sysmon 1 | - | T1059 |
| Audit policy modified | 4719 | - | T1562.002 |
| Sensitive directory file created | FIM | - | T1074 |

---

## Custom Rules

See [rules/local_rules.xml](rules/local_rules.xml)

Three custom rules written to enhance detection coverage 
with explicit MITRE ATT&CK mappings and adjusted severity levels.

---

## Investigation Reports

See the [investigations](investigations/) folder for 
formal write-ups of each simulated incident including 
timeline, evidence, analysis, and recommended response actions.

---

## Screenshots

See the [screenshots](screenshots/) folder. All screenshots 
are referenced and explained in the investigation reports.

---

## Key Skills Demonstrated

- SIEM deployment and agent management
- Windows event log analysis
- Sysmon telemetry configuration
- Custom detection rule authoring in XML
- File integrity monitoring configuration
- Alert triage and investigation methodology
- MITRE ATT&CK technique mapping
- Incident report writing

---

## Disclaimer

All simulated attacks were performed exclusively in a 
personal lab environment on systems I own and control. 
No real networks, users, or organisations were involved.
```
