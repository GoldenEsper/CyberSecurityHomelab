## What is it? 
The kernel is the core of an operating system. It is in charge of managing how software is allocated on a computer's hardware.

## User Mode vs Kernel Mode
Operating systems can be broken down into two modes
1. User mode: It is the restricted "execution environment" where processes run with limited privileges. In user mode process have restricted access to computers memory, cannot execute certain system calls and cannot access hardware.
2. Kernal Mode: Allows for processes to execute with full system privileges. Often reserved for the operating system itself. Processes have unrestricted access to memory, system calls and system recourses. 
Applications can request to switch to kernel mode when required [[SyncFolder/Studied Ideas and Concepts/4. LSASS Investigation/System calls|system calls]] or hardware interaction is needed. This is managed by the operating system
## What does it provide
1. Standardisation: Provides a standard interface between applications and hardware. Making it simpler for software developers to write programs on any machine.
2. Memory Protection: Protects against programs running on a computer from interfering with each other. E.g. stops Minecraft from accessing Firefox memory
3. Process management: Keeps track of what each process is permitted to do and ensure that it is only allowed to do as much as permissions allow 
4. Security: Also handles security features such as user authentication and access control
5. [[SyncFolder/Studied Ideas and Concepts/4. LSASS Investigation/System calls]] and hardware communication:  A [[SyncFolder/Studied Ideas and Concepts/4. LSASS Investigation/System calls|system call]] is a request to the operating system and hardware 
6. Stability: By managing processes and allocating memory the kernel prevents many software mistakes from causing system crashes 

![[SyncFolder/Images/RegularImages/Pasted image 20260924115311.png]]
Ref: https://en.wikipedia.org/wiki/Kernel_(operating_system)

