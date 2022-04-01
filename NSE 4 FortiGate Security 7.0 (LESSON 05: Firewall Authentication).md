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

Some vendors want or need to send attributes that do not match any of the defined IETF attributes. This can be accomplished by using RADIUS attribute type 26, which allows a vendor to encapsulate their own specific attributes in this standard AVP. In order to support VSAs, the RADIUS server requires a dictionary to define the VSAs. This dictionary is typically supplied by the client or server vendor.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/952303/radius-avps-and-vsas
