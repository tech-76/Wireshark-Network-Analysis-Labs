# Wireshark Network Analysis Labs

A hands-on portfolio project focused on packet capture, protocol analysis, network troubleshooting, and technical documentation using Wireshark.

This repository is designed to demonstrate a structured approach to analyzing common network protocols and investigating support-style connectivity problems in a controlled lab environment.

> **Portfolio note:** All activities in this repository are educational lab exercises. They do not represent production network administration or paid enterprise experience.

## Skills Demonstrated

- Wireshark packet capture and display filters
- ICMP, DNS, DHCP, ARP, TCP, HTTP, HTTPS/TLS, and IPv6 fundamentals
- Packet-level troubleshooting
- TCP connection analysis
- DNS and DHCP failure investigation
- Identification of retransmissions, resets, and error messages
- Evidence-based technical documentation
- Security, privacy, and ethical packet-capture practices

## Repository Structure

```text
```text
wireshark-network-analysis-labs/
├── README.md
├── LICENSE
├── ROADMAP.md
├── FILE-MANIFEST.md
├── .gitignore
│
├── docs/
│   ├── lab-environment-and-tools.md
│   ├── wireshark-installation-guide.md
│   ├── packet-capture-safety-and-privacy.md
│   ├── network-analysis-methodology.md
│   ├── wireshark-display-filters-cheatsheet.md
│   ├── common-protocols-reference.md
│   └── glossary.md
│
├── labs/
│   ├── fundamentals/
│   │   ├── lab-01-icmp-ping-analysis.md
│   │   ├── lab-02-dns-query-analysis.md
│   │   ├── lab-03-dhcp-dora-analysis.md
│   │   ├── lab-04-tcp-handshake-analysis.md
│   │   ├── lab-05-http-traffic-analysis.md
│   │   └── lab-06-https-tls-analysis.md
│   │
│   └── intermediate/
│       ├── lab-07-arp-resolution-analysis.md
│       ├── lab-08-tcp-retransmission-analysis.md
│       ├── lab-09-tcp-connection-termination.md
│       ├── lab-10-dns-failure-analysis.md
│       ├── lab-11-icmp-error-message-analysis.md
│       ├── lab-12-dhcp-failure-analysis.md
│       ├── lab-13-tls-certificate-analysis.md
│       └── lab-14-ipv6-neighbor-discovery.md
│
├── troubleshooting-scenarios/
│   ├── README.md
│   ├── scenario-01-website-unreachable.md
│   ├── scenario-02-dns-name-resolution-failure.md
│   ├── scenario-03-slow-network-connection.md
│   ├── scenario-04-intermittent-packet-loss.md
│   ├── scenario-05-tcp-port-connection-failure.md
│   ├── scenario-06-dhcp-address-assignment-failure.md
│   └── scenario-07-tls-connection-failure.md
│
├── templates/
│   ├── lab-report-template.md
│   ├── troubleshooting-ticket-template.md
│   ├── packet-analysis-findings-template.md
│   └── incident-escalation-template.md
│
├── screenshots/
│   ├── README.md
│   └── sanitized-examples/
│       └── README.md
│
└── sample-captures/
    └── README.md
```

```

## Fundamental Labs

| Lab | Topic | Main Skills |
|---|---|---|
| [Lab 01](labs/fundamentals/lab-01-icmp-ping-analysis.md) | ICMP Ping Analysis | Echo requests, replies, packet timing |
| [Lab 02](labs/fundamentals/lab-02-dns-query-analysis.md) | DNS Query Analysis | Queries, responses, record types |
| [Lab 03](labs/fundamentals/lab-03-dhcp-dora-analysis.md) | DHCP DORA Analysis | Discover, Offer, Request, ACK |
| [Lab 04](labs/fundamentals/lab-04-tcp-handshake-analysis.md) | TCP Three-Way Handshake | SYN, SYN-ACK, ACK |
| [Lab 05](labs/fundamentals/lab-05-http-traffic-analysis.md) | HTTP Traffic Analysis | Requests, responses, status codes |
| [Lab 06](labs/fundamentals/lab-06-https-tls-analysis.md) | HTTPS/TLS Analysis | TLS negotiation and encrypted traffic |

## Intermediate Labs

| Lab | Topic | Main Skills |
|---|---|---|
| [Lab 07](labs/intermediate/lab-07-arp-resolution-analysis.md) | ARP Resolution | IPv4-to-MAC mapping |
| [Lab 08](labs/intermediate/lab-08-tcp-retransmission-analysis.md) | TCP Retransmissions | Packet loss indicators and duplicate ACKs |
| [Lab 09](labs/intermediate/lab-09-tcp-connection-termination.md) | TCP Termination | FIN, ACK, and RST |
| [Lab 10](labs/intermediate/lab-10-dns-failure-analysis.md) | DNS Failure Analysis | NXDOMAIN, SERVFAIL, timeouts |
| [Lab 11](labs/intermediate/lab-11-icmp-error-message-analysis.md) | ICMP Errors | Destination unreachable and time exceeded |
| [Lab 12](labs/intermediate/lab-12-dhcp-failure-analysis.md) | DHCP Failure Analysis | Missing offers, repeated requests, APIPA |
| [Lab 13](labs/intermediate/lab-13-tls-certificate-analysis.md) | TLS Certificate Analysis | Versions, certificates, SNI |
| [Lab 14](labs/intermediate/lab-14-ipv6-neighbor-discovery.md) | IPv6 Neighbor Discovery | NS, NA, router discovery |

## Troubleshooting Scenarios

The scenarios simulate support cases and show how packet evidence can be used to narrow down a problem.

- [Website Unreachable](troubleshooting-scenarios/scenario-01-website-unreachable.md)
- [DNS Name Resolution Failure](troubleshooting-scenarios/scenario-02-dns-name-resolution-failure.md)
- [Slow Network Connection](troubleshooting-scenarios/scenario-03-slow-network-connection.md)
- [Intermittent Packet Loss](troubleshooting-scenarios/scenario-04-intermittent-packet-loss.md)
- [TCP Port Connection Failure](troubleshooting-scenarios/scenario-05-tcp-port-connection-failure.md)
- [DHCP Address Assignment Failure](troubleshooting-scenarios/scenario-06-dhcp-address-assignment-failure.md)
- [TLS Connection Failure](troubleshooting-scenarios/scenario-07-tls-connection-failure.md)

## Documentation and References

- [Lab Environment and Tools](docs/lab-environment-and-tools.md)
- [Wireshark Installation Guide](docs/wireshark-installation-guide.md)
- [Packet Capture Safety and Privacy](docs/packet-capture-safety-and-privacy.md)
- [Network Analysis Methodology](docs/network-analysis-methodology.md)
- [Display Filters Cheatsheet](docs/wireshark-display-filters-cheatsheet.md)
- [Common Protocols Reference](docs/common-protocols-reference.md)
- [Glossary](docs/glossary.md)

## Templates

- [Lab Report Template](templates/lab-report-template.md)
- [Troubleshooting Ticket Template](templates/troubleshooting-ticket-template.md)
- [Packet Analysis Findings Template](templates/packet-analysis-findings-template.md)
- [Incident Escalation Template](templates/incident-escalation-template.md)

## Recommended Workflow

1. Review the safety and privacy guidance.
2. Confirm the correct capture interface.
3. Start a capture before reproducing the issue.
4. Generate only authorized lab traffic.
5. Stop the capture after the required traffic is recorded.
6. Apply relevant display filters.
7. Document observations without overstating conclusions.
8. Sanitize screenshots and capture files before publishing.

## Ethical Use

Only capture traffic on systems and networks you own or are explicitly authorized to test. Never publish credentials, authentication tokens, private conversations, personal information, or third-party traffic.

## Future Improvements

Planned improvements are tracked in [ROADMAP.md](ROADMAP.md).
