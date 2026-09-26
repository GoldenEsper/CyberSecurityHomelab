## How does it work?
A system call is a "controlled entry point that allows a user program to request a service from the operating system"

![](../../Images/RegularImages/Pasted%20image%2020260926191318.png)
## How is it used?
Often related to any kind of operation that a user program can perform like creation, termination, forking, moving, communication etc. see below for how they are grouped. Effectively provides a layer of separation between the user mode and the kernel mode. 

![](../../Images/RegularImages/Pasted%20image%2020260926191323.png)

Ref: https://www.geeksforgeeks.org/operating-systems/introduction-of-system-call/

## Relation to cybersecurity
#### LSASS Dumping utilising direct system calls
The following can be used to dump LSASS memory `openprocess`,`ReadProcessMemory`, `MiniDumpWriteMemory` . These are relatively high level functions which fortunately are often monitored by EDR/AV's which use [[User-Mode Hooking]]. To bypass this detection often malicious actors will write a small amount of assembly code and manually load the [[../4. Scheduled Tasks (Persistence)/SSN]] into the [[EAX]] register. As this jumps past the regular high level system call this process can bypass some EDR tools.
