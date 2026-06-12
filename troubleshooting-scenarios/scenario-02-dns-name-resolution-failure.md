# Scenario 02 — DNS Name Resolution Failure

## Scenario Type

Simulated support and troubleshooting exercise.

## User Report

The user can reach a service by IP address but not by hostname.

## Investigation Goal

Confirm whether DNS queries are sent, whether a response is returned, and which response code is received.

## Relevant Protocols

- DNS
- UDP
- TCP

## Troubleshooting Steps

1. Test the service by IP address.
2. Run `nslookup` for the hostname.
3. Capture the lookup.
4. Compare configured DNS servers.
5. Review DNS response codes and timing.

## Suggested Wireshark Filters

```text
dns
```

## Evidence to Collect

- [ ] Queried hostname
- [ ] Destination DNS server
- [ ] DNS response code
- [ ] Returned records or lack of records
- [ ] Repeated queries

## Findings Table

| Packet Number | Timestamp | Source | Destination | Observation |
|---:|---:|---|---|---|
| | | | | |

## Example Interpretation

If the service works by IP address and the DNS response is NXDOMAIN, the issue is consistent with a missing or incorrect DNS record rather than general connectivity failure.

> The example above is a model interpretation. Replace it with the conclusion supported by your own capture.

## Resolution or Escalation

Escalate to the DNS or infrastructure team with the exact hostname, DNS server, response code, and packet evidence.

## User Communication

Explain the result in clear language without using unnecessary packet-analysis terminology.

## Documentation Notes

- Record commands used
- Record exact test times
- Attach sanitized screenshots
- State any uncertainty
