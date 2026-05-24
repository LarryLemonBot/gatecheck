# GateCheck Public Readiness Scorecard

GateCheck is a hosted remote MCP server for paid x402 and MCP seller-readiness checks before marketplace listing.

This scorecard is public, static evidence for directories and reviewers. It is claim-bounded and does not assert marketplace approval, payment settlement, security certification, buyer adoption, or xpay central discovery.

## Canonical Endpoints

- Public repo: `https://github.com/LarryLemonBot/gatecheck`
- Remote MCP endpoint: `https://x402-resource-scanner.vercel.app/gatecheck/mcp`
- Product homepage: `https://x402-resource-scanner.vercel.app/gatecheck`
- Product card: `https://x402-resource-scanner.vercel.app/gatecheck/product-card.md`
- Marketplace index: `https://x402-resource-scanner.vercel.app/gatecheck/marketplaces.json`
- Registry manifest: `https://github.com/LarryLemonBot/gatecheck/blob/main/server.json`
- Official MCP Registry: `https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.LarryLemonBot/gatecheck`

## Readiness Checks

| Area | Status | Evidence |
| --- | --- | --- |
| Discovery | Pass | Product-scoped homepage, `llms.txt`, `agents.txt`, product card, skill card, sitemap, and MCP server card are available for buyer and crawler inspection. |
| Tools | Pass | The product-scoped MCP endpoint supports public `initialize` and `tools/list` introspection with six GateCheck tools. |
| Pricing | Pass | Public docs expose quick readiness, report, launch-pack, paid-path probe, scan, and receipt price bands before any buyer signs or spends. |
| 402 behavior | Pass | GateCheck can inspect unpaid `402` challenge metadata for paid endpoints without submitting payment signatures or moving funds. |
| Directories | Partial | Registry-linked and directory pages are trackable; xpay central `agents.txt` propagation is not claimed until public evidence appears. |
| Boundary | Pass | Reports are limited to observed metadata, unpaid `402` behavior, request summaries, hashes, and explicit non-claims. |
| Next step | Ready | Sellers can run a readiness check, share the sample report, then package a launch only after evidence is clean. |

## Public Tool Inventory

- `boundary_guard_check`
- `scan_x402_resource`
- `probe_x402_paid_path`
- `check_agent_tool_readiness`
- `generate_x402_launch_pack`
- `generate_trust_receipt`

## Current Directory Visibility

Verified public surfaces include:

- GateCheck remote MCP endpoint: `https://x402-resource-scanner.vercel.app/gatecheck/mcp`
- Official MCP Registry: `https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.LarryLemonBot/gatecheck`
- Smithery: `https://smithery.ai/servers/larrybuildsai/gatecheck`
- Glama: `https://glama.ai/mcp/connectors/io.github.LarryLemonBot/gatecheck`
- mcpservers.org: `https://mcpservers.org/servers/x402-resource-scanner-vercel-app-gatecheck-marketplaces`
- MCP.so: `https://mcp.so/server/gatecheck-by-larrybuildsai`
- Cline MCP Marketplace submission: `https://github.com/cline/mcp-marketplace/issues/1654`

## Known External Blocker

`https://xpay.tools/agents.txt` has not yet exposed `gatecheck`, so xpay central discovery is not claimed.

## Claim Boundary

GateCheck reports and receipts prove observed public metadata, unpaid `402` behavior, request summaries, hashes, and returned artifacts only.

They do not prove marketplace endorsement, settlement, security certification, custody, KYC/AML coverage, buyer adoption, xpay central discovery, or downstream execution.

GateCheck is separate from Signal Desk and ResultRail.
