---
name: http-workflow
description: "Choose structured GET or POST for routine API calls, or read the supported curl-style arguments for advanced requests."
---

# Vulcan Curl

In Vulcan Code, read this guide with `skill` and send implicit requests through `tool_call`.

```json
{"skill":"luaskills-vulcan-curl:http-workflow","action":"vulcan_curl_get","arguments":{"url":"https://example.com/"}}
```

## Choose a tool

- `vulcan_curl_get` sends a structured GET for API debugging, webhook verification, or file downloads.
- `vulcan_curl_post` sends a structured POST for API writes, webhook testing, or multipart uploads.
- `vulcan_curl_request` accepts a supported subset of curl-style arguments for advanced HTTP requests. For HTTPS proxy certificate settings, use `--proxy-cacert`, `--proxy-capath`, or `--proxy-insecure`. Shell expansion, stdin/TTY interaction, prompts, and unimplemented curl options are unsupported.

Use these tools to debug APIs and webhook integrations, verify signatures and downloads, and inspect request or response headers. They return raw HTTP response content. Use a browser tool for JavaScript-rendered pages, page-content extraction, or Markdown conversion.

## References

- [GET](references/get.md)
- [POST](references/post.md)
- [curl-style requests](references/request.md)
