**Which IPS action allows traffic and logs the activity?**

- ~~Allow~~
- Monitor

**Which IPS component is updated most frequently?**

- ~~Protocol decoders~~
- IPS signature database

**Which behavior is a characteristic of a DoS attack?**

- ~~Attempts to exploit a known application vulnerability~~
- Attempts to overload a server with TCP SYN packets

**Which DoS anomaly sensor can be used to detect and block the probing attempts of a port scanner?**

- ~~tcp_syn_flood~~
- tcp_port_scan

**WAF protocol contraints protect against which type of attacks?**

- Buffer overflow
- ~~ICMP Sweep~~

**To use the WAF feature, which inspection mode should be used in the firewall policy?**

- ~~Flow~~
- Proxy

| UTM Profile | Flow Mode Inspection Policy (GUI/CLI) | Proxy Mode Inspection Policy (GUI/CLI) | Feature set option |
| --- | --- | --- | ---|
| Web Application Firewall | No/No | Yes/Yes | N/A |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/922096/inspection-mode-feature-comparison

**Which chipset uses NTurbo to accelerate IPS sessions?**

- ~~CP9~~
- SoC4

**Which feature requires full SSL inspection to maximize its detection capability?**

- WAF
- ~~DoS~~

**Which FQDN does FortiGate use to obtain IPS updates?**

- update.fortiguard.net
- ~~service.fortiguard.com~~

To verify FortiGuard connectivity in the CLI:

- execute ping service.fortiguard.net
- execute ping update.fortiguard.net

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/703926/verifying-connectivity-to-fortiguard

**When IPS fail open is triggered, what is the expected behavior, if the IPS fail-open option is set to enabled.**

- New packets pass through without inspection
- ~~New packets dropped~~

When enabled, the IPS engine fails open, and it affects all protocols inspected by FortiOS IPS protocol decoders, including but not limited to HTTP, HTTPS, FTP, SMTP, POP3, IMAP, and so on. When the IPS engine fails open, traffic continues to flow without IPS scanning.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/419589/ips-configuration-options#Fail-open

**Type: Signature, Action: Block, Packet logging: Enable, Status: Enable, Rate-based settings: Default, Exempt IPs: 0. Review the Intrusion Prevention System (IPS) profile signature settings. Which statement is correct in adding the FTP.Login.Failed signature to the IPS sensor profile?**

- Traffic matching the signature will be silently dropped and logged.
- ~~The signature setting uses a custom rating threshold.~~
- ~~The signature setting includes a group of other signatures.~~
- ~~Traffic matching the signature will be allowed and logged.~~

Each IPS signature comes with a default action such as Block and Pass. In some scenarios, you may want to override this action. You can override a set of IPS filter or signatures. By default, a set of IPS filter or signatures has an action of Default, which applies a signature’s default action when the signature is matched. By changing the action, you can override the setting for all signatures within the filter or signature set.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/213498/signature-based-defense#Custom/p
