## What is it?
System Service Number is a unique integer assigned by the operating system to every specific [Kernel](../3.%20LSASS%20Investigation/Kernel.md) function. They are dynamic and so SSN's can change from a windows update. 
## How is it implemented
Its like a long menu for the kernal of what it can do eg.
*service 1: create file*
*service 2: close a handle*
*service #55: Open a process (NtOpenProcess)*
*service #120: read virtual memory* 

## Why an attacker may use it?
When utlising direct [System calls](../3.%20LSASS%20Investigation/System%20calls.md) an attacker may build a custom program to load a manual SSN into into the [EAX](../3.%20LSASS%20Investigation/EAX.md) register.

![](../../Images/RegularImages/Pasted%20image%2020260926191348.png)