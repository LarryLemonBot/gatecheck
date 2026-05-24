# GateCheck by LarryBuildsAI

GateCheck is a hosted remote MCP server and x402 readiness surface for paid agent-tool sellers.

Use it before public submission, promotion, or paid agent routing to verify that a paid x402 or MCP tool is discoverable, inspectable, and claim-bounded.

## Hosted MCP Endpoint

- Remote MCP URL: `https://x402-resource-scanner.vercel.app/gatecheck/mcp`
- Transport: `streamable-http`
- Public introspection: `initialize` and `tools/list`
- Protected tool execution: bearer auth may be required for direct production calls
- Product homepage: `https://x402-resource-scanner.vercel.app/gatecheck`
- Scorecard: `https://github.com/LarryLemonBot/gatecheck/blob/main/scorecard.md`
- Product card: `https://x402-resource-scanner.vercel.app/gatecheck/product-card.md`
- Marketplace index: `https://x402-resource-scanner.vercel.app/gatecheck/marketplaces.json`

## MCP Client Config

```json
{
  "mcpServers": {
    "gatecheck": {
      "type": "streamable-http",
      "url": "https://x402-resource-scanner.vercel.app/gatecheck/mcp"
    }
  }
}
```

If your client supports request headers and you have a GateCheck production token, add:

```json
{
  "Authorization": "Bearer YOUR_GATECHECK_TOKEN"
}
```

Do not put private keys, wallet secrets, cookies, customer data, or marketplace dashboard credentials into public metadata.

## Tools

GateCheck currently exposes six MCP tools:

- `boundary_guard_check`
- `scan_x402_resource`
- `probe_x402_paid_path`
- `check_agent_tool_readiness`
- `generate_x402_launch_pack`
- `generate_trust_receipt`

Public `tools/list` is available so buyers, agents, and directories can inspect the tool inventory before protected calls.

## What GateCheck Checks

- Product-scoped discovery: homepage, `llms.txt`, `agents.txt`, product card, skill card, sitemap, and MCP server card.
- MCP inventory: public initialize and tool-list introspection.
- x402 behavior: unpaid `402` challenge metadata without submitting payment signatures or moving funds.
- Listing readiness: buyer-facing copy, prices, evidence links, launch-pack artifacts, and claim boundaries.

## Claim Boundary

GateCheck reports and receipts prove observed public metadata, unpaid `402` behavior, request summaries, hashes, and returned artifacts only.

They do not prove marketplace endorsement, settlement, security certification, custody, KYC/AML coverage, buyer adoption, or downstream execution.

## Product Boundary

GateCheck is separate from Signal Desk and ResultRail.

This repository is the public distribution and marketplace-submission surface for GateCheck only.

## Current Public Visibility

Verified public surfaces include:

- GateCheck remote MCP endpoint: `https://x402-resource-scanner.vercel.app/gatecheck/mcp`
- Official MCP Registry: `https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.LarryLemonBot/gatecheck`
- Smithery: `https://smithery.ai/servers/larrybuildsai/gatecheck`
- Glama: `https://glama.ai/mcp/connectors/io.github.LarryLemonBot/gatecheck`
- mcpservers.org: `https://mcpservers.org/servers/x402-resource-scanner-vercel-app-gatecheck-marketplaces`
- MCP.so: `https://mcp.so/server/gatecheck-by-larrybuildsai`

Known external blocker: `https://xpay.tools/agents.txt` has not yet exposed `gatecheck`, so xpay central discovery is not claimed.

## Marketplace Packet

- Cline submission draft: `marketplaces/cline-submission.md`
- MCP.Directory submission draft: `marketplaces/mcp-directory-submission.md`
- Server manifest: `server.json`
- Public scorecard: `scorecard.md`
- Logo SVG: `assets/gatecheck-logo.svg`
- Logo PNG: `assets/gatecheck-logo.png`
