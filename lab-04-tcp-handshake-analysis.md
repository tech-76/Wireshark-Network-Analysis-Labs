# Lab 04: TCP Handshake Analysis

## Objective

Use Wireshark to capture and analyze the TCP three-way handshake.

TCP establishes a reliable connection before application data is exchanged.

## Skills Practiced

- Capturing TCP traffic
- Identifying SYN, SYN-ACK, and ACK packets
- Filtering by TCP port
- Understanding connection setup
- Troubleshooting failed TCP connections

## TCP Three-Way Handshake

```text
Client -> Server: SYN
Server -> Client: SYN, ACK
Client -> Server: ACK
```

## Steps

1. Open Wireshark.
2. Start capture.
3. Open a website such as:

```text
https://example.com
```

Or run:

```cmd
curl -I https://example.com
```

4. Stop capture.
5. Apply a TCP filter:

```text
tcp
```

For HTTPS traffic:

```text
tcp.port == 443
```

## What to Look For

Look in the Info column for:

```text
[SYN]
[SYN, ACK]
[ACK]
```

## Useful TCP Filters

```text
tcp.flags.syn == 1
tcp.flags.syn == 1 and tcp.flags.ack == 0
tcp.flags.reset == 1
tcp.analysis.retransmission
```

## Troubleshooting Notes

| Finding | Possible Meaning |
|---|---|
| SYN, SYN-ACK, ACK visible | TCP connection established |
| Repeated SYN only | Server not responding or firewall blocking |
| TCP reset | Connection refused or reset |
| Retransmissions | Packet loss or network problem |
| Long delay before SYN-ACK | Latency or slow server response |

## Example Lab Summary

```text
Captured TCP traffic while browsing to https://example.com.
Filtered traffic using tcp.port == 443.
Identified SYN, SYN-ACK, and ACK packets.
Confirmed TCP session was established successfully before encrypted TLS traffic began.
```

## Skills Demonstrated

- TCP handshake analysis
- Port filtering
- Connection troubleshooting
- TCP flags awareness
- Network support documentation
