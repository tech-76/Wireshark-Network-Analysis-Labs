# Lab 11 — ICMP Error Message Analysis

## Objective

Identify ICMP destination-unreachable and time-exceeded messages and relate them to failed or incomplete network tests.

## Skills Demonstrated

- Filtering ICMP errors
- Reviewing ICMP type and code
- Interpreting route and reachability evidence
- Relating embedded packet data to the original request

## Scenario

Use a controlled route test or unreachable destination in an authorized lab.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Generate the approved test traffic.
3. Stop the capture.
4. Filter for ICMP errors.
5. Review the type, code, source, and embedded original packet.

## Display Filters

```text
icmp.type == 3 || icmp.type == 11
```

## Analysis Checklist

- [ ] Identify the ICMP type
- [ ] Identify the ICMP code
- [ ] Identify which device generated the error
- [ ] Review the embedded original packet
- [ ] Relate the error to the test

## Expected Observations

Destination-unreachable messages indicate that delivery failed for a stated reason. Time-exceeded messages commonly appear during traceroute or routing-loop conditions.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

ICMP errors provide useful path evidence, but some networks filter ICMP and may not return a message.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Use only approved test destinations.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
