## What does it do?
Allows for the scheduling of tasks to automate execution. In this instance it is managed by the Task Scheduler Service.
## How does it work?
Task scheduler operates with 4 main elements.
1. Trigger - Defines when to start a task (schedule(daily weekly), time, startup, login)
2. Action - Define what the task does (E.g. Start a program, send an email)
3. Conditions - Specific environmental requirements to run the task
4. Settings - Define how task behaves if fails or is already running

## Methods of interaction:
1. GUI (`taskschd.msc`) - [[MMC|Microsoft Management Console]] snap-in used for visual management.
2. Command Line (`schtasks.exe`) - CLI tool used for the creation, deletion and changing of tasks
3. Powershell (ScheduledTasks) - Modern means of managing tasks (e.g, get-ScheduledTask)

## Why an attacker may use it?

![](../../Images/RegularImages/Pasted%20image%2020260926191353.png)