# .NET and how it works

Effectively .NET is a framework that allows for universal execution of code so long as the machine has the .NET runtime installed. Once code is compiled it is turned into “Intermediate Language”. What this allows is for the program to interface with the machine's “Just In Time” compiler. What this does is for the instructions to be mapped to the hardware instructions specific to the machine. 
![](../../Images/RegularImages/Pasted%20image%2020260926185124.png)
Just In Time Compiler as it compiles the instructions “just in time” for the app that is running to use. Powershell is built on top of this framework,each output from a command is a .NET object. The .NET framework enables for abuse of the .NET capabilities. Examples include

- Fileless Execution utilising System.Reflection.Assembly which can load an entire malicious payload into memory
    
- Full access to windows internals (Win32 API)
    
- Evading binary check, does not require powershell.exe to run as it can call upon System.Management.Automation.DLL which will call the [Dynamic Link Libraries](Dynamic%20Link%20Libraries.md) assembly directly without ever using powershell.exe hence evading any detections or blocks specifically looking for powershell.exe.