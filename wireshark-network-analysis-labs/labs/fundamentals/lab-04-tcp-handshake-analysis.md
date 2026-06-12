# Lab 04 — TCP Three-Way Handshake Analysis

## Objective

Capture and analyze the TCP SYN, SYN-ACK, and ACK packets used to establish a connection.

## Skills Demonstrated

- Filtering TCP traffic
- Identifying TCP flags
- Following a TCP stream
- Reviewing sequence and acknowledgement behavior

## Scenario

Open an authorized TCP service or website and capture the initial connection.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Connect to the selected service.
3. Stop the capture.
4. Filter by the destination port or TCP stream.
5. Inspect the first three handshake packets.

## Display Filters

```text
tcp.flags.syn == 1
```

## Analysis Checklist

- [ ] Identify the client SYN
- [ ] Identify the server SYN-ACK
- [ ] Identify the client ACK
- [ ] Review source and destination ports
- [ ] Confirm the flags and packet order

## Expected Observations

A successful connection begins with SYN, SYN-ACK, and ACK. Repeated SYN packets without SYN-ACK suggest that the response is not returning.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

The handshake confirms that the TCP connection was established, but it does not confirm that the application completed its work successfully.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Use only a service you are authorized to access.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
