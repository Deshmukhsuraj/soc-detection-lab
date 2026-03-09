# SOC Detection Lab

> Personal blue team lab for building and testing ATT&CK-mapped detections.

## Stack
| Component | Purpose |
|-----------|---------|
| Splunk | SIEM — SPL detection queries |
| Sysmon + Windows EC2 | Endpoint telemetry |
| Kali Linux | Attacker simulation |
| Suricata (DMZ) | Network IDS / NDR |
| AWS CloudTrail | Cloud control plane logs |
| WireGuard VPN | Lab network segmentation |

## Detections Built

| # | File | ATT&CK Technique | Tactic | Severity | Date Tested |
|---|------|-----------------|--------|----------|-------------|
| 1 | [T1059_recon_commands.spl](detections/T1059_recon_commands.spl) | T1082, T1033, T1087 | Discovery | Medium | 2026-03-08 |
| 2 | [T1053_005_scheduled_task.spl](detections/T1053_005_scheduled_task.spl) | T1053.005, T1036.004 | Persistence | High | 2026-03-08 |
| 3 | [T1059_001_encoded_powershell.spl](detections/T1059_001_encoded_powershell.spl) | T1059.001, T1027 | Execution | Critical | 2026-03-08 |
| 4 | [T1046_network_port_scan.spl](detections/T1046_network_port_scan.spl) | T1046 | Discovery | Critical | 2026-03-09 |

## Lab Progress
- [x] Phase 0 — Lab setup (Splunk + Sysmon + Suricata + CloudTrail)
- [x] Lab 1 — Recon command detection
- [x] Lab 2 — Scheduled task persistence
- [ ] Lab 3 — Encoded PowerShell
- [ ] Lab 4 — Suricata port scan
- [ ] Lab 5 — Beaconing detection
- [ ] Lab 6 — AWS CloudTrail anomalies
```

Scroll down → commit message:
```
Add lab stack, detection index and progress tracker
