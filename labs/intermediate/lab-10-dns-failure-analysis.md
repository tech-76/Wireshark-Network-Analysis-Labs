# Lab 10 — DNS Failure Analysis

## Objective

Investigate unsuccessful DNS lookups, including NXDOMAIN, SERVFAIL, refused responses, and unanswered queries.

## Skills Demonstrated

- Filtering DNS errors
- Interpreting response codes
- Comparing successful and failed lookups
- Distinguishing DNS failure types

## Scenario

Query a deliberately invalid test hostname or use a controlled lab DNS failure.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Run the failed lookup.
3. Stop the capture.
4. Apply the DNS error filter.
5. Review response codes and timing.

## Display Filters

```text
dns.flags.rcode != 0 || dns.flags.response == 0
```

## Analysis Checklist

- [ ] Identify the requested name
- [ ] Check for a response
- [ ] Review the response code
- [ ] Compare query and response timing
- [ ] Check for repeated queries to multiple DNS servers

## Expected Observations

NXDOMAIN means the requested name does not exist according to the responding DNS server. SERVFAIL indicates that the server could not complete the lookup.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

Different DNS failure codes require different next steps. An unanswered query may suggest reachability or filtering issues rather than a missing record.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Do not expose internal hostnames or private DNS architecture.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
