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

| Setting | Description |
| --- | --- |
| Certificate | If using HTTPS protocol support, select the local certificate to use for authentication. This is available only if HTTPS and/or Redirect HTTP Challenge to a Secure Channel (HTTPS) are selected. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/709376/authentication-settings

**Which statement about active authentication is true?**

- ~~Active authentication is always used before passive authentication.~~
- The firewall policy must allow the HTTP, HTTPS, FTP, and/or Telnet protocols in order for the user to be prompted for credentials.

| Setting | Description |
| --- | --- |
| Protocol Support | Select the protocols to challenge during firewall user authentication. When you enable user authentication within a security policy, the authentication challenge is normally issued for any of four protocols, depending on the connection protocol: HTTP (you can set this to redirect to HTTPS), HTTPS, FTP, Telnet. The protocols selected here control which protocols support the authentication challenge. Users must connect with a supported protocol first so they can subsequently connect with other protocols. If HTTPS is selected as a protocol support method, it allows the user to authenticate with a customized local certificate. When you enable user authentication within a security policy, FortiOS challenges the security policy user to authenticate. For user ID and password authentication, the user must provide their username and password. For certificate authentication (HTTPS or HTTP redirected to HTTPS only), you can install customized certificates on the unit and the user can also install customized certificates on their browser. Otherwise, users see a warning message and must accept a default Fortinet certificate. The network user's web browser may deem the default certificate invalid. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/709376/authentication-settings

**Which statement about captive portal is true?**

- ~~Captive portal must be hosted on a FortiGate device.~~
- Captive portal exempt specific devices from authenticating.

|||
| --- | --- |
| Security Mode | Enable/disable captive portal authentication for this interface. After enabling captive portal authentication, you can configure the authentication portal, user and group access, custom portal messages, exempt sources and destinations/services, and redirect after captive portal. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/574723/interface-settings

**Which statement best describes the authentication idle timeout feature on FortiGate?**

- ~~The length of time FortiGate waits for the user to enter their authentication credentials~~
- The length of time an authenticated user is allowed to remian authenticated without any packets being generated by the host device

| Setting | Description |
| --- | --- |
| Authentication Timeout | Enter the desired timeout in minutes. You can enter a number between 1 and 1440 (24 hours). The authentication timeout controls how long an authenticated connection can be idle before the user must reauthenticate. The default value is 5. |

**Which command would you use to identify the IP addresses of all authenticated users?**

- ~~diagnose firewall auth clear~~
- diagnose firewall auth list

\# diagnose firewall auth list

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/879357/firewall-users-monitor
