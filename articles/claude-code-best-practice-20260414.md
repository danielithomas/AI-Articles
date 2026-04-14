# Claude Code Best Practice: From Vibe Coding to Agentic Engineering
**Authors:** shanraisshan (Shayan), with contributions from Boris Cherny, Thariq, Cat Wu, Lydia Hallie, Noah Zweben, and the Claude Code community

**Category:** Tooling & Technology

**Published:** 2025 (actively maintained)

---

## Key Points
- Provides 69 curated tips and tricks spanning prompting, planning, CLAUDE.md configuration, agent orchestration, hooks, git workflows, and debugging with Claude Code.
- Recommends structuring work around feature-specific subagents with skills rather than generic role-based agents, keeping CLAUDE.md under 200 lines, and using commands for repeatable workflows.
- Compares nine community-developed workflow frameworks (including Everything Claude Code, Superpowers, and Spec Kit) with star counts and methodology summaries.
- Advocates a progression from "vibe coding" to disciplined "agentic engineering" through plan-first development, small PRs, frequent commits, and product verification skills.
- Emphasises practical integration patterns including MCP servers for browser visibility, git worktrees for parallel agent teams, and permission sandboxing for reduced approval friction.

---

## Summary
This community-maintained GitHub repository serves as a comprehensive reference guide for Claude Code, Anthropic's official CLI tool for Claude. Created by shanraisshan and drawing on insights from Claude Code's creator Boris Cherny and other Anthropic team members, the resource catalogues best practices that have emerged as Claude Code has matured from a simple coding assistant into a full agentic engineering platform. The repository trended to number one on GitHub in March 2026, reflecting significant community interest in structured approaches to AI-assisted development.

The guide is organised into several major sections. The Concepts section covers core Claude Code primitives including subagents, commands, skills, hooks, MCP servers, memory, and checkpointing. A Hot Features section highlights newer capabilities such as Ultraplan (cloud-based planning with review), Agent SDK for building production agents, computer use on macOS, scheduled tasks, voice dictation, and multi-agent code review. A detailed comparison table evaluates nine community workflow frameworks, helping developers choose the right development methodology for their projects.

The heart of the resource is its collection of 69 tips and tricks, organised into categories covering prompting strategies, planning and specification approaches, CLAUDE.md configuration, agent orchestration, command and skill design, hook patterns, git and PR workflows, debugging techniques, and daily practices. Key themes throughout include the importance of plan-first development, keeping context clean through subagent delegation, converting repeated tasks into reusable skills or commands, and maintaining small frequent commits. The guide represents a shift from ad-hoc "vibe coding" toward a more disciplined "agentic engineering" paradigm where developers orchestrate AI agents with the same rigour applied to traditional software engineering.

---
**Captured:** 2026-04-14

**Link:** https://github.com/shanraisshan/claude-code-best-practice

**Key Words:** Claude Code; Agentic Engineering; Developer Workflows; Best Practices; AI Coding Tools
