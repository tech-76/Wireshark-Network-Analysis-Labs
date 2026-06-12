# Sample Captures

Packet captures are excluded by default through `.gitignore`.

Only add a capture file when:

- It was generated in an authorized lab
- It contains no credentials, tokens, or personal data
- It contains no private third-party traffic
- It has been reviewed before publication
- The related lab explains how it was generated

## Suggested Naming

```text
lab-01-icmp-sanitized.pcapng
lab-02-dns-sanitized.pcapng
lab-04-tcp-handshake-sanitized.pcapng
```

A Markdown explanation is preferred when a raw capture cannot be safely published.
