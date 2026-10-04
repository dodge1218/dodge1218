# Ryan Brubeck

AI infrastructure and application security researcher focused on MCP/server-side tooling, agentic control planes, SSRF, authentication and authorization boundaries, unsafe execution, and coordinated disclosure.

[Download my cybersecurity resume](./Ryan_Brubeck_Resume_Cybersecurity_2026.pdf)

## Security research

- **55 externally validated findings**: 6 Critical, 34 High/High-ish, and 15 Medium/lower, using a conservative evidence-gated ledger.
- Ranked **#337 on the Microsoft Security Response Center 2026 Q2 Points Leaderboard**.
- **AWS Security confirmed six implemented fixes** across `awslabs/mcp`, including SQL execution bypass, sensitive-data exposure, authentication-header logging, Kubernetes apply bypass, resource mutation bypass, and arbitrary file write.
- **IBM MCP Context Forge** added public regression coverage for my Critical RestrictedPython sandbox escape; additional IBM work includes a published SSRF advisory.
- **Google PR #3219** fixed a BigQuery ML allowlist bypass I reported.

I count a result only after a maintainer, platform, published advisory, fix, or case trail validates it. Scanner output and unconfirmed submissions are not counted as wins.

## Public GitHub advisory credit

GitHub's live [`credit:dodge1218` advisory index](https://github.com/advisories?query=credit%3Adodge1218) currently links these native public credits:

- [GHSA-rjr6-rcgv-9m7m](https://github.com/advisories/GHSA-rjr6-rcgv-9m7m) — MCP Ruby SDK DNS-rebinding / Host-Origin protection
- [GHSA-vj7q-gjh5-988w](https://github.com/advisories/GHSA-vj7q-gjh5-988w) — MCP Python SDK WebSocket Host-Origin validation
- [GHSA-hwpp-h97w-2h3j](https://github.com/advisories/GHSA-hwpp-h97w-2h3j) — Repomix local-file secret-scanning bypass
- [GHSA-v3f4-w7r7-v3hm](https://github.com/advisories/GHSA-v3f4-w7r7-v3hm) — Uni-CLI browser-originated localhost requests
- [GHSA-f3jg-756w-gm35](https://github.com/advisories/GHSA-f3jg-756w-gm35) — Gryph sensitive tool-payload filtering

## Additional published advisories from my research

- [GHSA-7hgr-7h44-33w2](https://github.com/advisories/GHSA-7hgr-7h44-33w2) — CamoFox MCP unauthenticated browser-control surface
- [GHSA-xm98-3vcf-fph7](https://github.com/advisories/GHSA-xm98-3vcf-fph7) — IBM MCP Context Forge RestrictedPython sandbox escape
- [GHSA-c7vv-9h9c-fvj4](https://github.com/IBM/mcp-context-forge/security/advisories/GHSA-c7vv-9h9c-fvj4) — IBM MCP Context Forge redirect-based SSRF bypass
- [GHSA-f5pj-2738-996m](https://github.com/advisories/GHSA-f5pj-2738-996m), [GHSA-3x77-wg38-92r3](https://github.com/advisories/GHSA-3x77-wg38-92r3), and [GHSA-74hp-mggr-hv58](https://github.com/advisories/GHSA-74hp-mggr-hv58) — MCP Shell execution-security hardening
- [GHSA-6xc5-4r68-67fc](https://github.com/advisories/GHSA-6xc5-4r68-67fc) — Langroid SQLChatAgent dangerous-function blocklist bypass
- [GHSA-m2jq-w2wv-43fh](https://github.com/rmaher001/z2m-mcp/security/advisories/GHSA-m2jq-w2wv-43fh) — z2m-mcp unauthenticated Zigbee control
- [GHSA-j7h9-2jh7-g967](https://github.com/advisories/GHSA-j7h9-2jh7-g967) — MCP SSH Tool path-policy bypass and token comparison
- [GHSA-52cq-7v8r-62c6](https://github.com/advisories/GHSA-52cq-7v8r-62c6) — Google Maps MCP unauthenticated billed API access
- [GHSA-8jr5-6gvj-rfpf](https://github.com/advisories/GHSA-8jr5-6gvj-rfpf) — MCP GitLab Server unauthenticated transport exposure
- [GHSA-jj4w-pfgv-4mrm](https://github.com/obot-platform/obot/security/advisories/GHSA-jj4w-pfgv-4mrm) — Obot unauthenticated Owner/Admin mapping
- [GHSA-2v5f-5r6w-p67r](https://github.com/advisories/GHSA-2v5f-5r6w-p67r) — MCP Registry OCI ownership validation fail-open
- [GHSA-hv85-774v-26fg](https://github.com/advisories/GHSA-hv85-774v-26fg) — Auth Fetch MCP SSRF and disk exfiltration
- [GHSA-pqmg-rq46-vm4m](https://github.com/triggerdotdev/trigger.dev/security/advisories/GHSA-pqmg-rq46-vm4m) — Trigger.dev unauthenticated MCP transport
- [GHSA-c9xm-49cp-xcr9](https://github.com/advisories/GHSA-c9xm-49cp-xcr9) and [GHSA-9g45-5xwm-f3wc](https://github.com/advisories/GHSA-9g45-5xwm-f3wc) — MCP Rust SDK OAuth request steering and cross-origin header leakage
- [GHSA-7xxm-gqxv-ph3v](https://github.com/1Panel-dev/MaxKB/security/advisories/GHSA-7xxm-gqxv-ph3v) — MaxKB server-side request forgery
- [GHSA-mrq8-fv7v-hhjg](https://github.com/advisories/GHSA-mrq8-fv7v-hhjg) and [GHSA-76pr-5669-3xf5](https://github.com/sooperset/mcp-atlassian/security/advisories/GHSA-76pr-5669-3xf5) — MCP Atlassian local-file access and OAuth backup permissions
- [GHSA-6prh-2h8m-c8cw](https://github.com/modelcontextprotocol/typescript-sdk/security/advisories/GHSA-6prh-2h8m-c8cw) — MCP TypeScript SDK cross-origin redirect leakage

Private or unpublished advisories are intentionally omitted until their maintainers publish them.

## Research practice

My reports use pinned-source review, non-destructive proof-of-concept transcripts, negative controls, adversarial falsification, private-route-first disclosure, and patch verification. The goal is a report a maintainer can reproduce, fix, and safely publish—not a scanner-generated claim.

Current research areas include MCP and agent/tool trust boundaries, server-side authentication, SSRF and redirect controls, unsafe command execution, sandbox escapes, authorization failures, path traversal, and insecure deployment defaults.

## Public projects

- [ContextClaw](https://github.com/dodge1218/contextclaw) — deterministic context budgeting for long-running agent sessions
- [PromptLens](https://github.com/dodge1218/promptlens) — local-first AI usage analytics for exported conversations
- [task-rag-mcp](https://github.com/dodge1218/task-rag-mcp) — local MCP retrieval for task instructions and project memory
- [Breaking Apps Hackathon](https://github.com/dodge1218/breaking-apps-hackathon) — AI-assisted Playwright regression checks
