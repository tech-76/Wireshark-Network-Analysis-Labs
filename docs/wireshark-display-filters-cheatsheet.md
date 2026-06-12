# Wireshark Display Filters Cheatsheet

## General Protocol Filters

```text
icmp
icmpv6
arp
dns
dhcp
tcp
udp
http
tls
```

## IP Address Filters

```text
ip.addr == 192.168.1.10
ip.src == 192.168.1.10
ip.dst == 192.168.1.10
ipv6.addr == 2001:db8::1
```

## Port Filters

```text
tcp.port == 80
tcp.port == 443
tcp.port == 3389
udp.port == 53
tcp.dstport == 445
```

## DNS Filters

```text
dns.flags.response == 0
dns.flags.response == 1
dns.qry.name contains "example"
dns.flags.rcode != 0
dns.flags.rcode == 3
```

## DHCP Filters

```text
dhcp
dhcp.option.dhcp == 1
dhcp.option.dhcp == 2
dhcp.option.dhcp == 3
dhcp.option.dhcp == 5
```

Common message-type values:

- 1 = Discover
- 2 = Offer
- 3 = Request
- 5 = ACK

## TCP Analysis Filters

```text
tcp.flags.syn == 1
tcp.flags.reset == 1
tcp.analysis.retransmission
tcp.analysis.fast_retransmission
tcp.analysis.duplicate_ack
tcp.analysis.lost_segment
tcp.stream eq 0
```

## HTTP Filters

```text
http.request
http.response
http.request.method == "GET"
http.response.code >= 400
http.host contains "example"
```

## TLS Filters

```text
tls.handshake
tls.handshake.type == 1
tls.handshake.type == 2
tls.record.version
tls.handshake.extensions_server_name
```

## ARP Filters

```text
arp
arp.opcode == 1
arp.opcode == 2
arp.src.proto_ipv4 == 192.168.1.10
```

## ICMP Filters

```text
icmp.type == 8
icmp.type == 0
icmp.type == 3
icmp.type == 11
```

## Combined Filters

```text
dns || icmp
tcp.flags.syn == 1 && tcp.flags.ack == 0
ip.addr == 192.168.1.10 && tcp
tcp.port == 443 && tls
```

## Notes

Display filters do not change the capture. They only control which captured packets are shown.
