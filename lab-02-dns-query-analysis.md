# Lab 02: DNS Query Analysis

## Objective

Use Wireshark to capture and analyze DNS queries and responses.

DNS translates names such as `example.com` into IP addresses.

## Skills Practiced

- Capturing DNS traffic
- Using `nslookup`
- Filtering DNS packets
- Reviewing DNS query and response details
- Troubleshooting name resolution issues

## Steps

1. Open Wireshark.
2. Start capture on the active network interface.
3. Run a DNS lookup.

Windows/Linux/macOS:

```cmd
nslookup example.com
```

Optional record checks:

```cmd
nslookup -type=mx example.com
nslookup -type=txt example.com
```

4. Stop capture.
5. Apply the filter:

```text
dns
```

## What to Look For

| Item | Meaning |
|---|---|
| Standard query | Client asks DNS server for a record |
| Standard query response | DNS server replies |
| Query name | Domain being requested |
| Query type | A, AAAA, MX, TXT, CNAME, etc. |
| Response code | Shows success or error |

## Common DNS Record Types

| Type | Purpose |
|---|---|
| A | IPv4 address |
| AAAA | IPv6 address |
| MX | Mail server |
| TXT | SPF, DKIM, DMARC, verification records |
| CNAME | Alias |
| NS | Nameserver |

## Troubleshooting Notes

| Finding | Possible Meaning |
|---|---|
| Query and response visible | DNS is working |
| Query only, no response | DNS server may be unreachable |
| NXDOMAIN | Domain does not exist |
| Public DNS works but internal DNS fails | VPN or internal DNS issue |
| Wrong DNS server | Device may have incorrect DNS settings |

## Example Lab Summary

```text
Started Wireshark capture and ran nslookup for example.com.
Applied dns display filter.
Observed DNS query from local computer and DNS response from configured DNS server.
Confirmed name resolution was working.
```

## Skills Demonstrated

- DNS troubleshooting
- Name resolution analysis
- nslookup usage
- Wireshark DNS filtering
- Technical documentation
