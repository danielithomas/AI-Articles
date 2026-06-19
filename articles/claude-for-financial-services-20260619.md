# Claude for Financial Services

**Authors:** Anthropic

**Category:** Architecture & Operations

**Published:** 23 February 2026 (repository; last updated 5 June 2026)

---

## Key Points
- Provides reference agents, skills, and data connectors for the financial-services workflows Anthropic sees most: investment banking, equity research, private equity, and wealth management.
- Everything ships "two ways from one source" — install as a Claude Cowork plugin, or deploy via the Claude Managed Agents API behind your own workflow engine, using the same system prompt and skills.
- Includes named end-to-end workflow agents (Pitch Agent, Meeting Prep Agent, Market Researcher, Earnings Reviewer, Model Builder, Valuation Reviewer, GL Reconciler, Month-End Closer, Statement Auditor, KYC Screener) plus vertical skill/command bundles.
- Wires Claude to data via 12 MCP connectors (Daloopa, Morningstar, S&P Global, FactSet, Moody's, PitchBook, LSEG, Box, and others), with partner-built plugins from LSEG and S&P Global.
- Agents draft analyst work product (models, memos, notes, reconciliations) staged for human sign-off — they do not give investment advice, execute transactions, or approve onboarding.

---

## Summary
Claude for Financial Services is an Anthropic reference repository packaging agents, skills, slash commands, and data connectors for common financial-services (FSI) workflows. It is built around a "two ways from one source" principle: each capability can be installed as a Claude Cowork plugin or deployed through the Claude Managed Agents API behind a firm's own workflow engine, with both paths referencing the same system prompt and skill files. The repository is entirely file-based (markdown and JSON, no build step), organised into self-contained agent plugins, vertical plugins, partner-built plugins, and managed-agent cookbooks.

The catalogue centres on named, end-to-end workflow agents grouped by function — coverage and advisory (Pitch Agent, Meeting Prep Agent), research and modeling (Market Researcher, Earnings Reviewer, Model Builder), fund admin and finance ops (Valuation Reviewer, GL Reconciler, Month-End Closer, Statement Auditor), and operations and onboarding (KYC Screener). Each agent bundles the skills it needs and is offered both as a Cowork plugin and as a Managed Agent template deployable via the `/v1/agents` endpoint, complete with `agent.yaml`, leaf-worker subagents, and steering-event examples. Underlying skills and commands (`/comps`, `/dcf`, `/earnings`, `/ic-memo`) are authored once in vertical plugins (financial-analysis core, investment-banking, equity-research, private-equity, wealth-management, fund-admin, operations) and synced into the agents that use them.

Connectivity comes through MCP servers centralised in the financial-analysis core plugin and shared across the rest, spanning data providers such as Daloopa, Morningstar, FactSet, S&P Global, Moody's, MT Newswires, Aiera, LSEG, PitchBook, Chronograph, Egnyte, and Box. The repository also includes admin tooling to provision the Claude Microsoft 365 add-in (Excel, PowerPoint, Word, Outlook) against a firm's own Vertex AI, Bedrock, or internal LLM gateway. Anthropic frames the templates as starting points meant to be tuned to each firm's connectors, terminology, formatting standards, and processes, and stresses that nothing in the repo constitutes investment, legal, tax, or accounting advice — every output is staged for review and sign-off by a qualified professional.

---
**Captured:** 19 June 2026

**Link:** https://github.com/anthropics/financial-services

**Key Words:** AI Agents; Financial Services; MCP; Managed Agents; Plugins
