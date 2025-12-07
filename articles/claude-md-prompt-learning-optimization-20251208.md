# CLAUDE.md: Best Practices Learned from Optimizing Claude Code with Prompt Learning
**Authors:** Priyan Jindal

**Category:** Tooling & Technology

**Published:** November 2025

---

## Key Points
- Prompt Learning is an optimisation approach inspired by reinforcement learning that improves AI agents through system prompt refinement rather than model weight updates.
- Optimising Claude Code's CLAUDE.md instructions yielded a 5.19% improvement in general coding performance on SWE Bench Lite.
- Repository-specific prompt optimisation showed even larger gains of 10.87% when tailored to a single codebase (Django).
- LLM evaluations provide richer learning signals than scalar rewards by explaining why code patches succeed or fail.
- Meaningful performance improvements came purely from refining instructions - no fine-tuning, retraining, or custom infrastructure required.

---

## Summary
The article describes how Arize applied their Prompt Learning technique to optimise Claude Code, one of the leading coding agents. Prompt Learning is inspired by reinforcement learning but instead of updating model weights, it focuses on optimising system prompts through meta-prompting and LLM-based feedback. The approach uses an iterative loop: run the agent on training data, evaluate outputs with unit tests and LLM feedback, then use meta-prompting to generate improved prompt instructions.

The team tested two train/test splitting approaches using SWE Bench Lite (300 GitHub issues from popular Python repositories). The first split divided data by repository to test general coding improvement across different codebases. The second split used Django issues chronologically, mimicking a developer workflow where past solutions inform future code generation. This second approach achieved a 10.87% accuracy improvement, while the cross-repository approach showed a 5.19% gain.

The key takeaway is that even top-tier coding agents like Claude Code (using Claude Sonnet 4.5) can be meaningfully improved through systematic prompt optimisation. By using LLM evaluators that explain why solutions work or fail - rather than just binary pass/fail signals - the meta-optimiser can target specific failure modes such as misunderstood APIs or incorrect assumptions about repository structure. This approach scales to any agent that exposes a system prompt.

---
**Captured:** 8 December 2025

**Link:** https://arize.com/blog/claude-md-best-practices-learned-from-optimizing-claude-code-with-prompt-learning/

**Key Words:** Claude Code; Prompt Optimisation; CLAUDE.md; Coding Agents; SWE Bench
