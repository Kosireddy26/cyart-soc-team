# Capstone Project: Full Alert-to-Response Cycle

1. Attack Simulation (Metasploitable2)

Target VM: DEV-Linux01

Vulnerability Exploited: vsftpd backdoor (Metasploit module exploit/unix/ftp/vsftpd_234_backdoor)

Attack Steps:

Launched Metasploit: msfconsole
Selected module: use exploit/unix/ftp/vsftpd_234_backdoor
Set target: set RHOST 10.10.5.21
Executed exploit: exploit
Obtained reverse shell → simulated attacker access

 2. Detection and Triage (Wazuh)
Timestamp	          Source IP	    Alert Description	     MITRE Technique
2025-09-09 14:10:00	  203.0.113.78	VSFTPD backdoor exploit	  T1190
2025-09-09 14:12:00	  203.0.113.78	Suspicious reverse shell  TA0003 (Execution)

Alert Priority: Critical

Triage: Checked IP in AlienVault OTX → confirmed malicious activity

3. Response (CrowdSec + Isolation)

Isolation: Quarantined DEV-Linux01 VM from network
IP Blocking: Added 203.0.113.78 to CrowdSec blocklist

Verification:
ping 203.0.113.78
Result: No response → IP successfully blocked

 4. Reporting 

Executive Summary:
On Sept 9, 2025, a simulated vsftpd backdoor attack was detected on DEV-Linux01. Wazuh alerted SOC analysts to critical exploitation attempts. The source IP (203.0.113.78) was identified as malicious via threat intelligence feeds. Immediate containment and remediation were executed to prevent lateral movement and data compromise.

Timeline:

14:10 – Wazuh detected VSFTPD exploit

14:12 – Reverse shell activity detected

14:15 – VM isolated

14:20 – IP blocked via CrowdSec

14:30 – Verification and logging completed

Impact Analysis:

Compromised VM: DEV-Linux01
Data at risk: None (isolated in time)
Potential business impact: High if left unresolved

Recommendations:

Continue monitoring all Linux FTP servers
Update IPS/IDS signatures for vsftpd vulnerabilities
Regular patching and vulnerability scans
Conduct SOC simulation exercises weekly

 5. Stakeholder Briefing 

Subject: Critical Security Incident on DEV-Linux01 – Contained

Dear Manager,

On Sept 9, 2025, SOC detected and contained a simulated attack exploiting a backdoor in the DEV-Linux01 FTP service. Alerts flagged the source IP 203.0.113.78, which was immediately blocked, and the VM isolated. No data was compromised, and the threat was fully mitigated. Recommended actions include updating server patches, improving monitoring, and conducting regular attack simulations to strengthen our defenses.

Thanks,
SOC Tier 1 Analyst