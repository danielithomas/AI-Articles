# How Claude Code is Built
**Authors:** Gergely Orosz (The Pragmatic Engineer)

**Published:** 24 September 2025

---

## Key Points
- Claude Code originated from a simple prototype that could tell what music an engineer was listening to, which evolved into a powerful development tool after being given filesystem access.
- The tech stack (TypeScript, React, Ink) was deliberately chosen to be "on distribution" for Claude, meaning the model already excels at these technologies, allowing 90% of Claude Code to be written by itself.
- The team achieves exceptional velocity with approximately 60-100 internal releases per day and engineers pushing around 5 pull requests daily, enabled by AI-assisted prototyping that produces 10-20 iterations in days.
- Claude Code runs locally without virtualisation, prioritising simplicity over complexity, with the permissions system being the most complex component to ensure safe execution.
- Anthropic saw a 67% increase in PR throughput despite doubling team size, demonstrating that Claude Code significantly amplifies engineering productivity rather than creating typical onboarding slowdowns.

---

## Summary

This article provides an in-depth look at how Anthropic built Claude Code, featuring interviews with founding engineers Boris Cherny and Sid Bidasaria, along with founding product manager Cat Wu. The tool, which generates over $500M in annual run-rate revenue, began as a simple command-line prototype in September 2024 that could interact with AppleScript to report music playback. The breakthrough came when filesystem and bash access were added, allowing Claude to autonomously explore codebases by reading files and following imports - a capability Boris Cherny describes as "product overhang," where the model's capabilities exceeded what existing products enabled.

The technical architecture reflects a philosophy of radical simplicity. The team deliberately chose TypeScript and React because Claude excels at these technologies ("on distribution"), enabling the tool to largely build itself. Claude Code functions as a minimal shell around the Claude model, with the team consistently deleting code with each model release rather than adding complexity. The decision to run locally without virtualisation prioritised simplicity, though this required building a sophisticated permissions system to ensure safety. The tool uses npm for distribution and incorporates technologies like Ink for terminal UI, Yoga for layout, and Bun for fast building.

The development velocity is remarkable, with the team conducting rapid prototyping cycles that were previously impossible. Boris Cherny demonstrated this by building approximately 20 prototypes of a todo list feature in just two days, iterating through different UX approaches with simple prompts. This AI-accelerated prototyping enables teams to test 5-10 distinct ideas per day, fundamentally changing what's possible in product development. The tool has been adopted by over 80% of Anthropic's engineering organisation and has expanded beyond its initial developer audience to data scientists and other technical roles, demonstrating broader applicability than originally envisioned.

---
**Captured:** 22 November 2025

**Link:** https://newsletter.pragmaticengineer.com/p/how-claude-code-is-built

**Key Words:** AI; Claude Code; Software Development; Development Tools; Engineering Productivity
