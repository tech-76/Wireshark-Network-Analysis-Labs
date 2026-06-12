# Lab 14 — IPv6 Neighbor Discovery

## Objective

Capture IPv6 neighbor solicitation and neighbor advertisement messages used for local address resolution.

## Skills Demonstrated

- Filtering ICMPv6 traffic
- Identifying NS and NA messages
- Reviewing IPv6 addresses
- Understanding IPv6 local discovery

## Scenario

Generate traffic to an authorized IPv6 destination on the local network.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Generate IPv6 traffic.
3. Stop the capture.
4. Apply the ICMPv6 neighbor-discovery filter.
5. Match solicitations with advertisements.

## Display Filters

```text
icmpv6.type == 135 || icmpv6.type == 136
```

## Analysis Checklist

- [ ] Identify Neighbor Solicitation
- [ ] Identify Neighbor Advertisement
- [ ] Review source and target IPv6 addresses
- [ ] Check link-layer address options
- [ ] Compare the exchange with ARP behavior

## Expected Observations

IPv6 uses Neighbor Discovery instead of ARP for local address resolution.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

Missing advertisements may indicate that the target is unavailable, the wrong interface is used, or IPv6 is not configured as expected.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Do not publish private IPv6 addressing details without approval.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
