# How Cmdlet’s work

Cmdlet’s (“command-let”) are a specialized [[SyncFolder/Studied Ideas and Concepts/3. Powershell Investigation/Framework .NET]] class that implements a specific task or operation. To clarify, the “class” defines the structure that must be followed to function within .NET infrastructure (must follow the “formula” imposed by the .NET framework). They follow a verb - noun format such as “Get-Process”. What these cmdlets retrieve aren't just plain text responses but instead objects which contain the attributes. For example with Get-Process each item retrieved has properties like “.CPU” and “.Id” and “.StartTime”. Using pipes (the | symbol) it is possible to pass the results from one cmdlet to another for further processing such as:

```
Get-Process | Where-Object { $_.Name -like “Microsoft*” }
```

With command it will retrieve all the processes and pass objects containing their details. The Where-Object cmdlet will filter these results. The $ sign signifies the start of a variable so that powershell can tell it apart from regular text. When in combination with _ the symbols $_ are a built-in variable that holds the object currently flowing through the pipeline.

Ref: [https://learn.microsoft.com/en-us/powershell/scripting/developer/cmdlet/cmdlet-overview?view=powershell-7.6](https://learn.microsoft.com/en-us/powershell/scripting/developer/cmdlet/cmdlet-overview?view=powershell-7.6)