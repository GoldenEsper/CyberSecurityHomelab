## What is it?
It is a virtual collection of policy settings. GPO can represent setting sin the file system/active directory.
![](Images/RegularImages/Pasted%20image%2020260930210324.png)
## How is it created?
Can be made utilising the Group Policy Editor which can be a stand alone tool. 
## What priority does each GPO take?
GPOs are processed in the following order:
1. The local GPO is applied.
2. GPOs linked to sites are applied.
3. GPOs linked to domains are applied.
4. GPOs linked to organizational units are applied. For nested organizational units, GPOs linked to parent organizational units are applied before GPOs linked to child organizational units are applied.
At each application process it overwrites the previous. 

Source: https://learn.microsoft.com/en-us/previous-versions/windows/desktop/policy/group-policy-objects