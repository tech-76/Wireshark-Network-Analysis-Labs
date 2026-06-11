# Lab 05: HTTP Traffic Analysis

## Objective

Use Wireshark to review basic HTTP traffic in a safe lab environment.

HTTP traffic is not encrypted, so this lab should be performed only with a local test page or authorized training website.

## Security Note

Do not capture usernames, passwords, cookies, or private user traffic. HTTP can expose sensitive information.

## Skills Practiced

- Capturing HTTP traffic
- Filtering web requests
- Identifying GET requests
- Reviewing response codes
- Understanding why HTTPS is preferred

## Safe Local Lab Setup

Create a simple `index.html` file:

```html
<h1>Wireshark HTTP Lab</h1>
<p>This is a local test page.</p>
```

Start a local web server.

Linux/macOS:

```bash
python3 -m http.server 8080
```

Windows:

```cmd
python -m http.server 8080
```

Open:

```text
http://localhost:8080
```

## Steps

1. Start the local HTTP server.
2. Open Wireshark.
3. Capture on loopback or the correct lab interface.
4. Open the local page in a browser.
5. Stop capture.
6. Apply filter:

```text
http
```

or:

```text
tcp.port == 8080
```

## What to Look For

| Item | Meaning |
|---|---|
| GET request | Browser requested a page |
| Host header | Requested host |
| User-Agent | Browser/client information |
| 200 OK | Page loaded successfully |
| 404 Not Found | File or path missing |
| 500 Server Error | Server-side issue |

## Common HTTP Status Codes

| Code | Meaning |
|---:|---|
| 200 | OK |
| 301 | Permanent redirect |
| 302 | Temporary redirect |
| 403 | Forbidden |
| 404 | Not found |
| 500 | Server error |

## Example Lab Summary

```text
Started a local Python HTTP server on port 8080.
Captured traffic in Wireshark while opening the test page.
Applied http filter and observed HTTP GET request and 200 OK response.
Confirmed basic HTTP request and response behavior.
```

## Skills Demonstrated

- HTTP traffic analysis
- Local lab setup
- Web response code interpretation
- Wireshark filtering
- Security awareness
