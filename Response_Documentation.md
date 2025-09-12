Response Documentation
Incident Response Template (Mock Phishing Incident – Sept 9, 2025)

1. Executive Summary
On Sept 9, 2025, a phishing email impersonating the IT Helpdesk was reported by an employee. The email contained a malicious link redirecting to a fake Microsoft 365 login page. Quick detection and response prevented credential theft and lateral movement.

2. Timeline

Timestamp	Action
2025-09-09 09:15:00	User reported suspicious email
2025-09-09 09:25:00	SOC isolated the user’s workstation
2025-09-09 09:40:00	Collected email headers & URL sample
2025-09-09 10:00:00	URL submitted to VirusTotal (malicious)
2025-09-09 10:20:00	Blocked domain on mail gateway & proxy
2025-09-09 11:00:00	Checked logs for affected users (none)
2025-09-09 12:30:00	Sent advisory to all employees

3. Impact Analysis

Affected User: 1 (Finance team)
Data Compromised: None (no credentials entered)
Business Impact: Minimal, prevented escalation
Potential Risk: Account takeover, lateral spread

4. Remediation Steps

Quarantined phishing email in mail system
Blocked malicious domain across firewall & proxy
Forced password reset for reported user
Conducted phishing awareness training for Finance team
Updated email filtering rules to flag similar patterns

5. Lessons Learned

Early user reporting significantly reduced response time
Need better mail gateway rules for impersonation detection
Continuous awareness campaigns improve detection

 Investigation Steps (Logged Actions)
Timestamp	Action
2025-09-09 09:25:00	Isolated workstation (HR-WS07)
2025-09-09 09:40:00	Collected email headers (Outlook .msg)
2025-09-09 09:50:00	Captured suspicious URL & tested hash
2025-09-09 10:10:00	Conducted memory dump of workstation
2025-09-09 11:00:00	Verified logs for lateral movement

Post-Mortem 

The Sept 9, 2025 phishing attempt highlighted the effectiveness of quick user reporting and SOC escalation. No credentials were stolen, but delayed domain blocking showed gaps in our mail security rules. Future improvements include enhancing email gateway filters, expanding employee training, and strengthening automated detection for impersonation-based phishing campaigns.