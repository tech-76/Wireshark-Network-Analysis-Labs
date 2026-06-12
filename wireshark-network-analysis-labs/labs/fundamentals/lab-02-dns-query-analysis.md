# Lab 02 — DNS Query and Response Analysis

## Objective

Capture DNS queries and responses and identify the requested name, record type, response code, and returned address.

## Skills Demonstrated

- Filtering DNS traffic
- Identifying query and response pairs
- Reviewing record types
- Interpreting DNS response codes

## Scenario

Use `nslookup` or a browser to request a known public hostname in a controlled lab capture.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Run a DNS lookup for a known hostname.
3. Stop the capture after the response is received.
4. Apply the DNS filter.
5. Match the transaction ID between query and response.

## Display Filters

```text
dns
```

## Analysis Checklist

- [ ] Identify the queried hostname
- [ ] Identify the query type such as A or AAAA
- [ ] Match the response to the query
- [ ] Review the returned address
- [ ] Check the DNS response code

## Expected Observations

A successful response should normally contain a response code of `No error` and one or more answer records. Some lookups may also include CNAME records.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

A failed or delayed DNS exchange can explain why a service works by IP address but not by hostname.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Do not publish private internal hostnames or private DNS suffixes.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
