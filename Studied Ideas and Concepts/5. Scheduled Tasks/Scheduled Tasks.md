## What are they?
Events/Services that are configured to be launched at a future time, recurring interval or with a specific trigger event. All major Operating Systems use them and can be abused. This tactic falls under T1053.005
## What do attackers gain?

Adversaries use multiple methods to modify the task schedulers. Some examples include [[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/Windows Task Scheduler]], [[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/NET wrapper|.NET Wrapper]], the Windows [[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/netapi32.dll]] and Windows Management Instrumentation ([[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/WMI]]). Attacks can use the task scheduler to facilitate recurring execution of malicious code. Attackers can use these recurring executions to establish persistence on a machine.
## Detection
**Windows event ID 4698** indicates that a scheduled task was created using task scheduler. Looking for unusual services creating scheduled tasks, e.g., office applications or a webserver. Also monitoring for unusual [[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/WMI]] permanent events.
## Methods of mitigation:

Ensure that administrative rights are secured to prevent unauthorised task creation. Enable advanced auditing for task scheduler and WMI.
# How each technology generates scheduled tasks 

#### Windows Managment Instrumentation ([[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/WMI]])
- Schedules tasks based off of events.
- Achieved through "WMI Event Subscriptions"
- Real time response, can be quite complex
#### NET Wrapper ([[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/NET wrapper|.Net Wrapper]])
- Utilises [[SyncFolder/Studied Ideas and Concepts/3. Powershell Investigation/Framework .NET|.NET]] with wrapper functions to schedule task
- The wrapper helps to make the execution chain less visible when creating the task
#### Windows Task scheduler ([[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/Windows Task Scheduler|WTS]])
- Can trigger off of defined events (Time, system startup, user logon)
- Quite visible as can be seen in task scheduler
#### [[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/netapi32.dll]]`
- A dynamic link library that is primarily used in network managment
- Has access to [[SyncFolder/Studied Ideas and Concepts/5. Scheduled Tasks/Legacy NET Schedule service]] which enables the netapi32.dll to schedule tasks
- Malicious actors can abuse access to this to schedule attacks. 
