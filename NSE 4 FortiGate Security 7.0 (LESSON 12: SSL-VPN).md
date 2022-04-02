**What does a VPN do?**

- Extends a private network across a public network
- ~~Protects a network from external attacks~~

**Which statement about SSL VPNs is true?**

- ~~An SSL VPN can be established between workstation and a FortiGate device only.~~
- An SSL VPN can be established between an end-user workstation and a FortiGate device or two FortiGate devices.

Fortinet offers VPN capabilities in the FortiGate Unified Threat Management (UTM) appliance and in the FortiClient Endpoint Security suite of applications. You can install a FortiGate unit on a private network and install FortiClient software on the user’s computer. You can also use a FortiGate unit to connect to the private network instead of using FortiClient software.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/729214/vpn

**A web-mode SSL VPN user connects to a remote web server. What is the source IP address of the HTTP request the web server receives?**

- ~~The remote user IP address~~
- The FortiGate device internal IP address

**Which statement about tunnel-mode SSL VPN is correct?**

- It supports split tunneling.
- ~~It requires bookmarks.~~

**A web-mode SSL VPN user users \_____ to access internal network resources.**

- bookmarks
- ~~FortiClient~~

**Which step is necessary to configure SSL VPN connections?**

- Create a firewall policy from the SSL VPN interface to the internal interface.
- ~~Enable event logs for SSL VPN traffic: users, VPN, and endpoints.~~

**Which action may allow internet access in tunnel mode, if the remote network does not allow internet access to SSL VPN users?**

- ~~Enable split tunneling~~
- Configure the DNS server to use the same DNS server as the client system DNS

**What does the SSL VPN monitor feature allow you to do?**

- ~~Monitor SSL VPN user actions, such as authentication~~
- Force SSL VPN user disconnections

**Which statement about SSL VPN timers is correct?**

- SSL VPN timers can prevent logouts when SSL VPN users experience long network latency.
- ~~The login timeout is a non-customizable hard value.~~

| Parameter | Description | Type | Size | Default |
| --- | --- | --- | --- | --- |
| login-timeout | SSLVPN maximum login timeout. | integer | Minimum value: 10 Maximum value: 180 | 30 |

https://docs.fortinet.com/document/fortigate/7.0.5/cli-reference/363620/config-vpn-ssl-settings

**Which component issues and signs the client certificate?**

- FortiClient EMS
- ~~FortiClient~~

**What does FortiClient EMS integration ensure?**

- Device identification
- ~~User identification~~
