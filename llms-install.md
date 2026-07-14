# GateCheck MCP Install Notes

GateCheck is a hosted remote MCP server for paid x402 and MCP seller-readiness checks.

Use the remote endpoint:

```json
{
  "mcpServers": {
    "gatecheck": {
      "type": "streamable-http",
      "url": "https://proofbeforepay.vercel.app/gatecheck/mcp"
    }
  }
}
```

After installation, call `tools/list` first. Public tool introspection should show:

- `boundary_guard_check`
- `scan_x402_resource`
- `probe_x402_paid_path`
- `check_agent_tool_readiness`
- `generate_x402_launch_pack`
- `generate_trust_receipt`

Protected tool execution may require an `Authorization: Bearer ...` header. Do not invent or expose a token.

Use GateCheck for:

- x402 seller readiness checks
- unpaid `402` challenge inspection
- public MCP discovery checks
- listing copy and launch-pack review
- bounded receipt generation

Do not use GateCheck as proof of marketplace approval, security certification, payment settlement, buyer adoption, custody, KYC/AML coverage, or downstream execution.

GateCheck is separate from Signal Desk and ResultRail.
