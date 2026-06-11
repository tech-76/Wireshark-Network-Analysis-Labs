# Lab 07: Network Troubleshooting Scenarios

## Overview

This lab provides common Wireshark-based troubleshooting scenarios for IT support practice.

Each scenario connects user symptoms, command-line tests, Wireshark filters, possible findings, and ticket-style documentation.

## Scenario 1: Websites Do Not Load by Name

### User Report

```text
Wi-Fi is connected, but websites do not load.
```

### Commands

```cmd
ipconfig /all
ping 8.8.8.8
ping google.com
nslookup google.com
```

### Wireshark Filter

```text
dns
```

### Possible Findings

| Finding | Possible Cause |
|---|---|
| Can ping 8.8.8.8 but DNS fails | DNS issue |
| DNS query with no response | DNS server unreachable |
| NXDOMAIN | Domain does not exist |

### Ticket-Style Note

```text
User could ping public IP address but could not resolve domain names.
Captured DNS traffic and observed queries without responses.
Confirmed likely DNS issue and escalated for DNS server review.
```

## Scenario 2: Device Gets 169.254.x.x Address

### User Report

```text
Computer says connected but has no internet.
```

### Commands

```cmd
ipconfig /all
ipconfig /release
ipconfig /renew
```

### Wireshark Filter

```text
dhcp
```

### Possible Findings

| Finding | Possible Cause |
|---|---|
| DHCP Discover repeats | DHCP server not responding |
| Discover, Offer, Request, ACK visible | DHCP process works |
| No DHCP traffic | Wrong interface or static IP |

### Ticket-Style Note

```text
Device had APIPA address in 169.254.x.x range.
Captured DHCP traffic and observed repeated Discover packets without Offer.
Escalated to network team for DHCP scope or switch port review.
```

## Scenario 3: Internal Website Does Not Open

### Commands

```cmd
nslookup internal-site.company.local
ping internal-site.company.local
tracert internal-site.company.local
```

### Wireshark Filters

```text
dns
tcp.port == 443
```

### Possible Findings

| Finding | Possible Cause |
|---|---|
| Internal DNS fails | VPN or DNS issue |
| Repeated SYN packets | Firewall, routing, or server issue |
| TLS alert | Certificate or TLS issue |

### Ticket-Style Note

```text
User could access public websites but not internal site.
Internal DNS failed while VPN was disconnected.
User connected VPN and internal DNS resolved successfully.
Internal website loaded after VPN connection.
Ticket resolved.
```

## Scenario 4: Website Is Slow

### Commands

```cmd
ping website.com
tracert website.com
nslookup website.com
```

### Wireshark Filters

```text
tcp.analysis.retransmission
tcp.port == 443
dns
```

### Possible Findings

| Finding | Possible Cause |
|---|---|
| TCP retransmissions | Packet loss or unstable network |
| Slow DNS response | DNS delay |
| Long TCP handshake | Latency or server delay |

### Ticket-Style Note

```text
User reported slow website loading.
Captured traffic and observed TCP retransmissions during HTTPS connection.
Ping showed intermittent packet loss.
Escalated to network team with destination and timestamps.
```

## Scenario 5: VPN Connects but Shared Drive Fails

### Commands

```cmd
ipconfig /all
nslookup fileserver01.company.local
ping fileserver01.company.local
```

### Wireshark Filter

```text
dns
```

### Possible Findings

| Finding | Possible Cause |
|---|---|
| Internal DNS fails | VPN DNS issue |
| DNS works but ping fails | Firewall or routing issue |
| Name works but access denied | Permission issue |

### Ticket-Style Note

```text
VPN client showed connected, but shared drive failed.
Checked VPN adapter and internal DNS resolution.
Internal hostname failed before reconnecting VPN.
After reconnecting VPN, internal DNS resolved and shared drive opened.
Ticket resolved.
```

## Skills Demonstrated

- Scenario-based troubleshooting
- DNS and DHCP analysis
- TCP connection review
- VPN support awareness
- Ticket documentation
