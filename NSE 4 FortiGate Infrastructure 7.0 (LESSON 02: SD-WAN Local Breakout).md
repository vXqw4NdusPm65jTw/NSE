**Which configuration task is correct when implementing SD-WAN?**

- Configure a default route using the SD-WAN virtual interface.
- ~~Configure firewall policies for each individual member interface.~~

You must configure a default route for the SD-WAN. The default gateways for each SD-WAN member interface do not need to be defined in the static routes table. FortiGate will decide what route or routes are preferred using Equal Cost Multi-Path (ECMP) based on distance and priority.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/626338/adding-a-static-route

**Which method of load balancing is supported by SD-WAN but not supported by ECMP routing?**

- ~~Sessions~~
- Volume

| ECMP | SD-WAN (GUI/CLI) | Description |
| --- | --- | --- |
| Not supported | Volume/measured-volume-based | This mode is supported in SD-WAN only. The workload is distributed based on the number of packets that are going through the interface. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/25967/equal-cost-multi-path

**Which link attribute is used in SD-WAN link quality measurements?**

- ~~Cost~~
- Latency

Performance SLA link health monitoring measures the health of links that are connected to SD-WAN member interfaces by either sending probing signals through each link to a server, or using session information that is captured on firewall policies (see Passive WAN health measurement for information), and measuring the link quality based on latency, jitter, and packet loss.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/580649/link-health-monitor

**Which status check protocol is available only on the CLI?**

- TCP-Echo
- ~~HTTP~~

You can configure the protocol that is used for status checks, including: Ping, HTTP, DNS, TCP echo, UDP echo, two-way active measurement protocol (TWAMP), TCP connect, and FTP. In the GUI, only Ping, HTTP, and DNS are available.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/580649/link-health-monitor

**You can configure SD-WAN rules to choose the egress interface based on which parameter?**

- ~~Weight~~
- Latency

When using Best Quality mode, SD-WAN will choose the best link to forward traffic by comparing the link-cost-factor, selected from one of the following:

| GUI | CLI | Description |
| --- | --- | --- |
| Latency | latency | Select a link based on latency. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/022371/best-quality-strategy

**What is an SD-WAN rule matching parameter for traffic sources?**

- User groups
- ~~IPS signature~~

**Which monitor should you use to monitor the session distribution across the SD-WAN member interfaces?**

- ~~SD-WAN Link Status monitor~~
- SD-WAN Usage monitor

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/241925/using-the-sd-wan-monitor

**When verifying SD-WAN traffic routing with the CLI packet capture tool, which verbosity level should you use?**

- ~~1~~
- 4

|||
| --- | --- |
| \<verbose\> | The level of verbosity as one of: 1 - print header of packets, 2 - print header and data from IP of packets, 3 - print header and data from Ethernet of packets, 4 - print header of packets with interface name |
