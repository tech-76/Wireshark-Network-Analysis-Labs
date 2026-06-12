# Lab 09 — TCP Connection Termination

## Objective

Analyze orderly TCP connection closure and immediate resets using FIN, ACK, and RST flags.

## Skills Demonstrated

- Filtering TCP flags
- Comparing FIN and RST behavior
- Following TCP streams
- Understanding connection closure

## Scenario

Open and close an authorized TCP session, then review the ending packets.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Open an authorized connection.
3. Close the connection normally.
4. Stop the capture.
5. Filter FIN and RST packets and inspect the stream.

## Display Filters

```text
tcp.flags.fin == 1 || tcp.flags.reset == 1
```

## Analysis Checklist

- [ ] Identify FIN packets
- [ ] Identify acknowledgements of FIN packets
- [ ] Check whether both sides close the session
- [ ] Identify any RST packets
- [ ] Review the packet order

## Expected Observations

An orderly close usually uses FIN and ACK exchanges. A reset immediately terminates the connection and may indicate refusal, application termination, or a policy decision.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

A reset shows that a connection was rejected or terminated, but further testing is needed to identify the exact reason.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Do not test against systems without permission.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
