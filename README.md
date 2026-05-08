# Ryan Vonbrubeck

AI infrastructure and application security researcher focused on MCP/server-side tooling, agentic control planes, deployment trust boundaries, SSRF, authn/authz gaps, and coordinated disclosure.

As of May 2026, my internal research ledger tracks 15 maintainer/platform-validated or fix-track vulnerability reports, including 1 Critical and 8 High findings by conservative current bucketing. I do not count submitted or internally rated findings as wins until a maintainer, platform, advisory, fix, or case trail validates them.

## Research areas

- MCP and agent/tool invocation trust boundaries
- Server-side auth, SSRF, and fetch controls
- Default deployment exposure and misconfiguration risk
- AI/ML open-source and model/tool integration security
- Local-first AI infrastructure, context budgeting, and workflow analytics
- Reproducible, non-destructive proof-of-concept workflows

## Disclosure practice

I prioritize coordinated disclosure, clear scope boundaries, deterministic reproduction steps, and minimal-impact testing. Reports are written to help maintainers reproduce, patch, and verify issues quickly.

My default report format is source-cited code review against pinned commits, a non-destructive reproduction path, root-cause and trust-boundary analysis, and concrete fix guidance. I use GitHub Private Vulnerability Reporting where enabled and direct maintainer channels otherwise.

## Current public work

- [ContextClaw](https://github.com/dodge1218/contextclaw), deterministic context budgeting for long-running OpenClaw agent sessions.
- [PromptLens](https://github.com/dodge1218/promptlens), local-first AI usage analytics for exported conversations and workflow patterns. Related writeup: [Google/Gemini memory import prompts](https://dev.to/vonb/google-just-unlocked-something-huge-with-gemini-memory-import-heres-how-to-actually-profit-from-2ckf).
- [task-rag-mcp](https://github.com/dodge1218/task-rag-mcp), local MCP retrieval for task instructions, skills, and project memory.
- [Breaking Apps Hackathon](https://github.com/dodge1218/breaking-apps-hackathon), AI-assisted Playwright regression checks for small-business websites.
- [OpenClaw fork](https://github.com/dodge1218/openclaw), local-first personal AI assistant infrastructure.

## Public advisories

- GHSA-m2jq-w2wv-43fh, z2m-mcp, High
- GHSA-j7h9-2jh7-g967, mcp-ssh-tool, High
- GHSA-52cq-7v8r-62c6, google-maps-mcp, High
- GHSA-74mx-837f-7x87, Critical
- GHSA-f3jg-756w-gm35, gryph, published with reporter credit
- GHSA-8jr5-6gvj-rfpf, mcp-gitlab-server, High, maintainer-accepted/fix-track

## Current focus

- MCP transport authentication and browser/control-plane exposure
- Command execution, SSRF, IDOR/authz, path/archive traversal, and default-credential classes
- AI-agent tool trust boundaries and prompt-to-tool escalation paths
- Reproducible local PoCs and patch-validation workflows
- Smart-contract and protocol bounty work where scope, value at risk, and proof quality are clear
