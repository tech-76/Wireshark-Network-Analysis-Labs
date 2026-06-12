# Lab Environment and Tools

## Purpose

This document records the environment used to complete the Wireshark labs. Update the fields below with the actual tools and versions used.

## Environment

| Item | Details |
|---|---|
| Host operating system | Replace with actual operating system |
| Wireshark version | Replace with actual version |
| Virtualization platform | VMware, VirtualBox, Hyper-V, or not used |
| Guest operating system | Replace if applicable |
| Network type | NAT, bridged, host-only, or physical LAN |
| Test browser | Replace with actual browser |
| Command-line tools | `ping`, `ipconfig`, `nslookup`, `tracert`, `curl`, or equivalents |

## Suggested Lab Setup

A basic environment can include:

- One Windows or Linux workstation
- Wireshark installed locally
- Access to a controlled home or virtual network
- A browser for generating HTTP or HTTPS traffic
- Command-line tools for ping, DNS, and route testing
- Optional virtual machines for DHCP, DNS, or server scenarios

## Capture Interface Selection

Before starting a capture:

1. Open Wireshark.
2. Review the available interfaces.
3. Select the interface showing active traffic.
4. Confirm that the interface matches the current network connection.
5. Avoid capturing on unrelated interfaces.

## Evidence Standards

For every completed lab, record:

- Date completed
- Wireshark version
- Interface used
- Display filters used
- Packet numbers referenced
- Screenshots added
- Findings based on actual evidence

## Limitations

Wireshark can show packet-level evidence, but it does not always prove the final root cause. Findings should distinguish between:

- What the capture confirms
- What the capture suggests
- What still requires additional testing
