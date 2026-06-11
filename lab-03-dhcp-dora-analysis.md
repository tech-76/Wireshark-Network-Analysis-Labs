# Lab 03: DHCP DORA Analysis

## Objective

Use Wireshark to observe the DHCP process known as DORA:

```text
Discover -> Offer -> Request -> Acknowledge
```

DHCP automatically assigns IP settings to devices.

## Skills Practiced

- Capturing DHCP traffic
- Understanding the DHCP lease process
- Identifying DHCP message types
- Troubleshooting IP address assignment issues

## What DHCP Provides

- IP address
- Subnet mask
- Default gateway
- DNS servers
- Lease time

## Steps

1. Open Wireshark.
2. Start capture on the active network interface.
3. Renew the IP address.

Windows:

```cmd
ipconfig /release
ipconfig /renew
ipconfig /all
```

Linux example:

```bash
sudo dhclient -r
sudo dhclient
ip addr
```

4. Stop capture.
5. Apply a DHCP filter.

```text
dhcp
```

If needed, use:

```text
bootp
```

## What to Look For

| DHCP Step | Meaning |
|---|---|
| Discover | Client searches for DHCP server |
| Offer | Server offers an IP address |
| Request | Client requests the offered IP |
| ACK | Server confirms the lease |

## Healthy Result Example

```text
DHCP Discover
DHCP Offer
DHCP Request
DHCP ACK
```

## Troubleshooting Notes

| Finding | Possible Meaning |
|---|---|
| Discover repeats only | DHCP server not responding |
| No DHCP traffic | Wrong interface or static IP |
| Device gets 169.254.x.x | DHCP failed / APIPA address |
| Wrong gateway or DNS | DHCP options may be misconfigured |

## Example Lab Summary

```text
Captured DHCP traffic during IP release and renew.
Observed Discover, Offer, Request, and ACK packets.
Confirmed the DHCP server assigned IP address, gateway, and DNS settings successfully.
```

## Skills Demonstrated

- DHCP analysis
- DORA process understanding
- APIPA troubleshooting
- IP address support
- Wireshark filtering
