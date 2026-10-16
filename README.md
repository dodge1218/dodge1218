# Ryan Brubeck

AI infrastructure and application security researcher focused on MCP/server-side tooling, agentic control planes, SSRF, authentication and authorization boundaries, unsafe execution, and coordinated disclosure.

[Download my cybersecurity resume](./Ryan_Brubeck_Resume_Cybersecurity_2026.pdf)

## Security research

- **57 externally validated findings** in a conservative evidence-gated ledger. Severity is recorded per finding; I do not combine the ledger's High, High-ish, and Medium-High categories into one High/Critical total.
- **18 directly attributable public records** across vendor advisories, security bulletins, releases, and maintainer-confirmed issues. The validated-findings and public-credit totals measure different things.
- **AWS:** Publicly credited by AWS for a PostgreSQL MCP read-only enforcement bypass leading to OS command execution under specific elevated database-role prerequisites. AWS rates it Important; the linked GitHub advisory rates it Critical. [AWS-2026-104](https://aws.amazon.com/security/security-bulletins/2026-104-aws/) / [GHSA-fph8-pg5w-78fv](https://github.com/advisories/GHSA-fph8-pg5w-78fv).
- **IBM MCP Context Forge:** Publicly credited for a [RestrictedPython sandbox escape](https://github.com/IBM/mcp-context-forge/security/advisories/GHSA-xm98-3vcf-fph7), rated Critical for HTTP exposure and High for stdio. The project added [regression coverage](https://github.com/IBM/mcp-context-forge/compare/v1.0.1...v1.0.2). A second [published SSRF advisory](https://github.com/IBM/mcp-context-forge/security/advisories/GHSA-c7vv-9h9c-fvj4) credits me; its update narrows the claim: the REST tool path was not exploitable as filed, while Gateway/A2A paths were source-evident but not runtime-validated in that update.

I count a result only after a maintainer, platform, published advisory, fix, or case trail validates it. Scanner output and unconfirmed submissions are not counted as wins.

## Publicly attributable security work

These records directly name Ryan, `dodge1218`, or vonbrubeck as reporter, finder, issue author, or coordinated-disclosure contributor:

- [AWS Security Bulletin AWS-2026-104](https://aws.amazon.com/security/security-bulletins/2026-104-aws/) / [GHSA-fph8-pg5w-78fv](https://github.com/advisories/GHSA-fph8-pg5w-78fv) — PostgreSQL MCP read-only enforcement bypass leading to OS command execution under specific elevated database-role prerequisites
- [GHSA-jj4w-pfgv-4mrm](https://github.com/obot-platform/obot/security/advisories/GHSA-jj4w-pfgv-4mrm) — Obot Docker quickstart mapped reachable unauthenticated users to Owner/Admin capabilities
- [GHSA-vj7q-gjh5-988w](https://github.com/advisories/GHSA-vj7q-gjh5-988w) — MCP Python SDK WebSocket Host/Origin validation
- [GHSA-rjr6-rcgv-9m7m](https://github.com/advisories/GHSA-rjr6-rcgv-9m7m) — MCP Ruby SDK DNS-rebinding and Host/Origin protection
- [GHSA-5h93-6whr-6q8j](https://github.com/advisories/GHSA-5h93-6whr-6q8j) — MCP Python SDK cross-origin redirect forwarding of custom headers and request bodies
- [GHSA-q3h7-gpc9-2rxc](https://github.com/SigNoz/signoz/security/advisories/GHSA-q3h7-gpc9-2rxc) — SigNoz Querybuilder SQL injection through telemetry key names
- [GHSA-m2jq-w2wv-43fh](https://github.com/rmaher001/z2m-mcp/security/advisories/GHSA-m2jq-w2wv-43fh) — unauthenticated Zigbee2MQTT MCP control on reachable SSE deployments
- [GHSA-j7h9-2jh7-g967](https://github.com/advisories/GHSA-j7h9-2jh7-g967) — MCP SSH Tool path-policy bypass and bearer-token comparison weakness
- [GHSA-hwpp-h97w-2h3j](https://github.com/advisories/GHSA-hwpp-h97w-2h3j) — Repomix local-file secret-scanning bypass
- [GHSA-f3jg-756w-gm35](https://github.com/advisories/GHSA-f3jg-756w-gm35) — Gryph sensitive tool-payload storage
- [Heimdall MCP v0.2.1](https://github.com/sarva-20/heimdall-mcp/releases/tag/v0.2.1) — command-injection remediation and public release credit
- [mcp-shell issue #13](https://github.com/sonirico/mcp-shell/issues/13) — execution-security finding cluster fixed in v0.6.0; counted as one root cause
- [Termux MCP issue #2](https://github.com/termuxgpt/termux-mcp/issues/2) — default external bind and unauthenticated command surface
- [x64dbg MCP v1.0.8](https://github.com/SetsunaYukiOvO/x64dbg-mcp/releases/tag/v1.0.8) — browser-originated local MCP security flaw and shipped hardening
- [DeepCode issue #128](https://github.com/HKUDS/DeepCode/issues/128) — unsafe shell execution in MCP command tools leading to sandbox hardening
- [MariaDB MCP issue #55](https://github.com/MariaDB/mcp/issues/55) / [fix commit](https://github.com/MariaDB/mcp/commit/64876fb1a4cb81bf51564c46eb60401097c067cc) — sensitive `SHOW` variants bypassed the intended read-only policy
- [IBM GHSA-xm98-3vcf-fph7](https://github.com/IBM/mcp-context-forge/security/advisories/GHSA-xm98-3vcf-fph7) — RestrictedPython sandbox escape in `python_sandbox_server`; HTTP exposure rated Critical, stdio rated High
- [IBM GHSA-c7vv-9h9c-fvj4](https://github.com/IBM/mcp-context-forge/security/advisories/GHSA-c7vv-9h9c-fvj4) — SSRF via outbound redirects; advisory update records a withdrawn REST-path claim and limits remaining paths as described above

Private, unpublished, uncredited, identity-ambiguous, and disputed-attribution records are intentionally excluded from this public-credit list.

## Research practice

My reports use pinned-source review, non-destructive proof-of-concept transcripts, negative controls, adversarial falsification, private-route-first disclosure, and patch verification. The goal is a report a maintainer can reproduce, fix, and safely publish—not a scanner-generated claim.

Current research areas include MCP and agent/tool trust boundaries, server-side authentication, SSRF and redirect controls, unsafe command execution, sandbox escapes, authorization failures, path traversal, and insecure deployment defaults.

## Public projects

- [ContextClaw](https://github.com/dodge1218/contextclaw) — deterministic context budgeting for long-running agent sessions
- [PromptLens](https://github.com/dodge1218/promptlens) — local-first AI usage analytics for exported conversations
- [task-rag-mcp](https://github.com/dodge1218/task-rag-mcp) — local MCP retrieval for task instructions and project memory
- [Breaking Apps Hackathon](https://github.com/dodge1218/breaking-apps-hackathon) — AI-assisted Playwright regression checks
