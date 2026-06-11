# Wireshark Display Filters Cheatsheet

## Overview

This cheatsheet lists common Wireshark display filters used for network troubleshooting and packet analysis.

## Basic Protocol Filters

| Purpose | Filter |
|---|---|
| ICMP / Ping | `icmp` |
| DNS | `dns` |
| DHCP | `dhcp` |
| DHCP older filter | `bootp` |
| TCP | `tcp` |
| UDP | `udp` |
| HTTP | `http` |
| HTTPS/TLS | `tls` |
| ARP | `arp` |
| SMB | `smb` or `smb2` |

## IP Address Filters

```text
ip.addr == 192.168.1.10
ip.src == 192.168.1.10
ip.dst == 192.168.1.1
ip.addr != 192.168.1.10
```

## Port Filters

```text
tcp.port == 443
udp.port == 53
tcp.srcport == 443
tcp.dstport == 443
```

## Common Service Filters

| Service | Filter |
|---|---|
| DNS | `udp.port == 53` |
| HTTP | `tcp.port == 80` |
| HTTPS | `tcp.port == 443` |
| SSH | `tcp.port == 22` |
| SMTP | `tcp.port == 25` |
| SMTP Submission | `tcp.port == 587` |
| IMAP | `tcp.port == 143` |
| IMAPS | `tcp.port == 993` |
| SMB | `tcp.port == 445` |
| RDP | `tcp.port == 3389` |

## TCP Troubleshooting Filters

```text
tcp.flags.syn == 1
tcp.flags.syn == 1 and tcp.flags.ack == 0
tcp.flags.reset == 1
tcp.analysis.retransmission
tcp.analysis.duplicate_ack
tcp.analysis.lost_segment
tcp.analysis.flags
```

## DNS Filters

```text
dns
dns.flags.response == 0
dns.flags.response == 1
dns.qry.name contains "example.com"
dns.flags.rcode != 0
```

## DHCP Filters

```text
dhcp
bootp
udp.port == 67
udp.port == 68
```

## HTTP Filters

```text
http
http.request.method == "GET"
http.request.method == "POST"
http.response.code == 404
http.response.code >= 500
```

## TLS Filters

```text
tls
tls.handshake
tcp.port == 443
```

## Combining Filters

AND:

```text
ip.addr == 192.168.1.10 and dns
```

OR:

```text
dns or icmp
```

NOT:

```text
not arp
```

## Example Documentation

```text
Filter used: dns
Reason: User reported websites not loading by name.
Finding: DNS queries were sent, but no DNS responses were received.
Conclusion: Possible DNS server issue.
```

## Skills Demonstrated

- Wireshark display filters
- Protocol filtering
- DNS and DHCP analysis
- TCP troubleshooting
- Network documentation
