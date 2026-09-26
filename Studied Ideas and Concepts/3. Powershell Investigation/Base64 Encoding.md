Base64 encoding maps 64 characters to numbers 0-63 which can then be converted to binary. The encoding can be seen in the table below. 
![](SyncFolder/Images/RegularImages/Pasted%20image%2020260926185027.png)

This process is often used when there is a need to encode binary data. There are wide applications for this technology but in this instance it can be used to obfuscate an attack by converting scripts into binary data that is represented by text. 

For example the command:

Write-Output "Hello World"

Would become:

V3JpdGUtT3V0cHV0ICJIZWxsbyBXb3JsZCI=

Ref: [https://en.wikipedia.org/wiki/Base64](https://en.wikipedia.org/wiki/Base64)