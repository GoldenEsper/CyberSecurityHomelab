# What are the best methods to protect against [[LSASS]] attack?

1. The best method to protect against this attack is to ensure that admin accounts are correctly secured as this attack method requires a privileged account to access. 
2. In addition ensuring that RunAsPPL (Privileged Process Integrity) is enabled. This can be checked in the [[../2. Powershell Investigation/Registry]] under the local security authority registry:  
```
    HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa\RunAsPPL  
    This setting protects LSASS and other critical processes. 
```
3. Finally, user training to ensure that credential overlap is reduced for multiple accounts
4. Utilising [[Credential Guard]] to isolate secrets in memory. Credential guard places sensitive data in its own virtualised section of memory that is not accessible from the OS. This isolated section of memory does not host any device drivers; it only hosts binaries that are needed for security, nothing else. 
    

Ref: 

[Privileged Process Integrity, Mitigation M1025 - Enterprise | MITRE ATT&CK®](https://attack.mitre.org/mitigations/M1025/)