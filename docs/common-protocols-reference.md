# Common Protocols Reference

| Protocol | Purpose | Common Port or Identifier |
|---|---|---|
| ARP | Maps IPv4 addresses to MAC addresses | No TCP/UDP port |
| ICMP | Reachability and error reporting | IP protocol 1 |
| ICMPv6 | IPv6 control and error reporting | IP protocol 58 |
| DNS | Name resolution | UDP/TCP 53 |
| DHCP | Dynamic IPv4 configuration | UDP 67/68 |
| HTTP | Unencrypted web traffic | TCP 80 |
| HTTPS | Encrypted web traffic | TCP 443 |
| TLS | Encryption for application traffic | Commonly TCP 443 |
| SSH | Secure remote administration | TCP 22 |
| SMTP | Sending email | TCP 25, 465, 587 |
| IMAP | Retrieving email | TCP 143, 993 |
| SMB | Windows file sharing | TCP 445 |
| RDP | Windows remote desktop | TCP/UDP 3389 |
| LDAP | Directory services | TCP/UDP 389 |
| LDAPS | Encrypted directory services | TCP 636 |
| NTP | Time synchronization | UDP 123 |
| SNMP | Network monitoring | UDP 161/162 |

## Reminder

A port number can suggest the expected service, but the packet contents and context should be reviewed before drawing conclusions.
