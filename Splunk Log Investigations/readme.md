# Splunk Log Investigations Summary

Developed custom Splunk detection rules mapped to MITRE ATT&CK techniques, validated using Atomic Red Team tests to generate realistic attack traffic. Covered four major detection scenarios: obfuscated PowerShell (T1059.001), LSASS credential theft (T1003.001), persistence via scheduled tasks (T1053.005), and multi-event correlation for discovery followed by privilege escalation (T1082 + T1068). Built detection logic using Sysmon and Windows security event logs, implemented whitelist tables and alert throttling to reduce false positives, and consolidated results into an executive Splunk dashboard.

---

[T1059.001 - Power Shell Investigation](Tests%20Conducted/T1059.001%20-%20Power%20Shell%20Investigation.md)
- AI Summary
> Investigated and detected obfuscated PowerShell execution using Atomic Red Team test T1059.001. Validated Splunk Universal Forwarder XML field extraction, installed the Splunk Windows Add-On, and built alerts using `eval` and `rex` to parse Sysmon Event ID 1 logs for suspicious flags (`-enc`, `-w hidden`).

[T1003.001 - LSASS Credential Theft](Tests%20Conducted/T1003.001%20-%20LSASS%20Credential%20Theft.md)
- AI Summary
> Developed detection for LSASS memory dumping attacks using ProcDump, Dumpert, Nanodump, and comsvcs.dll. Built Splunk alert on Sysmon Event ID 10 targeting unauthorized lsass.exe access with whitelist logic (MsMpEng.exe, taskmgr.exe, csrss.exe) via Splunk Lookup Tables. Validated detection across multiple dumping tools and tuned alert throttling to prevent alert fatigue.  


[T1053.005 - Scheduled tasks](Tests%20Conducted/T1053.005%20-%20Scheduled%20tasks.md)
- AI Summary
> Investigated multiple scheduled task persistence vectors including COM automation, WMI/PS_ScheduledTask, VBA macro execution, and registry-encoded payloads. Built detection on Windows Event ID 4698 and Sysmon Event ID 1, configured Local Security Policy audit subcategories for complete log coverage, and identified suspicious execution paths (`\AppData\`, `\Temp\`, `\Public\`).

[T1082, T1068 - Correlation & Capstone Alerting](Tests%20Conducted/T1082,%20T1068%20-%20Correlation%20&%20Capstone%20Alerting.md)
- AI Summary
> Engineered a multi-event correlation alert detecting when 3+ reconnaissance commands (`whoami`, `systeminfo`, `net user`, `netstat`) occur within 300 seconds of a privilege escalation event (`sc create` / driver loading). Used Splunk `join` and sub-searches with rolling time windows to correlate Sysmon and Windows security events across endpoints.

To learn: 
- Understand behavioral techniques
- Understand trends in logs and what can make something suspicious