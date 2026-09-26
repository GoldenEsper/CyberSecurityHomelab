## What is it?
System Service Number is a unique integer assigned by the operating system to every specific [[../3. LSASS Investigation/Kernel]] function. They are dynamic and so SSN's can change from a windows update. 
## How is it implemented
Its like a long menu for the kernal of what it can do eg.
*service 1: create file*
*service 2: close a handle*
*service #55: Open a process (NtOpenProcess)*
*service #120: read virtual memory* 

## Why an attacker may use it?
When utlising direct [[../3. LSASS Investigation/System calls]] an attacker may build a custom program to load a manual SSN into into the [[../3. LSASS Investigation/EAX]] register.

![](../../Images/RegularImages/Pasted%20image%2020260926191348.png)