# Lab 03 — DHCP DORA Analysis

## Objective

Review the DHCP Discover, Offer, Request, and ACK process used to assign IPv4 configuration.

## Skills Demonstrated

- Filtering DHCP traffic
- Identifying DORA message types
- Reviewing offered IP settings
- Understanding lease assignment

## Scenario

Release and renew an address only in a controlled lab where doing so will not interrupt other users.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start a capture on the active interface.
2. Trigger a DHCP renewal using an approved method.
3. Stop the capture after the address is assigned.
4. Apply the DHCP filter.
5. Review the message-type options.

## Display Filters

```text
dhcp
```

## Analysis Checklist

- [ ] Locate DHCP Discover
- [ ] Locate DHCP Offer
- [ ] Locate DHCP Request
- [ ] Locate DHCP ACK
- [ ] Review offered IP address, gateway, DNS, and lease information

## Expected Observations

A complete exchange normally follows Discover, Offer, Request, and ACK. Some systems may renew a lease without showing every phase.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

Repeated Discover or Request packets without an Offer or ACK may indicate that no DHCP server response is reaching the client.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Do not disrupt a production connection. Use a virtual machine or controlled lab network.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
