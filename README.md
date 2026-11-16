# Steadyline Data web tools

Pay-per-result web data tools for developers and AI agents, published by [Steadyline Data](https://steadylinedata.com).

This repository holds the official [MCP Registry](https://registry.modelcontextprotocol.io) manifest (`server.json`) and client config snippets. The tools themselves run as public [Apify Actors](https://apify.com/steadyline) and are exposed over Streamable HTTP by Apify's hosted MCP server. You do not install a local server.

Contact: hello@steadylinedata.com

## Add all 13 tools to an MCP client

```
https://mcp.apify.com?tools=steadyline/ats-jobs-feed,steadyline/sec-form-d-funded-companies,steadyline/website-contact-extractor,steadyline/website-team-extractor,steadyline/tech-stack-detector,steadyline/email-deliverability-checker,steadyline/phone-number-validator,steadyline/domain-intel,steadyline/site-discovery,steadyline/website-screenshot,steadyline/pdf-document-to-markdown,steadyline/http-request-runner,steadyline/app-store-reviews
```

Auth: sign in with Apify (OAuth) on first connect, or send `Authorization: Bearer <APIFY_TOKEN>`. A free Apify account works. Runs are billed to your Apify account at each tool's pay-per-result price. There is no Steadyline subscription.

Config files:

- Cursor: [`mcp/cursor-mcp.json`](mcp/cursor-mcp.json) → `~/.cursor/mcp.json`
- VS Code: [`mcp/vscode-mcp.json`](mcp/vscode-mcp.json) → `.vscode/mcp.json`
- Claude Code: `claude mcp add --transport http steadyline "https://mcp.apify.com?tools=steadyline/ats-jobs-feed,steadyline/sec-form-d-funded-companies,steadyline/website-contact-extractor,steadyline/website-team-extractor,steadyline/tech-stack-detector,steadyline/email-deliverability-checker,steadyline/phone-number-validator,steadyline/domain-intel,steadyline/site-discovery,steadyline/website-screenshot,steadyline/pdf-document-to-markdown,steadyline/http-request-runner,steadyline/app-store-reviews"`

Docs: https://steadylinedata.com/mcp/

Official registry name: `com.steadylinedata/web-data-tools`

## The tools

| Tool | Apify Store | Price (primary) |
|---|---|---|
| ATS job feeds | [ats-jobs-feed](https://apify.com/steadyline/ats-jobs-feed) | $2 / 1,000 jobs |
| SEC Form D funded companies | [sec-form-d-funded-companies](https://apify.com/steadyline/sec-form-d-funded-companies) | $2 / 1,000 filings |
| Website contacts | [website-contact-extractor](https://apify.com/steadyline/website-contact-extractor) | $2 / 1,000 sites |
| Team page people | [website-team-extractor](https://apify.com/steadyline/website-team-extractor) | $0.004 / person |
| Tech stack detector | [tech-stack-detector](https://apify.com/steadyline/tech-stack-detector) | $2 / 1,000 domains |
| Email deliverability (no SMTP) | [email-deliverability-checker](https://apify.com/steadyline/email-deliverability-checker) | $0.50 / 1,000 emails |
| Phone validator (offline, E.164) | [phone-number-validator](https://apify.com/steadyline/phone-number-validator) | $0.50 / 1,000 numbers |
| WHOIS / DNS / SSL | [domain-intel](https://apify.com/steadyline/domain-intel) | $1 / 1,000 domains |
| Sitemaps, robots.txt, llms.txt | [site-discovery](https://apify.com/steadyline/site-discovery) | $2 / 1,000 domains |
| Website screenshots | [website-screenshot](https://apify.com/steadyline/website-screenshot) | $2 / 1,000 shots |
| PDF to Markdown | [pdf-document-to-markdown](https://apify.com/steadyline/pdf-document-to-markdown) | $2 / 1,000 docs |
| Bulk HTTP runner | [http-request-runner](https://apify.com/steadyline/http-request-runner) | $0.80 / 1,000 requests |
| App Store reviews | [app-store-reviews](https://apify.com/steadyline/app-store-reviews) | from $0.30 / 1,000 reviews |

A JSON HTTP API for 11 of these tools (not the team extractor or HTTP runner) is at https://api.steadylinedata.com with OpenAPI at `/openapi.yaml`. Customer access is through API marketplaces.

## License

MIT. The Actors and API remain separately licensed and billed on their host platforms.
