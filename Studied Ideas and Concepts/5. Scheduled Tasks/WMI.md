## What is it?
The windows management instrumentation serves as the fundamental management infrastructure for Windows OS. It is the implementation of [[CIM]] standard.
## How does it work?
WMI architecture is composed of several layers.
1. At the base is the **WMI repository**, a database that stores all the info about a systems hardware software and configuration. 
2. Above the **WMI repository** is the **WMI Service**. This is the engine that processes requests and manages the repository. When requested it will query the WMI repositiory for information.
3. Finally there is the WMI Provider, Providers are the translators of the WMI world. These sit between the WMI service and the system resource. When query is made it gather the raw data from the hardware and converts into a format that WMI can understand. Essentially allows for the same command to work across different hardware. 
#### How WMI data is structed
All system info is organised in to an **object-oriented** structure. This structure is built upon three concepts.
1. Classes
2. Instances
3. Properties

A class is the blueprint. It essentially defines what things should look like in windows. For example `Win32_Process` defines what a process should look like in windows eg. Process ID, executable path, parent process... other information it should store.

An Instance is the "realisation" of a Class A.K.A it an example of what the class is describing. For example for `Win32_Process` it could be Firefox running. 

Finally Properties are the components that make up the instances. In the example of firefox these properties would be "Process ID, executable path, etc.". What these should be are defined in the class

![](../../Images/RegularImages/Pasted%20image%2020260926191405.png)