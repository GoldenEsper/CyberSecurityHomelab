## What is it?
`netapi32.dll` is a windows system [DLL](../2.%20Powershell%20Investigation/Dynamic%20Link%20Libraries.md)] that exposes Microsoft's Network Management API. Primarily provides network management functionality such as providing information on user accounts, groups, domain information, computer information etc.

## Why would an attacker use it

`netapi32.dll` allows for the following uses:

| Use                        | Relevant API                              | Potential attacker purpose                                                      |
| -------------------------- | ----------------------------------------- | ------------------------------------------------------------------------------- |
| Account discovery          | NetUserEnum                               | Discover local or remote user accounts                                          |
| Share discovery            | NetShareEnum                              | Identify accessible network shares                                              |
| Session discovery          | NetSessionEnum                            | Identify users/computers connected to a server                                  |
| Network resource discovery | Network Management APIs                   | Build an understanding of the Windows/network environment                       |
| Share manipulation         | NetShareAdd, NetShareDel, NetShareSetInfo | Modify shared resources where permissions allow                                 |
| Legacy scheduled execution | NetScheduleJobAdd                         | Historically submit scheduled jobs when appropriate privileges are already held |
As `netapi32.dll` is part of the Win32 [API](API.md) it is an example of "living of the land". Utilising `netapi32.dll` is not malicious in itself and as such, often it required to use context based detections.

`netapi32.dll` can also be used for scheduling tasks. This is expanded on in [Legacy NET Schedule service](Legacy%20NET%20Schedule%20service.md)
