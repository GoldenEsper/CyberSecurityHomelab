New Technology LAN Manager (NTLM) is a set of Microsoft security protocols intended to provide confidentiality, integrity and confidentiality to users. Consists of three messages:

1. Negotiation Message - From Client
2. Challenge Message - From Server
3. Authentication Message - From Server
![](SyncFolder/Images/RegularImages/Pasted%20image%2020260926185356.png)

Here is the NTLM process as described by the crowdstrike page:

NTLM authentication typically follows the following step-by-step process:

1. The user shares their username, password and domain name with the client.
2. The client develops a scrambled version of the password — or hash — and deletes the full password.
3. The client passes a plain text version of the username to the relevant server.
4. The server replies to the client with a challenge, which is a 16-byte random number.
5. In response, the client sends the challenge encrypted by the hash of the user’s password.
6. The server then sends the challenge, response and username to the domain controller (DC).
7. The DC retrieves the user’s password from the database and uses it to encrypt the challenge.
8. The DC then compares the encrypted challenge and client response. If these two pieces match, then the user is authenticated and access is granted.

NTLM only authenticates the client and not the server and relies on password hashing to obfuscate the password.  NTLM has mostly been replaced by [[SyncFolder/Studied Ideas and Concepts/4. LSASS Investigation/Kerberos]]

Weaknesses of NTLM:

- Passwords stored on server and domain controller not salted. This allows attackers with password hash to authenticate.
- Cryptography does not utilise new algorithms that enhance security capabilities

Ref: 

[What is the NTLM (NT LAN Manager) protocol? - IONOS UK](https://www.ionos.co.uk/digitalguide/server/know-how/ntlm-nt-lan-manager/)

[NTLM Explained: Definition, Protocols & More | CrowdStrike](https://www.crowdstrike.com/en-au/cybersecurity-101/identity-security/windows-ntlm/)

[NTLM - Wikipedia](https://en.wikipedia.org/wiki/NTLM)