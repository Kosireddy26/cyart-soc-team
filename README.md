# Week 4 - Capstone SOC Incident Response

## Objective
Simulate a full SOC workflow covering attack simulation, detection, triage, response, automation, RCA, and reporting.

## Tools Used
- Metasploit (Attack Simulation)
- MITRE Caldera (Adversary Emulation)
- Wazuh SIEM (Detection & Alerting)
- CrowdSec (Response & Blocking)
- TheHive (Case Management & SOAR Automation)
- Elastic Security (Metrics & Dashboards)
- Google Docs/Sheets (Reports & Documentation)
- Draw.io (Fishbone Diagrams)

## Workflow Steps
1. Attack Simulation: Metasploit (`exploit/multi/samba/usermap_script`) vs Metasploitable2.
2. Detection & Triage: Wazuh detects Samba exploit -> alert forwarded to TheHive. Mapped to MITRE T1210.
3. Response & Containment: CrowdSec blocks attacker IP `192.168.1.102`. Verify via ping.
4. SOAR Automation: Playbook auto-creates case & blocks IP.
5. RCA: 5 Whys and Fishbone Diagram (Draw.io).
6. Metrics: Dashboard for MTTD, MTTR, Dwell Time.
7. Reporting: Capstone Report, Stakeholder Briefing, Attack Logs, Visuals.

## Folder Structure
```
Week_4/
│── README.md
│── Capstone_Report.pdf
│── Stakeholder_Briefing.pdf
│── Attack_Logs.pdf
│── Wazuh_Alert.png
│── CrowdSec_Block.png
│── Dashboard.png
│── RCA_Fishbone.png
```

## Notes
All artifacts are realistic-styled mockups intended for assignment submission. Timestamps in logs are simulated for demonstration.
Prepared on 2025-10-06 10:49:23 UTC
