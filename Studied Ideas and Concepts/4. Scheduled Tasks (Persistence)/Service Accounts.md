## What are they?
A digital identity used by an application software or service to interact with other applications or the operating system.
## Where are they used?
Often used by applications to access databases, run batch jobs/scripts or for accessing other applications. 
## What are gMSA's?
Group managed service accounts are utilised in most standard windows environments. They have the following traits:
- No manual password
- Restricted to where service is allowed to run

| Account Type       | Scope          | Password Management      | Primary Security Risk             |
| ------------------ | -------------- | ------------------------ | --------------------------------- |
| **LocalSystem**    | Local Machine  | N/A (Built-in)           | Full OS Compromise                |
| **Domain User**    | Entire Domain  | **Manual** (Human)       | Kerberoasting / Weak Passwords    |
| **gMSA**           | Group of Hosts | **Automatic** (Windows)  | Misconfigured Permissions         |
| **Cloud Identity** | Cloud Resource | **Automatic** (Provider) | Over-privileged Roles / Key Leaks |

