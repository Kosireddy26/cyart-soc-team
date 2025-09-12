
# Incident Response Lifecycle

Incident Response Lifecycle Steps

Step 1: Preparation

Ensured playbooks for phishing incidents were ready
Confirmed SOC monitoring rules and alert channels were active
Users were trained to report suspicious emails

Step 2: Identification

Timestamp	Action
2025-09-09 09:15:00	User reported suspicious email
2025-09-09 09:25:00	SOC verified email headers and link

Step 3: Containment

Isolated affected workstation (HR-WS07) from network
Quarantined phishing email across all mailboxes
Disabled link in mail gateway

Step 4: Eradication

Checked for any affected users or credentials (none found)
Deleted malicious email from backups and mail server logs
Updated mail gateway rules to block similar URLs

Step 5: Recovery

Restored normal access for the affected workstation
Conducted additional training for HR team on phishing awareness
Monitored logs for any follow-up malicious activity

Step 6: Lessons Learned

Early reporting reduced risk exposure
Need to enhance automated email filtering for impersonation attacks
Regular awareness campaigns increase user vigilance

Phishing Response Checklist
Confirm email headers (SPF/DKIM/From address)
Check link reputation (VirusTotal, URLHaus)
Identify affected users
Quarantine malicious email from all inboxes
Force password reset if credentials were exposed
Update SIEM and mail gateway rules