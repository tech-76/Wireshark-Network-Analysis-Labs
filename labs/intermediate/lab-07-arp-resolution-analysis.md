# Lab 07 — ARP Resolution Analysis

## Objective

Capture ARP requests and replies used to map an IPv4 address to a MAC address on the local network.

## Skills Demonstrated

- Filtering ARP traffic
- Identifying request and reply opcodes
- Reviewing IPv4-to-MAC mappings
- Understanding local-layer communication

## Scenario

Clear the ARP cache only in a safe lab, then generate traffic to the local gateway or another authorized local device.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Generate traffic to a local IPv4 destination.
3. Stop the capture.
4. Apply the ARP filter.
5. Match the request asking for a MAC address with the reply.

## Display Filters

```text
arp
```

## Analysis Checklist

- [ ] Identify the target IPv4 address in the request
- [ ] Identify the sender MAC address in the reply
- [ ] Confirm request and reply opcodes
- [ ] Check for repeated unanswered requests

## Expected Observations

A request usually asks who owns a specific IPv4 address, and the reply provides the corresponding MAC address.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

Repeated unanswered ARP requests may suggest that the target is offline, on another subnet, or not reachable at Layer 2.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Do not publish identifiable device details from third-party systems.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
