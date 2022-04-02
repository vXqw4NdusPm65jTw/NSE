**If antivirus, grayware, and AI scans are enabled, in what order are they performed?**

- ~~AI scan, followed by grayware scan, followed by antivirus scan~~
- Antivirus scan, followed by grayware scan, followed by AI scan

**Which databases can be manually selected for use in antivirus scanning?**

- Extended and Extreme
- ~~Quick, Normal, and Extreme~~

|||
| --- | --- |
| Extended | This is the default setting. This database includes currently spreading viruses, as determined by the FortiGuard Global Security Research Team, plus recent viruses that are no longer active. These viruses may have been spreading within the last year but have since nearly or completely disappeared. |
| Extreme | This includes the extended database, plus a large collection of zoo viruses. These are viruses that have not spread in a long time and are largely dormant. Some zoo viruses might rely on operating systems and hardware that are no longer widely used. |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/923365/databases

**What three additional features of an antivirus profile are available in proxy-based inspection mode?**

- MAPI, SSH, and CDR
- ~~Full and quick~~

The following table indicates which protocols can be inspected by the designated antivirus scan modes.

|| HTTP | FTP | IMAP | POP3 | SMTP | NNTP | MAPI | CIFS | SSH |
| Proxy | Yes | Yes | Yes | Yes | Yes | Yes | Yes | Yes* | Yes |
| Flow | Yes | Yes | Yes | Yes | Yes | Yes | No | Yes | No |

\* Proxy mode antivirus inspection on CIFS protocol has the following limitations:

- Cannot detect infections within some archive files.
- Cannot detect oversized files.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/836396/antivirus

The following table indicates which Antivirus features are supported by their designated scan modes.

| Part1 | Replacement Message | Content Disarm | Mobile Malware | Virus Outbreak | Sandbox Inspection | NAC Quarantine |
| --- | --- | --- | --- | --- | --- | --- |
| Proxy | Yes | Yes | Yes | Yes | Yes | Yes |
| Flow | Yes* | No | Yes | Yes | Yes | Yes |

\*IPS Engine caches the URL and a replacement message is presented after the second attempt.

| Part 2 | Archive Blocking | Emulator | Client Comforting | Infection Quarantine | Heuristics | Treat EXE as Virus |
| --- | --- | --- | --- | --- | --- | --- |
| Proxy | Yes | Yes | Yes | Yes (1) | Yes | Yes (2) |
| Flow | Yes* | No | Yes | Yes | Yes | Yes (2) |

1. Only available on FortiGate models with HDD or when FortiAnalyzer or FortiGate Cloud is connected and enabled.
2. Only applies to inspection on IMAP, POP3, SMTP, and MAPI protocols.

| Part 3 | External Blocklist | EMS Threat Feed | AI/ML Based Detection | FortiAI Inline Detection |
| --- | --- | --- | --- | --- |
| Proxy | Yes | Yes | Yes | Yes |
| Flow | Yes | Yes | Yes | No |

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/922096/inspection-mode-feature-comparison

**What antivirus database is limited to specific FortiGate models?**

- ~~Extended~~
- Extreme

All FortiGates have the normal antivirus signature database. Some models have additional databases that you can use. The database you use depends on your network and security needs, and on your FortiGate model.

The extended virus definitions database is the default setting and provides comprehensive antivirus protection. Low-end FortiGate models cannot support the extreme database. The FortiGate 300D is the lowest model that supports the extreme database. All VMs support the extreme database. The use-extreme-db setting is only available on models that support the extreme database.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/923365/databases

**What is the default scanning behavior for files over 10 MB?**

- Allow the file without scanning
- ~~Block all large files that exceed the buffer threshold~~

The scan method is determined by the IPS engine algorithm that is based on the type of file being scanned. When handling oversized files in flow-based AV, the action can either be pass (default) or block. When theaction is pass, IPS appends to-be-scan data into the AV scan buffer. If the appended file size exceeds the oversize-limit that is defined in the protocol option profile, then the AV session is cleared and the file is bypassed from AV scanning.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/836396/antivirus

**Which type of inspection mode can be offloaded using NTurbo hardware acceleration?**

- ~~Proxy-based~~
- Flow-based

Some FortiGate models support a feature call NTurbo that can offload flow-based firewall sessions to network processors.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/419589/ips-configuration-options#Hardware

**What does the logging of oversized files option do?**

- Enables logging of all files that cannot be scanned because of oversize limit
- ~~Logs all files that are over 5 MB~~

| Parameter | Description | Type | Size | Default |
| oversize-log | Enable/disable logging for antivirus oversize file blocking. | option | - | disable |

| Option | Description |
| disable | Disable logging for antivirus oversize file blocking. |
| enable | Enable logging for antivirus oversize file blocking. |

https://docs.fortinet.com/document/fortigate/7.0.5/cli-reference/318620/config-firewall-profile-protocol-options

**What command do you use to force FortiGate to check for new antivirus updates?**

- ~~execute update antivirus~~
- execute update-av
