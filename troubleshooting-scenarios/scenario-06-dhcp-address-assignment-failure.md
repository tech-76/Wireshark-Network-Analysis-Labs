# Scenario 06 — DHCP Address Assignment Failure

## Scenario Type

Simulated support and troubleshooting exercise.

## User Report

The user reports no network access and the device has an automatic private address.

## Investigation Goal

Determine which DHCP stages occurred and whether a server response reached the client.

## Relevant Protocols

- DHCP
- ARP

## Troubleshooting Steps

1. Review the client IP configuration.
2. Start the capture.
3. Trigger an approved lease renewal.
4. Review DHCP Discover, Offer, Request, ACK, or NAK messages.
5. Confirm whether the client assigned an APIPA address.

## Suggested Wireshark Filters

```text
dhcp || arp
```

## Evidence to Collect

- [ ] Repeated Discover packets
- [ ] DHCP Offer presence
- [ ] Request and ACK presence
- [ ] Server identifier
- [ ] Client-assigned address

## Findings Table

| Packet Number | Timestamp | Source | Destination | Observation |
|---:|---:|---|---|---|
| | | | | |

## Example Interpretation

Repeated Discover messages without an Offer are consistent with a DHCP response not reaching the client.

> The example above is a model interpretation. Replace it with the conclusion supported by your own capture.

## Resolution or Escalation

Escalate with the client MAC address only when appropriate, the switch or VLAN context, timestamps, and DHCP packet sequence.

## User Communication

Explain the result in clear language without using unnecessary packet-analysis terminology.

## Documentation Notes

- Record commands used
- Record exact test times
- Attach sanitized screenshots
- State any uncertainty
