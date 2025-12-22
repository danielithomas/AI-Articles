# 2025 LLM Year in Review
**Authors:** Andrej Karpathy

**Category:** Technical Fundamentals

**Published:** 19 December 2025

---

## Key Points

- RLVR (Reinforcement Learning from Verifiable Rewards) emerged as the dominant new training stage in 2025, enabling LLMs to spontaneously develop reasoning strategies through optimisation against objective, non-gameable reward functions.
- LLM intelligence displays "jagged" performance characteristics - simultaneously genius-level in verifiable domains and cognitively challenged in others - more akin to "summoned ghosts" than "evolving animals."
- Cursor revealed a new "LLM app" layer that orchestrates multiple LLM calls, manages context engineering, and provides domain-specific interfaces for human-in-the-loop workflows.
- Claude Code emerged as the first convincing LLM agent demonstration, running locally on developers' computers with access to their private environment, data, and context.
- "Vibe coding" crossed a capability threshold enabling non-programmers to build software via natural language, democratising programming while empowering professionals to write ephemeral, single-use code.

---

## Summary

Karpathy identifies six "paradigm changes" that reshaped the LLM landscape in 2025. The most significant is RLVR - a new training stage where models are trained against automatically verifiable rewards (such as maths and code puzzles), causing them to spontaneously develop reasoning strategies. Unlike the relatively thin SFT and RLHF stages, RLVR allows much longer optimisation runs against objective reward functions, and most of 2025's capability progress came from labs exploiting this new training paradigm rather than scaling model parameters.

The article introduces the conceptual framework of "ghosts versus animals" to understand LLM intelligence. Rather than viewing LLMs as evolving biological intelligences, Karpathy argues they are fundamentally different entities - "summoned ghosts" optimised for imitating text and collecting rewards, not survival. This explains their "jagged" performance profile: exceptional in RLVR-susceptible domains but easily fooled by jailbreaks. This framing also explains why benchmarks have become unreliable - they are verifiable environments immediately susceptible to "benchmaxxing" through training on adjacent data.

On the application side, Cursor demonstrated a new "LLM app" layer that bundles context engineering, orchestration, and domain-specific interfaces, while Claude Code proved the value of agents running locally on developer machines rather than in cloud containers. Karpathy coined "vibe coding" to describe the paradigm where anyone can build software through natural language, noting that code has become "free, ephemeral, malleable, discardable after single use." Looking ahead, he highlights Google's Gemini Nano "banana" model as an early hint of the "LLM GUI" - where AI communicates through images, infographics, and web apps rather than just text.

---
**Captured:** 23 December 2025

**Link:** https://karpathy.bearblog.dev/year-in-review-2025/

**Key Words:** RLVR; LLM Reasoning; Vibe Coding; AI Agents; Training Paradigms
