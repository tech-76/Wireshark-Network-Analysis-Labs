# Scenario 01 — Website Unreachable

## Scenario Type

Simulated support and troubleshooting exercise.

## User Report

The user reports that a specific website does not open, while other sites may still work.

## Investigation Goal

Determine whether the issue is related to DNS resolution, network reachability, TCP connection establishment, or the web service.

## Relevant Protocols

- DNS
- ICMP
- TCP
- HTTP or TLS

## Troubleshooting Steps

1. Confirm whether the problem affects one site or all sites.
2. Test the hostname with `nslookup`.
3. Test reachability to the resolved address where appropriate.
4. Capture a browser connection attempt.
5. Review DNS, TCP, and HTTP/TLS evidence.

## Suggested Wireshark Filters

```text
dns || icmp || tcp.port == 80 || tcp.port == 443 || tls
```

## Evidence to Collect

- [ ] DNS query and response
- [ ] Resolved IP address
- [ ] TCP SYN and response behavior
- [ ] HTTP status or TLS negotiation
- [ ] Timing of failures

## Findings Table

| Packet Number | Timestamp | Source | Destination | Observation |
|---:|---:|---|---|---|
| | | | | |

## Example Interpretation

If DNS succeeds but repeated TCP SYN packets receive no reply, the problem is likely beyond basic name resolution. A firewall, unreachable host, or unavailable service may be involved.

> The example above is a model interpretation. Replace it with the conclusion supported by your own capture.

## Resolution or Escalation

Escalate with the hostname, destination IP, timestamps, packet numbers, and tests already completed when the issue is outside the local support scope.

## User Communication

Explain the result in clear language without using unnecessary packet-analysis terminology.

## Documentation Notes

- Record commands used
- Record exact test times
- Attach sanitized screenshots
- State any uncertainty
