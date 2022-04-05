**In FSSO, FortiGate allows network access based on \_____.**

- ~~Active user authentication with username and password~~
- Passive user identification by user ID, IP address, and group membership

When a user logs on at a workstation in a monitored domain, FSSO:

- Detects the logon event and records the workstation name, domain, and user,
- Resolves the workstation name to an IP address,
- Determines which user groups the user belongs to,
- Sends the user logon information, including IP address and groups list, to the FortiGate unit, and
- Creates one or more log entries on the FortiGate unit for this logon event as appropriate.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/450337/fsso

**Which working mode is used for monitoring user sign-on activities in Windows AD?**

- Polling mode (collector agent-based or agentless)
- ~~eDirectory agent mode~~

The Collector Agent (CA) is installed as a service on a server in the Windows AD network to monitor user logons and send the required information to the FortiGate unit. The Collector agent can collect information from a DC agent (Windows AD) and TS agent (Citrix or VMware Horizon Terminal Server).

For Windows AD networks, FortiGate devices can also provide SSO capability by directly polling Windows Security Event log entries on Windows DC for user log in information.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/450337/fsso

**Which is the recommended mode for FSSO deployments?**

- DC agent mode
- ~~Polling mode: Agentless~~

**Which FSSO mode requires more FortiGate system resources (CPU and RAM)?**

- ~~Polling mode: Collector agent-based~~
- Polling mode: Agentless

**What may cause an NTLM authentication to occur?**

- ~~Traffic coming from an IP on the FSSO user list~~
- Traffic coming from an IP not on the FSSO user list

**When performing NTLM authentication, what information does the web browser supply to FortiGate?**

- The user's credentials (username and password)
- ~~The user's user ID, IP address, and group membership~~

**If you have collector agents using either the DC agent mode or the collector agent-based polling mode, which fabric connector should you select on FortiGate?**

- ~~Poll Active Directory Server~~
- Fortinet Single Sign-On Agent

Fortinet single sign-on agent

- For most FSSO Agent-based deployments, this connector option will be used. Specify either Collector Agent or Local as User Group Source to collect user groups from the Collector Agent, or to match users to user groups from a LDAP server.

Poll Active Directory server

- This connection option directly polls Windows Security Event log entries on Windows DC for user log in information.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/450337/fsso

**Which naming conventions does the FSSO collector agent use to access the Windows AD in Standard access mode?**

- Windows convention - NetBios: Domain\groups
- ~~LDAP convention: CN=User,OU=Name,DC=Domain~~

**Which logging level shows the login events on the collector agent?**

- Information
- ~~Warning~~

**The command diagnose debug fsso-polling detail displays information for which mode of FSSO?**

- Agentless polling
- ~~Collector agent-based polling~~
