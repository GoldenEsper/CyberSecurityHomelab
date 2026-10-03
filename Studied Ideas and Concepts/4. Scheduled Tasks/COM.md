## What is it?
The **component object model** is a framework developed by Microsoft to enable different software components to interact with each other. It is only available on Microsoft Windows and Apple's Core Foundation 1.3 
## How does it work?
COM utilises what is known as COM objects to allow of programs written in different languages to interact with one another. This allows for reusable code components that can be integrated larger applications. 

COM interfaces are utilised to access the fields that a COM object holds. Clients must request an interface to gain access to the object.
## What is it's replacement?
The [.NET Framework](../2.%20Powershell%20Investigation/Framework%20.NET)] is replacing COM. However COM objects can still be accessed via .NET language via the tool COM interop which adds a [NET wrapper](NET%20wrapper.md). 