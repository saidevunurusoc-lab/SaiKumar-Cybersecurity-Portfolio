# Splunk – Detection Engineering

## 🔹 Brute Force Detection Rule
Search:
index=* sourcetype=WinEventLog:Security "4625"
| stats count() by src_ip, user
| where count > 10

📌 Result: Detects too many failed logins

Add dashboard screenshots here:  
`Splunk-Lab/Dashboard-Screenshots/`
