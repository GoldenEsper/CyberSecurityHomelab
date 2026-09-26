## What is it?
System Service Number is a unique integer assigned by the operating system to every specific [[SyncFolder/Studied Ideas and Concepts/4. LSASS Investigation/Kernel]] function. They are dynamic and so SSN's can change from a windows update. 
## How is it implemented
Its like a long menu for the kernal of what it can do eg.
*service 1: create file*
*service 2: close a handle*
*service #55: Open a process (NtOpenProcess)*
*service #120: read virtual memory* 

## Why an attacker may use it?
When utlising direct [[SyncFolder/Studied Ideas and Concepts/4. LSASS Investigation/System calls]] an attacker may build a custom program to load a manual SSN into into the [[SyncFolder/Studied Ideas and Concepts/4. LSASS Investigation/EAX]] register.

![[SyncFolder/Images/RegularImages/Pasted image 20260924093652.png]]