# Ryan Vonbrubeck

AI infrastructure and application security researcher focused on MCP/server-side tooling, deployment trust boundaries, SSRF, authn/authz gaps, and coordinated disclosure.

## Research areas

- MCP and agent/tool invocation trust boundaries
- Server-side auth, SSRF, and fetch controls
- Default deployment exposure and misconfiguration risk
- AI/ML open-source and model/tool integration security
- Reproducible, non-destructive proof-of-concept workflows

## Disclosure practice

I prioritize coordinated disclosure, clear scope boundaries, deterministic reproduction steps, and minimal-impact testing. Reports are written to help maintainers reproduce, patch, and verify issues quickly.

## Current public work

- [ContextClaw](https://github.com/dodge1218/contextclaw), deterministic context budgeting for long-running OpenClaw agent sessions.
- [task-rag-mcp](https://github.com/dodge1218/task-rag-mcp), local MCP retrieval for task instructions, skills, and project memory.
- [OpenClaw fork](https://github.com/dodge1218/openclaw), local-first personal AI assistant infrastructure.

## Public advisories

- GHSA-m2jq-w2wv-43fh, z2m-mcp, High
- GHSA-j7h9-2jh7-g967, mcp-ssh-tool, High
- GHSA-52cq-7v8r-62c6, google-maps-mcp, High
- GHSA-74mx-837f-7x87, Critical
