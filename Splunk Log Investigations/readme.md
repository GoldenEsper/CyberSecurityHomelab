# Splunk Log Investigations Summary

Developed custom Splunk detection rules mapped to MITRE ATT&CK techniques, validated using Atomic Red Team tests to generate realistic attack traffic. Covered four major detection scenarios: obfuscated PowerShell (T1059.001), LSASS credential theft (T1003.001), persistence via scheduled tasks (T1053.005), and multi-event correlation for discovery followed by privilege escalation (T1082 + T1068). Built detection logic using Sysmon and Windows security event logs, implemented whitelist tables and alert throttling to reduce false positives, and consolidated results into an executive Splunk dashboard.

---

[Obfuscated PowerShell Detection (Defense Evasion)](https://github.com/GoldenEsper/CyberSecurityHomelab/blob/main/Splunk%20Log%20Investigations/Tests%20Conducted/T1059.001%20-%20Power%20Shell%20Investigation.md)
- Atomic Test: Invoke-AtomicTest T1059.001 (Encoded PowerShell).
- SSE Mapping: Unusually Long Command Line / Obfuscated PowerShell.
- Workflow: Open Splunk Security Essentials, navigate to Find Content, search for "Encoded PowerShell", and inspect the SPL logic.
- Deliverable: Build a Splunk alert using eval and rex to parse Sysmon Event ID 1 logs, extract encoded strings, and trigger an alert when flags like -enc or -w hidden appear.

[Credential Theft (LSASS Scraping)](https://github.com/GoldenEsper/CyberSecurityHomelab/blob/main/Splunk%20Log%20Investigations/Tests%20Conducted/T1003.001%20-%20LSASS%20Credential%20Theft.md)

- Atomic Test: Invoke-AtomicTest T1003.001 (LSASS Dumping).
- SSE Mapping: LSASS Memory Access / Process Injection.
- Workflow: Look up "LSASS Process Access" inside SSE to analyze how enterprise rules flag non-standard process access.
- Deliverable: Write a targeted alert for Sysmon Event ID 10 targeting lsass.exe. Add whitelist logic using a Splunk Lookup Table to filter out legitimate system processes.

[Persistence Mechanism Identification](https://github.com/GoldenEsper/CyberSecurityHomelab/blob/main/Splunk%20Log%20Investigations/Tests%20Conducted/T1053.005%20-%20Scheduled%20tasks.md)

- Atomic Test: Invoke-AtomicTest T1053.005 (Scheduled Tasks).
- SSE Mapping: Scheduled Task Creation in Suspicious Paths.
- Workflow: Search SSE for "Persistence via Scheduled Task" to see how Sysmon Event ID 1 or Windows Event ID 4698 are structured.
- Deliverable: Build an alert that flags schtasks.exe executions where the task payload executes out of \AppData\, \Temp\, or \Public\.

[T1082, T1068 - Correlation & Capstone Alerting](Tests%20Conducted/T1082,%20T1068%20-%20Correlation%20&%20Capstone%20Alerting.md)

- Atomic Test: T1082 (Discovery) followed by T1068 (Privilege Escalation).
- SSE Mapping: Multi-Event Sequences / Discovery Activity.
- Workflow: Review SSE rules under the Correlation Searches category to learn how to link multiple event IDs over a rolling time window.
- Deliverable: Create a single Splunk alert that triggers only when 3+ rapid reconnaissance commands occur on an endpoint within 5 minutes of a process elevation. Save these alerts to an executive Splunk dashboard.

To learn: 
- Understand behavioral techniques
- Understand trends in logs and what can make something suspicious