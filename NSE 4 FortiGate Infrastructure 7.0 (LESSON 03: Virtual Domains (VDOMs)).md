**Which traffic is always generated from the management VDOM?**

- ~~Link Health Monitor~~
- FortiGuard

**Which statement about the management VDOM is true?**

- ~~It is root by default and cannot be changed in multi-vdom mode.~~
- It is root by default, but can be changed to any VDOM in multi-vdom mode.

**Which type of administrator can make changes to all VDOMs?**

- ~~A custom VDOM administrator~~
- An administrator with the super_admin profile

To assign an administrator to multiple VDOMs, they must be created at the global level. When creating an administrator at the VDOM level, the super_admin administrator profile cannot be used.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/719410/create-per-vdom-administrators

**Which statement about VDOM administrators is true?**

- ~~There can be only one administrator per VDOM.~~
- Each VDOM can have multiple administrators.

**Which configuration settings are global settings?**

- ~~Firewall policies~~
- FortiGuard settings

**Which configuration settings are per-VDOM settings?**

- ~~Host name~~
- NGFW mode

**What is a requirement for creating an inter-VDOM link between two VDOMs?**

- ~~The NGFW mode of at least one VDOM must be profile based.~~
- At least one of the VDOMs must be operating in NAT mode.

In this example, both VDOM-A and VDOM-B use NAT mode.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/806116/nat-mode

In this example, VDOM-A uses NAT mode and VDOM-B uses transparent mode.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/986787/nat-and-transparent-mode

**Which type of VDOM link requires that both sides of the link be assigned an IP address within the same subnet?**

- ~~NAT-to-transparent~~
- NAT-to-NAT

**Of these options, what is a possible reason why an administrator might not be able to gain access to a specific VDOM?**

- The administrator is using an IP address that is not specified as a trusted host.
- ~~The administrator is using the super_admin profile.~~

**Which troubleshooting tool is most suitable when trying to verify the firewall policy used by an inter-VDOM link?**

- ~~Sniffer trace~~
- Packet flow trace
