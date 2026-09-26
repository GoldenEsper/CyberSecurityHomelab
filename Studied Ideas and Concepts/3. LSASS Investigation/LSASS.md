LSASS (Local Security Authority Subsystem Service) is a windows process for authentication, authorization, credential management and stores credentials in memory. During the user logon process (WinLogon) sends credential information to LSASS.exe for verification. LSASS validates creds against the correct authority:

- Security Accounts Manager (SAM) Database for local or
- Domain Controller for domain accounts

Following a successful login LSASS generates access tokens containing the users security identifier. It also caches credential types in memory including [[NTLM]] pass hashes, [[Kerberos]] ticket grant tickets and service tickets. The caching enables single sign-on functionality. Microsoft implements protected process technology to shield LSASS from unauthorized access. Administrative access can still bypass the protections.

Ref: https://en.wikipedia.org/wiki/Local_Security_Authority_Subsystem_Service