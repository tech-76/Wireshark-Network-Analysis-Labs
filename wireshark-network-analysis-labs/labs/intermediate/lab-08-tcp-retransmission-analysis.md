# Lab 08 — TCP Retransmission Analysis

## Objective

Identify TCP retransmissions, duplicate acknowledgements, and other indicators that may be associated with packet loss or delay.

## Skills Demonstrated

- Using TCP analysis filters
- Reviewing retransmissions
- Comparing duplicate ACKs
- Interpreting packet-loss indicators carefully

## Scenario

Generate authorized TCP traffic and review a capture that contains retransmission indicators. Do not artificially disrupt shared networks.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Capture a TCP session.
2. Stop the capture.
3. Apply retransmission and duplicate-ACK filters.
4. Follow the relevant TCP stream.
5. Review timing and sequence behavior.

## Display Filters

```text
tcp.analysis.retransmission || tcp.analysis.fast_retransmission || tcp.analysis.duplicate_ack
```

## Analysis Checklist

- [ ] Identify retransmitted segments
- [ ] Identify duplicate ACKs
- [ ] Review time between original and retransmitted packets
- [ ] Check whether retransmissions are isolated or repeated
- [ ] Compare client and server direction

## Expected Observations

Retransmissions may occur because of packet loss, delay, capture limitations, or out-of-order delivery.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

A retransmission alone does not prove the location of the fault. Additional path, interface, and endpoint testing may be required.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Use authorized captures and avoid publishing payload data.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
