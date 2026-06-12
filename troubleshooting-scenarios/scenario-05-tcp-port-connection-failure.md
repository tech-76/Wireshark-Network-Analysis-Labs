# Scenario 05 — TCP Port Connection Failure

## Scenario Type

Simulated support and troubleshooting exercise.

## User Report

The user can reach the destination system but cannot connect to a specific application or port.

## Investigation Goal

Determine whether the TCP connection succeeds, times out, or is actively refused.

## Relevant Protocols

- ICMP
- TCP

## Troubleshooting Steps

1. Confirm basic reachability where allowed.
2. Attempt the application connection.
3. Capture the attempt.
4. Review SYN, SYN-ACK, and RST behavior.
5. Compare with a known working port if appropriate.

## Suggested Wireshark Filters

```text
tcp.flags.syn == 1 || tcp.flags.reset == 1 || icmp
```

## Evidence to Collect

- [ ] Client SYN
- [ ] Server SYN-ACK or RST
- [ ] Repeated SYN packets
- [ ] Destination port
- [ ] ICMP unreachable messages

## Findings Table

| Packet Number | Timestamp | Source | Destination | Observation |
|---:|---:|---|---|---|
| | | | | |

## Example Interpretation

A server RST suggests that the destination was reachable but the port was closed or the connection was refused. Unanswered SYN packets suggest filtering, loss, or an unavailable path.

> The example above is a model interpretation. Replace it with the conclusion supported by your own capture.

## Resolution or Escalation

Escalate with the destination, port, timestamp, packet numbers, and whether a reset or timeout occurred.

## User Communication

Explain the result in clear language without using unnecessary packet-analysis terminology.

## Documentation Notes

- Record commands used
- Record exact test times
- Attach sanitized screenshots
- State any uncertainty
