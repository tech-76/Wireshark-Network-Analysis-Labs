# Lab 12 — DHCP Failure Analysis

## Objective

Investigate missing DHCP offers, repeated requests, failed acknowledgements, and automatic private addressing.

## Skills Demonstrated

- Identifying incomplete DHCP exchanges
- Recognizing repeated client requests
- Understanding APIPA symptoms
- Documenting DHCP troubleshooting evidence

## Scenario

Use a virtual lab where the DHCP service can be safely disabled, isolated, or misconfigured.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Trigger a DHCP request in the controlled lab.
3. Stop the capture after the failure is reproduced.
4. Apply the DHCP filter.
5. Review the sequence and missing responses.

## Display Filters

```text
dhcp
```

## Analysis Checklist

- [ ] Check for repeated Discover packets
- [ ] Check whether an Offer is present
- [ ] Check whether the client sends a Request
- [ ] Check whether an ACK or NAK is present
- [ ] Review the client IP configuration

## Expected Observations

Repeated Discover messages without an Offer suggest that no DHCP server response reached the client. A Windows client may assign itself an APIPA address.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

The capture can confirm which DHCP stages occurred, but server logs or switch configuration may be required to identify the exact cause.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Do not disable DHCP on a shared or production network.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
