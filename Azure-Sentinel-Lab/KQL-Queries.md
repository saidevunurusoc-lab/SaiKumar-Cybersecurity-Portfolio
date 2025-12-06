# Azure Sentinel – KQL Queries

## 1️⃣ Failed Login Detection
KQL:
SigninLogs
| where ResultType != 0
| summarize count() by IPAddress, UserPrincipalName
| order by count_ desc


📌 Purpose: Detect repeated failed logins (Brute Force)

---

## 2️⃣ Suspicious IP Reputation Check
SigninLogs
| where IPAddress in ("<malicious_ip_here>")


📌 Add screenshot in:  
`Azure-Sentinel-Lab/Incident-Screenshots/`
