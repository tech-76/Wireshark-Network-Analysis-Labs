# Scenario 04 — Intermittent Packet Loss

## Scenario Type

Simulated support and troubleshooting exercise.

## User Report

The user reports occasional disconnects or inconsistent response times.

## Investigation Goal

Determine whether packets or responses are intermittently missing during a controlled test.

## Relevant Protocols

- ICMP
- TCP

## Troubleshooting Steps

1. Run a timed ping test.
2. Capture the same period.
3. Compare sent requests with replies.
4. Review TCP retransmission indicators during an application test.
5. Record the exact times of visible symptoms.

## Suggested Wireshark Filters

```text
icmp || tcp.analysis.retransmission || tcp.analysis.duplicate_ack
```

## Evidence to Collect

- [ ] Missing ICMP replies
- [ ] Changes in round-trip timing
- [ ] TCP retransmissions
- [ ] Duplicate ACKs
- [ ] Direction of packet loss indicators

## Findings Table

| Packet Number | Timestamp | Source | Destination | Observation |
|---:|---:|---|---|---|
| | | | | |

## Example Interpretation

Missing echo replies or repeated TCP retransmissions may support intermittent loss, but filtered ICMP or capture limitations must be considered.

> The example above is a model interpretation. Replace it with the conclusion supported by your own capture.

## Resolution or Escalation

Escalate with a time range, packet-loss pattern, affected path, and whether the issue occurs over wired, wireless, or VPN connections.

## User Communication

Explain the result in clear language without using unnecessary packet-analysis terminology.

## Documentation Notes

- Record commands used
- Record exact test times
- Attach sanitized screenshots
- State any uncertainty
