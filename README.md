# MCPSentry scanner

Point-in-time findings on any MCP server or agent-skill set — including private and local stdio servers — using the Readiness Kit's corpus for tool-description and context-file payloads. The free tier of [MCPSentry](https://rainkernel.com/products/mcpsentry); the paid service adds continuous pin-and-verify, drift alerts, the permission audit and the Agent BOM statement.

**Status: ships in Q1 2027 with MCPSentry early access.** Until the first tag this repository holds only this README and the licence — we do not announce releases before they are tagged ([why](https://rainkernel.com/open-source)).

## What the scanner will do

- Scan an MCP server (remote or local stdio) and report risky tool descriptions, undeclared capabilities and known payload patterns.
- Scan a skill set (SKILL.md, CLAUDE.md, cursor rules, editor tasks) for context-file poisoning.
- Hash every tool definition it sees, so a later run can show what changed.
- Export a CycloneDX-shaped Agent Bill of Materials for the servers and skills found.
- Run the open scanners it builds on (snyk-agent-scan, Cisco mcp-scanner) and merge their findings.

## Why free

Scanning is commoditised; we publish the scanner and charge for what a scanner cannot do — re-verifying what you approved every 15 minutes, covering your private servers, and giving your risk function a monthly statement. The prices are published at [rainkernel.com/pricing](https://rainkernel.com/pricing) and stay published.

## Security

Vulnerabilities in this tool: security@rainkernel.com or a private security advisory on this repository. We credit reporters. See [rainkernel.com/.well-known/security.txt](https://rainkernel.com/.well-known/security.txt).

## Licence

Apache-2.0 — see [LICENSE](LICENSE). © 2026 Rainkernel Technologies Private Limited.
