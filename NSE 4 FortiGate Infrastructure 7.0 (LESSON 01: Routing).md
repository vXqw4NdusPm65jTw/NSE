**Which objects can you use to create static routes?**

- ISDB objects
- ~~Service objects~~

**When the Stop policy routing action is used in a policy route, which behavior is expected?**

- ~~FortiGate skips over this policy route and tries to match another in the list.~~
- FortiGate routes the traffic based on the regular routing table.

**The Priority attribute applies to which type of routes?**

- Static
- ~~Dynamic~~

| Field | Description |
| --- | --- |
| Priority | In static routes, priorities are 0 by default. When two routes have an equal distance, the route with the lower priority number will take precedence. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/139692/routing-concepts

**Which attribute does FortiGate use to determine the best route for a packet, if it matches multiple dynamic routes that have he same Distance?**

- ~~Priority~~
- Metric

| Field | Description |
| --- | --- |
| Metric | The metric associated with the route type. The metric of a route influences how the FortiGate dynamically adds it to the routing table. The following are types of metrics and the protocols they are applied to: Hop count (Routes learned through RIP), Relative cost (Routes learned through OSPF), Multi-Exit Discriminator (MED) (Routes learned through BGP. By default, the MED value associated with a BGP route is zero. However, the MED value can be modified dynamically. If the value was changed from the default, the Metric column displays a non-zero value.)

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/139692/routing-concepts

**Which static route attribute does not appear on the GUI routing monitor?**

- ~~Distance~~
- Priority

The Static & Dynamic Routing Monitor displays the routing table on the FortiGate, including all static and dynamic routing protocols in IPv4 and IPv6. You can also use this monitor to view policy routes, BGP neighbors and paths, and OSPF neighbors.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/655407/static-dynamic-routing-monitor

**What is the default ECMP method on FortiGate?**

- ~~Weighted~~
- Source IP

| ECMP | SD-WAN (GUI/CLI) | Description |
| --- | --- | --- |
| source-ip-based | Source IP/source-ip-based | Traffic is divided equally between the interfaces. Sessions that start at the same source IP address use the same path. This is the default selection. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/25967/equal-cost-multi-path

**How does FortiGate load balance traffic when using the spillover method in ECMP routing?**

- Sessions are distributed based on interface threshold.
- ~~Sessions are distributed based on route weight.~~

| ECMP | SD-WAN (GUI/CLI) | Description |
| --- | --- | --- |
| usage-based | Spillover/usage-based | The interface is used until the traffic bandwidth exceeds the ingress and egress thresholds that you set for that interface. Additional traffic is then sent through the next interface member. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/25967/equal-cost-multi-path

**What is the default RPF check method on FortiGate?**

- Loose
- ~~Strict~~

Whenever a packet arrives at one of the interfaces on a FortiGate, the FortiGate determines whether the packet was received on a legitimate interface by doing a reverse look-up using the source IP address in the packet header. This protects against IP spoofing attacks. If the FortiGate does not have a route to the source IP address through the interface on which the packet was received, the FortiGate drops the packet as per Reverse Path Forwarding (RPF) check. There are two modes of RPF – feasible path and strict. The default feasible RPF mode checks only for the existence of at least one active route back to the source using the incoming interface. The strict RPF check ensures the best route back to the source is used as the incoming interface.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/139692/routing-concepts

**Which route lookup scenario satisfies the RPF check for a packet?**

- ~~Routing table has an active route for the destination IP of the packet~~
- Routing table has an active route for the source IP of the packet

Whenever a packet arrives at one of the interfaces on a FortiGate, the FortiGate determines whether the packet was received on a legitimate interface by doing a reverse look-up using the source IP address in the packet header. This protects against IP spoofing attacks. If the FortiGate does not have a route to the source IP address through the interface on which the packet was received, the FortiGate drops the packet as per Reverse Path Forwarding (RPF) check. There are two modes of RPF – feasible path and strict. The default feasible RPF mode checks only for the existence of at least one active route back to the source using the incoming interface. The strict RPF check ensures the best route back to the source is used as the incoming interface.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/139692/routing-concepts

**What is the purpose of the link health monitor seeting update-static-route?**

- ~~It creates a new static route for the backup interface.~~
- It removes all static routes associated with the link health monitor's interface.

| Parameter | Description | Type | Size | Default |
| --- | --- | --- | --- | --- |
| update-static-route | Enable/disable updating the static route. | option | - | enable |

| Option | Description |
| --- | --- |
| enable | Enable updating the static route. |
| disable | Disable updating the static route. |

https://docs.fortinet.com/document/fortigate/7.0.5/cli-reference/122620/config-system-link-monitor

**When using link health monitoring, which route attribute must you also configure to achieve route failover protection?**

- Distance
- ~~Metric~~

**What is the distance value for this route?**

**10.200.2.0/24 [110/2] via 10.200.2.254, [25/0]**

- 110
- ~~2~~

**Which CLI commands can you use to view standby and inactive routes?**

- ~~get router info routing-table all~~
- get router info routing-table database

The routing database consists of all learned routes from all routing protocols before they are injected into the routing table. This likely lists more routes than the routing table as it consists of routes to the same destinations with different distances. Only the best routes are injected into the routing table. However, it is useful to see all learned routes for troubleshooting purposes.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/139692/routing-concepts#Viewing

**Which CLI packet capture verbosity level prints interface names?**

- ~~3~~
- 4

|||
| --- | --- |
| \<verbose\> | The level of verbosity as one of: 1 - print header of packets, 2 - print header and data from IP of packets, 3 - print header and data from Ethernet of packets, 4 - print header of packets with interface name |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/680228/performing-a-sniffer-trace-cli-and-packet-capture

----------------------------------------------------------------------------------------------------

**An administrator has configured a strict RPF check on FortiGate. Which statement is true about the strict RPF check?**

- ~~The strict RPF check is run on the first sent and reply packet of any new session.~~
- Strict RPF checks the best route back to the source using the incoming interface.
- ~~Strict RPF checks only for the existence of at least one active route back to the source using the incoming interface.~~
- ~~Strict RPF checks only for the existence of at least one active route back to the source using the incoming interface.~~
- ~~Strict RPF allows packets back to sources with all active routes.~~
