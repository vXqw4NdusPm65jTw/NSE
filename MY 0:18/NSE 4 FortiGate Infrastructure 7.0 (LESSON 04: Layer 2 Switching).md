**Which mode must the FortiGate VDOM be operating in, to route traffic between VLANs?**

- ~~Transparent mode~~
- NAT mode

In NAT mode, the FortiGate unit functions as a layer-3 device. In this mode, the FortiGate unit controls the flow of packets between VLANs and can also remove VLAN tags from incoming VLAN packets. The FortiGate unit can also forward untagged packets to other networks such as the Internet.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/402940/vlans

**Which statement about FortiGate operating in transparent mode is true?**

- It has a management IP address.
- ~~Each interface has its own IP address.~~

When you add a FortiGate that is in transparent mode to a network, it only needs to be provided with a management IP address in order to access the device. It is recommended that a dedicated interface is used to connect to the management network in transparent mode.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/617430/system

**How can an administrator configure FortiGate to have four interfaces in the same broadcast domain?**

- ~~Create a firewall policy on each of the four interfaces~~
- Configure the operation mode as transparent and use the same forward domain ID.

**Which configuration setting must be enabled to allow VLAN-tagged traffic through a virtual wire pair?**

- ~~Transparent bridging~~
- Wildcard VLAN

**How is traffic handled in a virtual wire pair?**

- Incoming traffic to one interface is always forwarded out through the other interface.
- ~~Traffic is forwarded based on the destination MAC address.~~

A virtual wire pair consists of two interfaces that do not have IP addressing and are treated like a transparent mode VDOM. All traffic received by one interface in the virtual wire pair can only be forwarded to the other interface, provided a virtual wire pair firewall policy allows this traffic. Traffic from other interfaces cannot be routed to the interfaces in a virtual wire pair.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/166804/virtual-wire-pair

**In which operating mode is the software switch function supported?**

- ~~Transparent mode~~
- NAT mode

**Which interface can be a member of a software switch?**

- ~~VLAN interface~~
- Wireless interface

|||
| --- | --- |
| Interface Members | This section can have different formats depending on the Type. Members can be selected for some interface types: - Software Switch or Hardware Switch: Specify the physical and wireless interfaces joined into the switch. - 802.3ad Aggregate or Redundant Interface: This field includes the available and selected interface lists.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/574723/interface-settings

**What is the default STP mode for FortiGate?**

- ~~FortiGate passively forwards BPDUs.~~
- FortiGate has all STP functions disabled.
