# Lab 05 — HTTP Traffic Analysis

## Objective

Review unencrypted HTTP requests and responses in a controlled training environment.

## Skills Demonstrated

- Filtering HTTP traffic
- Identifying methods and status codes
- Reviewing headers
- Following an HTTP stream

## Scenario

Use a deliberately unencrypted local test service or approved training site. Do not enter credentials or personal information.

## Lab Environment

Complete the environment details in [`../../docs/lab-environment-and-tools.md`](../../docs/lab-environment-and-tools.md).

## Capture Procedure

1. Start the capture.
2. Open the approved HTTP test page.
3. Stop the capture.
4. Apply HTTP request and response filters.
5. Review the request method, host, path, and status code.

## Display Filters

```text
http.request || http.response
```

## Analysis Checklist

- [ ] Identify the request method
- [ ] Identify the host and request path
- [ ] Identify the response status code
- [ ] Review selected headers
- [ ] Confirm that no sensitive payload is present

## Expected Observations

A normal page request may show a GET request and a 200-series response. Redirects may show 300-series codes, and failed requests may show 400- or 500-series codes.

> Replace expected observations with the results from your actual capture before presenting the lab as completed.

## Findings Table

| Packet Number | Source | Destination | Protocol | Observation |
|---:|---|---|---|---|
| | | | | |
| | | | | |

## Troubleshooting Interpretation

HTTP status codes provide application-level evidence and should be interpreted with the surrounding request and response.

## Screenshots

Add sanitized screenshots showing the most relevant packet fields and filters.

## Security and Privacy Notes

Never use real credentials in an unencrypted HTTP lab.

## Lessons Learned

- What packet fields were most useful?
- What evidence supported the conclusion?
- What additional test would improve confidence?
