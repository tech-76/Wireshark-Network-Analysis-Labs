# Lab 06 — HTTPS and TLS Handshake Analysis

## Objective

Identify TLS handshake traffic and review visible negotiation details without decrypting application content.

## Skills Demonstrated

- Filtering TLS traffic
- Identifying Client Hello and Server Hello
- Reviewing TLS versions
- Understanding encrypted payload limitations

## Scenario

Open an authorized HTTPS website and capture the connection setup.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Open the HTTPS destination.
3. Stop the capture.
4. Apply the TLS handshake filter.
5. Review Client Hello, Server Hello, and subsequent encrypted records.

## Display Filters

```text
tls.handshake
```

## Analysis Checklist

- [ ] Identify Client Hello
- [ ] Identify Server Hello
- [ ] Review supported and selected TLS versions
- [ ] Review the server name indication if visible
- [ ] Confirm that application data is encrypted

## Expected Observations

TLS negotiation metadata may be visible while the application payload remains encrypted.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

Wireshark can confirm that a TLS session was attempted and negotiated, but encrypted content cannot normally be read without approved decryption keys.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Do not attempt to decrypt traffic without authorization.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
