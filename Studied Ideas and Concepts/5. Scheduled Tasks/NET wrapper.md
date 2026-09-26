## What is it?
A wrapper is used to provide a simpler interface with complex code. A .NET wrapper is just a simpler interface for code within [[SyncFolder/Studied Ideas and Concepts/3. Powershell Investigation/Framework .NET|.NET]] infrastructure.
## Why use it?
There are three main reasons for using a “wrapper” are as follows

- Adapt code inputs to allow two pieces to interface with each other.
- Allow for simpler interface with lower level operations
- Abstract code execution and possibly reduce visibility to some security controls
## Analogy
It's like an automatic car compared with a manual transmission car. For an automatic car there is a “wrapper” that acts as an intermediary between the driver and the transmission. There is still a transmission that has manual gears however the “wrapper” handles the translation.

## Use in cybersecurity
Wrappers essentially expose a different interface to calling applications which hides the complexity of the core program. The wrapper can also enable a program to indirectly interact with sensitive libraries, [[API|API's]], or system functionality by interacting through the .NET layer. This can modify the “execution chain” making the behavior less apparent.

![[SyncFolder/Images/RegularImages/Designer.jpg]]