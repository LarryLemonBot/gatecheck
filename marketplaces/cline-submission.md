# Cline MCP Marketplace Submission Draft

## Issue Title

Add GateCheck by LarryBuildsAI

## GitHub Repo URL

https://github.com/LarryLemonBot/gatecheck

## Logo Image

https://raw.githubusercontent.com/LarryLemonBot/gatecheck/main/assets/gatecheck-logo.png

## Reason for Addition

GateCheck is a hosted remote MCP server for paid x402 and MCP sellers. It lets agents and buyers inspect seller-readiness evidence before public launch: discovery surfaces, public MCP tool inventory, unpaid `402` challenge metadata, launch-pack copy, and explicit claim boundaries.

GateCheck helps Cline users evaluate whether a paid agent tool is discoverable, payable, and accurately described before routing agents or buyers into a paid flow.

## Install / Remote MCP Configuration

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

## Public Verification

- Product homepage: `https://x402-resource-scanner.vercel.app/gatecheck`
- Scorecard: `https://github.com/LarryLemonBot/gatecheck/blob/main/scorecard.md`
- Product card: `https://x402-resource-scanner.vercel.app/gatecheck/product-card.md`
- Marketplace index: `https://x402-resource-scanner.vercel.app/gatecheck/marketplaces.json`
- Server manifest: `https://x402-resource-scanner.vercel.app/mcp-registry/gatecheck/server.json`
- Public `tools/list`: returns six GateCheck tools, starting with `boundary_guard_check`

## Tool Inventory

- `boundary_guard_check`
- `scan_x402_resource`
- `probe_x402_paid_path`
- `check_agent_tool_readiness`
- `generate_x402_launch_pack`
- `generate_trust_receipt`

## Claim Boundary

GateCheck reports and receipts prove observed public metadata, unpaid `402` behavior, request summaries, hashes, and returned artifacts only.

They do not prove marketplace endorsement, settlement, security certification, custody, KYC/AML coverage, buyer adoption, or downstream execution.

GateCheck is separate from Signal Desk and ResultRail.
