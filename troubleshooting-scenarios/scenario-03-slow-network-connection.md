# Scenario 03 — Slow Network Connection

## Scenario Type

Simulated support and troubleshooting exercise.

## User Report

The user reports that a network application is unusually slow.

## Investigation Goal

Look for delayed responses, retransmissions, duplicate acknowledgements, or repeated connection attempts.

## Relevant Protocols

- TCP
- DNS
- TLS

## Troubleshooting Steps

1. Record the exact slow action.
2. Capture the transaction.
3. Check whether DNS is delayed.
4. Review TCP retransmissions and duplicate ACKs.
5. Compare connection setup time with application response time.

## Suggested Wireshark Filters

```text
dns || tcp.analysis.retransmission || tcp.analysis.duplicate_ack || tcp.analysis.lost_segment || tls
```

## Evidence to Collect

- [ ] DNS response time
- [ ] TCP handshake timing
- [ ] Retransmission count
- [ ] Duplicate ACKs
- [ ] Server response timing

## Findings Table

| Packet Number | Timestamp | Source | Destination | Observation |
|---:|---:|---|---|---|
| | | | | |

## Example Interpretation

Repeated retransmissions and duplicate acknowledgements may support a packet-loss or delay hypothesis, but endpoint load and capture location must also be considered.

> The example above is a model interpretation. Replace it with the conclusion supported by your own capture.

## Resolution or Escalation

Escalate with the affected application, test time, stream number, retransmission evidence, and whether other users are affected.

## User Communication

Explain the result in clear language without using unnecessary packet-analysis terminology.

## Documentation Notes

- Record commands used
- Record exact test times
- Attach sanitized screenshots
- State any uncertainty
