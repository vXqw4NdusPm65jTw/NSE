**In FSSO, FortiGate allows network access based on \_____.**

- ~~Active user authentication with username and password~~
- Passive user identification by user ID, IP address, and group membership

**Which working mode is used for monitoring user sign-on activities in Windows AD?**

- Polling mode (collector agent-based or agentless)
- ~~eDirectory agent mode~~

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

**Which naming conventions does the FSSO collector agent use to access the Windows AD in Standard access mode?**

- Windows convention - NetBios: Domain\groups
- ~~LDAP convention: CN=User,OU=Name,DC=Domain~~

**Which logging level shows the login events on the collector agent?**

- Information
- ~~Warning~~

**The command diagnose debug fsso-polling detail displays information for which mode of FSSO?**

- Agentless polling
- ~~Collector agent-based polling~~
