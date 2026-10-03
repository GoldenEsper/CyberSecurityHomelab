## What is it?
It is a framework used to define security constraints on a computer or workstation that is NOT part of an [Active directory](../1.%20Active%20Directory%20Attacks/Active%20directory.md) domain. It's kind like the rulebook that tells the system how to handle identities and what users are allowed to perform including what actions are recorded in security logs.
## What is it made up of?
 - Account policies - Settings that govern security requirements of a user account. (eg. password lockout)
 - Local Policies - Settings that govern how system behaves and how a user interacts with it. (eg. audit policy, user rights assignments for groups, security options)
## Methods of interacting
- Usage of `secpol.msc` for manual configuration for individual machines. 
- Command line utilising `secedit` tool. `secedit.exe` used to configure and analyse setting via command line. Can export in `.inf` file edit the file then import back in.
## Local Security Policy vs Group Policy Objects
In the event of conflict between LSP and [GPO](GPO.md) the GPO always wins. Eg. if local machine has 10 character password min but domain GPO requires 14 the machine will enforce 14.