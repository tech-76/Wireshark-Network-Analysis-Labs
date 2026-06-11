# Wireshark Lab Report Template

## Lab Title

```text
Enter lab title here
```

## Date

```text
YYYY-MM-DD
```

## Objective

Describe the purpose of the lab.

Example:

```text
Capture and analyze ICMP echo request and echo reply packets using Wireshark.
```

## Lab Environment

| Item | Details |
|---|---|
| Operating System | Windows / Linux / macOS |
| Tool Used | Wireshark |
| Network Type | Home lab / VM lab / Authorized training network |
| Interface Captured | Wi-Fi / Ethernet / Loopback / VPN |
| Target Tested | IP address or hostname |

## Authorization Statement

```text
This lab was performed in a personal or authorized lab environment.
No unauthorized network traffic was captured.
```

## Commands Used

```cmd
ping 8.8.8.8
nslookup example.com
ipconfig /all
```

## Wireshark Filters Used

```text
icmp
dns
tcp.port == 443
```

## Steps Performed

```text
1. Opened Wireshark.
2. Selected active network interface.
3. Started packet capture.
4. Ran test command.
5. Stopped packet capture.
6. Applied display filter.
7. Reviewed packet details.
8. Documented findings.
```

## Observations

```text
Document packet observations here.
```

## Packet Details

| Field | Value |
|---|---|
| Source IP |  |
| Destination IP |  |
| Protocol |  |
| Source Port |  |
| Destination Port |  |
| Packet Type |  |
| Notes |  |

## Findings

```text
Summarize what was discovered.
```

## Troubleshooting Conclusion

```text
Explain what the packet capture showed and what the likely issue or result was.
```

## Screenshots

Suggested screenshots:

- Wireshark packet list with filter applied
- Packet details pane
- Command output
- Final test result

## Ticket-Style Summary

```text
Performed Wireshark capture during network test.
Applied relevant display filter and reviewed packet flow.
Confirmed expected protocol behavior and documented results.
No unauthorized traffic was captured.
```

## Skills Demonstrated

- Packet capture
- Display filtering
- Protocol analysis
- Command-line testing
- Network troubleshooting
- Technical documentation
