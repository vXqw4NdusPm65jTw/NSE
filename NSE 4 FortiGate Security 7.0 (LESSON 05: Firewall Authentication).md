**Which firewall authentication method does FortiGate support?**

- Local password authentication
- ~~Biometric authentication~~

You can define local users and peer users on the FortiGate unit. You can also define user accounts on remote authentication servers and connect them to FortiOS.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/622284/user-authentication

**Which type of token can generate OTPs to provide two-factor authentication to users in your network?**

- FortiToken Mobile
- ~~USB FortiToken~~

FortiToken is available as either a mobile or a physical (hard) token. Mobile tokens can be purchased as a license, or consumed with points as part of the FortiToken Cloud service. FortiToken Mobile and physical FortiTokens store their encryption seeds on the cloud. FortiToken Mobile seeds are generated dynamically when the token is provisioned. They are always encrypted whether in motion or at rest.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/323465/fortitokens

**When FortiGate uses a RADIUS server for remote authentication, which statement about RADIUS is true?**

- ~~FortiGate must query the remote RADIUS server using the distinguished name (dn).~~
- RADIUS group memberships are provided by vendor-specific attributes (VSAs) configured on the RADIUS server.

|||
| --- | --- |
| **Distinguished Name** | Used to look up user account entries on the LDAP server. It reflects the hierarchy of LDAP database object classes above the CN identifier in which you are doing the lookup. Enter dc=COMPANY,dc=com to specify the root of the domain to include all objects. Enter ou=VPN-Users,dc=COMPANY,dc=com to look up users under a specific organization unit.|

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/102264/configuring-an-ldap-server

Some vendors want or need to send attributes that do not match any of the defined IETF attributes. This can be accomplished by using RADIUS attribute type 26, which allows a vendor to encapsulate their own specific attributes in this standard AVP. In order to support VSAs, the RADIUS server requires a dictionary to define the VSAs. This dictionary is typically supplied by the client or server vendor.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/952303/radius-avps-and-vsas

**What is a valid reply from a RADIUS server to an ACCESS-REQUEST packet from FortiGate?**

- ~~ACCESS-PENDING~~
- ACCESS-REJECT

A second RADIUS server can be configured in the same RADIUS profile so in the event the first RADIUS server does not respond, the second server can be checked. If the first RADIUS server responds with an Access-Reject, no further servers are queried.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/177729/using-multiple-radius-servers

**A remote LDAP user is trying to authenticate with a username and password. How does FortiGate verify the login credentials?**

- ~~FortiGate queries its own database for user credentials.~~
- FortiGate sends the user-entered credentials to the remote server for verification.

When using the GUI, wildcard admin is the only remote admin account that does not require you to enter a password on account creation. That password is normally used when the remote authentication server is unavailable during authentication.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/747268/configuring-wildcard-admin-accounts

**Which statement about guest user groups is true?**

- Guest user group accounts are temporary.
- ~~Guest user group account passwords are temporary.~~

In some scenarios, an administrator might need to create temporary user accounts with a defined expiry time to access network resources.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/29900/user-groups#guest

**Guest accounts are most commonly used for which purposes?**

- ~~To provide temporary visitor access to corporate network resources~~
- To provide temporary visitor access to wireless networks

For example, if there is a large conference and may attendees require temporary network access for a few days.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/29900/user-groups#guest

**Firewall policies dictate whether a user or device can or cannot authenticate on a network. Which statement about firewall authentication is true?**

- Firewall policies can be configured to authenticate certificate users.
- ~~The order of the firewall policies always determines whether a user's credentials are determined actively or passively.~~
