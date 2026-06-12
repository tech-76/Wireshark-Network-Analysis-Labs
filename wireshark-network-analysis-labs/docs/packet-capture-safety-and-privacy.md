# Packet Capture Safety and Privacy

## Purpose

Packet captures may contain sensitive information. This repository uses only authorized lab traffic and sanitized evidence.

## Rules

- Capture only traffic from systems and networks you own or are authorized to test.
- Do not capture third-party traffic without consent.
- Do not publish credentials, session tokens, cookies, email addresses, private messages, or personal information.
- Do not upload corporate, school, public Wi-Fi, or workplace captures unless written authorization exists.
- Use test accounts and lab systems whenever possible.
- Review every screenshot before publishing.
- Review every `.pcap` or `.pcapng` file before committing it to GitHub.

## Sanitization Checklist

Before publishing:

- [ ] Source and destination IP addresses are safe to show
- [ ] MAC addresses are not tied to identifiable devices
- [ ] DNS queries do not expose private services
- [ ] HTTP payloads contain no personal data
- [ ] Authentication headers are removed
- [ ] Cookies and tokens are removed
- [ ] Usernames and email addresses are removed
- [ ] File names do not contain private information
- [ ] Packet comments do not expose sensitive details

## Safer Alternatives

When a raw capture is not safe to publish:

- Add a screenshot with sensitive values hidden
- Describe the relevant packet fields in Markdown
- Reproduce the traffic using a disposable lab
- Use a public training capture from a trusted educational source
- Provide a packet-number reference without uploading the file

## Ethical Statement

The purpose of this repository is defensive learning, support troubleshooting, and technical documentation. It is not intended for unauthorized monitoring.
