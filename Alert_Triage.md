Alert Triage Practice
1. Triage Simulation (Wazuh Mock Alert)
Alert ID Description	               Source IP	  Priority	Status
037	     Brute-force SSH Attempts	   172.16.45.23	  Medium	Open
038	     Suspicious PowerShell Script  192.168.56.10  High	    In Progress
039	     Port Scan Detected	           203.0.113.77	  Low	    Closed
040	     Unusual Login – After Hours   10.10.5.44	  Medium	Open

Example Focus: Alert ID 037

Wazuh flagged repeated failed SSH logins from external IP 172.16.45.23 against WEB-SRV02.

Priority: Medium, since brute-force attempts were detected but no successful login observed.

Action: IP temporarily blocked at firewall pending further TI validation.

2. Threat Intelligence Validation (AlienVault OTX & VirusTotal)

Queried 172.16.45.23 in AlienVault OTX → Found in 2 community pulses tagged as Brute Force and SSH dictionary attacks (last seen: Aug 2025).

VirusTotal check showed 5/92 vendors flagged the IP as malicious (brute force botnet).

IOC Enrichment: Correlated with attack timeframe (Sept 9, 2025, 02:15 AM – 02:20 AM).

 3. IOC Findings Summary 

The IP 172.16.45.23 was confirmed malicious via AlienVault OTX and VirusTotal, associated with brute force botnet activity. While no successful logins occurred, multiple attempts were recorded against WEB-SRV02. The incident was escalated for monitoring, firewall blocking, and log correlation to ensure no further attempts succeed against exposed services.