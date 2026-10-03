## What are they?
Events/Services that are configured to be launched at a future time, recurring interval or with a specific trigger event. All major Operating Systems use them and can be abused. This tactic falls under T1053.005
## What do attackers gain?

Adversaries use multiple methods to modify the task schedulers. Some examples include [Windows Task Scheduler](Windows%20Task%20Scheduler.md), [NET wrapper](NET%20wrapper.md), the Windows [netapi32.dll](netapi32.dll.md) and Windows Management Instrumentation ([WMI](WMI.md)). Attacks can use the task scheduler to facilitate recurring execution of malicious code. Attackers can use these recurring executions to establish persistence on a machine.
## Detection
**Windows event ID 4698** indicates that a scheduled task was created using task scheduler. Looking for unusual services creating scheduled tasks, e.g., office applications or a webserver. Also monitoring for unusual [WMI](WMI.md)] permanent events.
## Methods of mitigation:

Ensure that administrative rights are secured to prevent unauthorised task creation. Enable advanced auditing for task scheduler and WMI.
# How each technology generates scheduled tasks 

#### Windows Managment Instrumentation ([WMI](WMI.md))
- Schedules tasks based off of events.
- Achieved through "WMI Event Subscriptions"
- Real time response, can be quite complex
#### NET Wrapper ([.NET wrapper](NET%20wrapper.md))
- Utilises [[../2. Powershell Investigation/Framework .NET|.NET]] with wrapper functions to schedule task
- The wrapper helps to make the execution chain less visible when creating the task
#### Windows Task scheduler ([Windows Task Scheduler](Windows%20Task%20Scheduler.md))
- Can trigger off of defined events (Time, system startup, user logon)
- Quite visible as can be seen in task scheduler
#### [netapi32.dll](netapi32.dll.md)`
- A dynamic link library that is primarily used in network managment
- Has access to [Legacy NET Schedule service](Legacy%20NET%20Schedule%20service.md) which enables the netapi32.dll to schedule tasks
- Malicious actors can abuse access to this to schedule attacks. 
