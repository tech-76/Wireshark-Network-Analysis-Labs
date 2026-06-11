# Lab 06: HTTPS and TLS Analysis

## Objective

Use Wireshark to identify HTTPS/TLS traffic patterns.

HTTPS encrypts web traffic. Wireshark can show connection metadata and TLS handshake activity, but the actual content is normally encrypted.

## Skills Practiced

- Identifying TLS traffic
- Filtering HTTPS packets
- Observing TCP handshake before TLS
- Recognizing TLS Client Hello and Server Hello
- Understanding encrypted application data

## HTTPS/TLS Basics

| Item | Description |
|---|---|
| HTTPS | Secure version of HTTP |
| TLS | Encryption protocol used by HTTPS |
| Port 443 | Common HTTPS port |
| Certificate | Helps verify server identity |
| Application Data | Encrypted traffic after handshake |

## Steps

1. Open Wireshark.
2. Start capture.
3. Open a website:

```text
https://example.com
```

Or run:

```cmd
curl -I https://example.com
```

4. Stop capture.
5. Apply filters:

```text
tls
```

```text
tcp.port == 443
```

## What to Look For

Common TLS packets:

| Packet | Meaning |
|---|---|
| Client Hello | Client starts TLS negotiation |
| Server Hello | Server responds with TLS details |
| Certificate | Server certificate information |
| Application Data | Encrypted content |

## What Is Visible

Wireshark may show:

- Source IP
- Destination IP
- TCP port
- TLS version
- Handshake messages
- Encrypted application data

## What Is Not Normally Visible

Wireshark should not normally show:

- Passwords
- Form details
- Private page content
- Message contents

That is the purpose of HTTPS encryption.

## Troubleshooting Notes

| Finding | Possible Meaning |
|---|---|
| TCP handshake succeeds but TLS fails | Certificate, protocol, or firewall issue |
| TLS alert | TLS negotiation problem |
| Repeated retransmissions | Packet loss or network issue |
| HTTP instead of HTTPS | Website may not be forcing encryption |

## Example Lab Summary

```text
Captured traffic while browsing to https://example.com.
Applied tls and tcp.port == 443 filters.
Observed TCP handshake followed by TLS Client Hello and Server Hello.
Confirmed website content was encrypted as TLS application data.
```

## Skills Demonstrated

- HTTPS/TLS traffic awareness
- Encrypted traffic recognition
- TCP and TLS sequence review
- Security awareness
- Network documentation
