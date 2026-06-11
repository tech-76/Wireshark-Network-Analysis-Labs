# Lab 01: ICMP Ping Analysis

## Objective

Use Wireshark to capture and analyze ICMP ping traffic.

This lab demonstrates basic network connectivity testing and packet analysis.

## Skills Practiced

- Starting a Wireshark capture
- Running a ping test
- Filtering ICMP traffic
- Identifying echo request and echo reply packets
- Documenting network test results

## Lab Environment

```text
Tool: Wireshark
Command: ping
Target: 8.8.8.8 or local default gateway
Network: Authorized lab or home network
```

## Steps

1. Open Wireshark.
2. Select the active network interface.
3. Start capture.
4. Open Command Prompt or Terminal.
5. Run a ping test.

Windows:

```cmd
ping 8.8.8.8
```

Linux/macOS:

```bash
ping -c 4 8.8.8.8
```

6. Stop the Wireshark capture.
7. Apply the display filter:

```text
icmp
```

## What to Look For

| Packet | Meaning |
|---|---|
| Echo request | Your computer sent a ping request |
| Echo reply | The destination responded |

A successful ping should show request and reply packets.

## Troubleshooting Notes

| Finding | Possible Meaning |
|---|---|
| Echo request and reply | Basic connectivity works |
| Echo request only | Target may be unreachable or blocking ICMP |
| No ICMP traffic | Wrong interface selected |
| High response time | Latency or congestion |
| Packet loss | Network instability |

## Example Lab Summary

```text
Captured ICMP traffic while running ping to 8.8.8.8.
Applied the icmp display filter.
Observed echo requests from the local computer and echo replies from the destination.
Confirmed basic network connectivity was working.
```

## Skills Demonstrated

- ICMP analysis
- Ping troubleshooting
- Source and destination IP review
- Wireshark filtering
- Lab documentation
