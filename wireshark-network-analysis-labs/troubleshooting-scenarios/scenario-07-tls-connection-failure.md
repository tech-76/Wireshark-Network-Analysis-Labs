# Scenario 07 — TLS Connection Failure

## Scenario Type

Simulated support and troubleshooting exercise.

## User Report

The user reports that a secure website or application displays a certificate or secure-connection error.

## Investigation Goal

Review whether TLS negotiation begins, which versions are offered, and whether an alert or certificate problem is visible.

## Relevant Protocols

- TCP
- TLS
- DNS

## Troubleshooting Steps

1. Confirm system date and time.
2. Confirm DNS resolution.
3. Capture the secure connection attempt.
4. Review Client Hello, Server Hello, certificate, and alert messages.
5. Compare with a working secure site.

## Suggested Wireshark Filters

```text
dns || tcp.port == 443 || tls.handshake || tls.alert_message
```

## Evidence to Collect

- [ ] DNS result
- [ ] TCP handshake
- [ ] Client Hello
- [ ] Server Hello
- [ ] Certificate details or TLS alert

## Findings Table

| Packet Number | Timestamp | Source | Destination | Observation |
|---:|---:|---|---|---|
| | | | | |

## Example Interpretation

A TLS alert after a successful TCP handshake suggests that basic network connectivity worked and the failure occurred during secure-session negotiation.

> The example above is a model interpretation. Replace it with the conclusion supported by your own capture.

## Resolution or Escalation

Escalate with the hostname, certificate details if safe, TLS alert, timestamps, and endpoint date/time status.

## User Communication

Explain the result in clear language without using unnecessary packet-analysis terminology.

## Documentation Notes

- Record commands used
- Record exact test times
- Attach sanitized screenshots
- State any uncertainty
