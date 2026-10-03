# Overview
[[Kerberoasting]] is a type of [[Active directory]] attack where an attacker seeks to steal credentials from [Service Accounts](../4.%20Scheduled%20Tasks/Service%20Accounts.md) that have a [[Service Principal Name]] (SPN) assigned to them. The ultimate goal is to obtain a high-privilege password hash to escalate privileges within the domain.

## Method of attack
1. **Requesting a Ticket:** The attacker requests a Service Ticket (TGS) from the [Kerberos](../3.%20LSASS%20Investigation/Kerberos.md) Key Distribution Center (KDC) for a specific service account identified by its [[Service Principal Name]]
2. **Encryption:** The KDC issues a TGS that is encrypted with the hash of the service account's password.
3. **Offline Cracking:** The attacker exports the encrypted ticket and moves it to an offline environment to perform a [Brute Force](../4.%20Scheduled%20Tasks/Brute%20Force.md) or dictionary attack against the encrypted hash. If successful, the attacker recovers the cleartext password of the service account.

## Detection
To detect [[Kerberoasting]], security professionals should monitor for anomalous [Kerberos](../3.%20LSASS%20Investigation/Kerberos.md) activity, specifically:
* **[Sysmon](../2.%20Powershell%20Investigation/Sysmon.md) Logs:** Monitor for unusual network traffic patterns or specific authentication events related to service ticket requests.
* **TGS Request Spikes:** An unusual volume of `TGS-REQ` requests from a single workstation or user can indicate an attacker scanning for SPNs.
* **Anomalous Account Activity:** Monitor for service accounts performing authentication patterns that deviate from their normal baseline.

## Mitigations
* Use long, complex, and randomly generated passwords for all [Service Accounts](../4.%20Scheduled%20Tasks/Service%20Accounts.md).
* Implement [[../4. Scheduled Tasks/Service Accounts|Managed Service Accounts]] or Group Managed Service Accounts (gMSAs) to automate password management and reduce the risk of cracking.
* Monitor for unauthorized [[Service Principal Name]] registrations.