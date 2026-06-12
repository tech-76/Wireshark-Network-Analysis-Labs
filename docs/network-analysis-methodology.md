# Network Analysis Methodology

Use this process to keep investigations structured and evidence-based.

## 1. Define the Problem

Record:

- User-reported symptom
- Affected device
- Affected application or service
- Start time
- Frequency
- Whether other users are affected

## 2. Identify the Relevant Protocol

Examples:

- Name resolution problem → DNS
- IP assignment problem → DHCP
- Reachability problem → ICMP
- Application connection problem → TCP
- Web problem → HTTP or TLS
- Local address resolution problem → ARP

## 3. Start the Capture

- Select the correct interface
- Start the capture before reproducing the issue
- Note the exact test time
- Avoid collecting unrelated traffic

## 4. Reproduce the Issue

Use a controlled test such as:

- `ping`
- `nslookup`
- `curl`
- Browser request
- DHCP renewal
- Connection to a known port

## 5. Apply Display Filters

Filter only after the capture unless a capture filter is specifically required.

Examples:

```text
icmp
dns
arp
dhcp
tcp
http
tls
```

## 6. Follow the Conversation

Review:

- Source and destination
- Request and response order
- Timing
- Error codes
- Retransmissions
- Resets
- Missing responses
- Negotiated versions or options

## 7. Separate Evidence From Assumptions

Use language such as:

- **Confirmed:** The capture shows three unanswered SYN packets.
- **Suggested:** A firewall or unavailable service may be blocking the connection.
- **Not yet confirmed:** The specific device responsible for the block.

## 8. Document the Result

Include:

- Filters used
- Packet numbers
- Screenshots
- Findings
- Likely next steps
- Escalation requirements

## 9. Recommend a Resolution or Escalation

A recommendation should match the evidence and avoid unsupported claims.
