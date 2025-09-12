# Alert Management Practice

 1. Google Sheets – Alert Classification System
Alert ID	    Type	       Priority	   MITRE Tactic (Technique ID)
021	Suspicious  Email Link	   High	       Initial Access (T1566.002)
022	Ransomware  Execution	  Critical     Impact (T1486)
023	Port Scan   (Recon)	      Low	       Reconnaissance (T1046)
024	Failed RDP  Attempts	  Medium	   Credential Access (T1110)
025	Log4Shell   Exploit Try	  Critical     Execution (T1190)

Alert: “User received phishing email with login link” → Classified High, maps to T1566.002.

2. Prioritizing Alerts with CVSS
Alert Type	         CVSS Score	 Priority
Log4Shell Exploit	 9.8	     Critical
Ransomware (LockBit) 9.5	     Critical
Failed RDP Attempts	 6.5	     Medium
Phishing Email	     7.3	     High
Port Scan	         3.1	     Low

3.TheHive – Incident Ticket

Title: [Critical] LockBit Ransomware Detected on DB-SQL01
Description:

Detected file: lockbit_payload.exe

Abnormal file encryption in C:\Finance\ shared folder

Malicious outbound IP: 203.0.113.45

Persistence via scheduled task (UpdateCheck)
Priority: Critical
Assignee: Tier 1 SOC Analyst

4. Escalation Email (100 words)

Subject: [Escalation] Critical LockBit Ransomware Incident on DB-SQL01

Body:
Hello Tier 2 Team,

We have identified a Critical ransomware incident on DB-SQL01. The malware lockbit_payload.exe was detected encrypting files in the C:\Finance\ folder. Outbound connections to IP 203.0.113.45 were observed, flagged by Wazuh as CVSS 9.5 (Critical). Persistence was established via a scheduled task named UpdateCheck. A case has been opened in TheHive with all relevant indicators. Immediate containment is advised to prevent further spread to connected systems. Please take over for deep analysis and eradication.

Thanks,
SOC Tier 1 Analyst