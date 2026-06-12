# Lab 13 — TLS Certificate and Negotiation Analysis

## Objective

Review TLS negotiation details, certificate metadata, server name indication, and selected versions in an authorized capture.

## Skills Demonstrated

- Reviewing TLS handshake messages
- Identifying certificate metadata
- Checking SNI
- Comparing offered and selected TLS versions

## Scenario

Connect to an authorized HTTPS service and capture the initial TLS negotiation.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Connect to the approved HTTPS service.
3. Stop the capture.
4. Apply TLS handshake filters.
5. Review the Client Hello, Server Hello, certificate, and extensions.

## Display Filters

```text
tls.handshake
```

## Analysis Checklist

- [ ] Identify Client Hello
- [ ] Identify Server Hello
- [ ] Review SNI if visible
- [ ] Review certificate subject and issuer if available
- [ ] Review validity dates and selected protocol version

## Expected Observations

Certificate and negotiation details may help explain trust, hostname, or version-related failures.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

A valid-looking certificate in a capture does not prove full application trust. Endpoint trust stores, date settings, and application policies may also matter.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Do not publish certificates or hostnames from private internal services without approval.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
