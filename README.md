# Wireshark Network Analysis Labs

## Overview

This repository contains practical Wireshark network analysis labs for IT support, help desk, junior network administrator, and entry-level cybersecurity awareness practice.

The goal is to show the ability to capture traffic, apply filters, understand common network protocols, document findings, and troubleshoot issues using a structured process.

## Important Ethical Use Note

Use Wireshark only on systems and networks you own or have permission to monitor. Packet captures may contain sensitive information such as IP addresses, hostnames, cookies, internal systems, and user activity. Do not capture or share traffic without authorization.

## Repository Contents

| File | Description |
|---|---|
| `lab-01-icmp-ping-analysis.md` | Capture and analyze ping traffic |
| `lab-02-dns-query-analysis.md` | Analyze DNS queries and responses |
| `lab-03-dhcp-dora-analysis.md` | Review DHCP Discover, Offer, Request, and ACK |
| `lab-04-tcp-handshake-analysis.md` | Analyze the TCP three-way handshake |
| `lab-05-http-traffic-analysis.md` | Review basic HTTP request and response traffic in a lab |
| `lab-06-https-tls-analysis.md` | Identify HTTPS/TLS handshake traffic |
| `lab-07-network-troubleshooting-scenarios.md` | Practice common support troubleshooting scenarios |
| `wireshark-display-filters-cheatsheet.md` | Common Wireshark filters for troubleshooting |
| `lab-report-template.md` | Reusable template for documenting lab results |

## Recommended Lab Environment

```text
Computer: Windows, macOS, or Linux
Tool: Wireshark
Optional VM: Ubuntu, Kali Linux, or Windows test VM
Network: Private home lab or authorized training network
```

## Basic Wireshark Workflow

1. Open Wireshark.
2. Select the correct network interface.
3. Start capture.
4. Reproduce the network activity.
5. Stop capture.
6. Apply display filters.
7. Review packet details.
8. Document findings.
9. Save the capture only if allowed.

## Common Filters

```text
icmp
dns
dhcp
tcp
udp
http
tls
ip.addr == 192.168.1.10
tcp.port == 443
udp.port == 53
```

## Skills Demonstrated

- Wireshark packet capture
- Network troubleshooting
- DNS and DHCP analysis
- ICMP ping analysis
- TCP handshake review
- HTTP and HTTPS traffic awareness
- Display filter usage
- Technical documentation
- Ethical security awareness
