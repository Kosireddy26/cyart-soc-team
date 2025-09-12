# Week 2 SOC Project

1.Alert Management Practice

Tools: Google Sheets, Wazuh, TheHive

Created an alert classification table mapping alerts to MITRE ATT&CK techniques.
Simulated alerts in Google Sheets and calculated CVSS scores for prioritization.
Created a Wazuh dashboard visualizing alert priorities.
Drafted incident ticket in TheHive:

Title: [Critical] LockBit Ransomware on DB-SQL01

Indicators: lockbit_payload.exe, IP 203.0.113.45
Priority: Critical
Assignee: SOC Analyst
Escalated a Critical alert via a 100-word email to Tier 2 SOC.


2.Response Documentation (Phishing Incident)

Tools Used: Google Docs, Draw.io

Steps Completed (Incident Response Lifecycle – Sept 9, 2025):

Preparation: Verified playbooks and user reporting.

Identification: User reported phishing email; headers and link analyzed.

Timestamp	Action
2025-09-09 09:15:00	User reported suspicious email
2025-09-09 09:25:00	SOC verified email headers and link

Containment: Isolated HR-WS07, quarantined email, blocked malicious link.
Eradication: Deleted email from backups and mail server; updated rules.
Recovery: Restored workstation access; monitored logs.
Lessons Learned: Enhance mail filtering and conduct phishing awareness campaigns.
Post-Mortem :
Early reporting prevented credential theft. Mail gateway rules were improved to detect impersonation attacks. Continuous user training is essential to strengthen organizational security and reduce response time for future phishing attempts.

3️. Alert Triage Practice

Tools Used: Wazuh, VirusTotal, AlienVault OTX

Steps Completed:

Analyzed mock alerts and assigned priorities:
Validated malicious IPs with AlienVault OTX & VirusTotal.
Documented IOC validation in 50-word summary. 

4. Evidence Preservation

Tools Used: Velociraptor, FTK Imager

Steps Completed:

Collected network connections from DB-SQL01 using Velociraptor and saved as CSV.
Acquired memory dump DB-SQL01_memory_2025-09-09.raw and generated SHA256 hash.

5.Capstone Project: Full Alert-to-Response Cycle

Tools Used: Metasploit, Wazuh, CrowdSec, Google Docs

Steps Completed:

Exploit simulated vsftpd backdoor on DEV-Linux01 using Metasploit.
Wazuh detected VSFTPD exploit and reverse shell activity.
Response: Isolated VM, blocked IP in CrowdSec, verified ping test.
Reporting: 200-word SANS-style report with Executive Summary, Timeline, Recommendations.
Stakeholder Briefing: 100-word non-technical summary delivered.