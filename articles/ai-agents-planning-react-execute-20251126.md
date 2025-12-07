# Writing AI Agents From Scratch: Planning Is The Key
**Authors:** Paul Iusztin

**Category:** Architecture & Operations

**Published:** 11 November 2025

---

## Key Points
- Planning is the critical component that separates true AI agents from simple tool loops, enabling the transition from workflow to agent.
- ReAct (Reason + Act) interleaves thinking, acting, and observing in a continuous cycle, allowing dynamic adjustment based on feedback.
- Plan-and-Execute separates comprehensive planning from execution, enabling more efficient batch-style processing with parallel task execution.
- Modern reasoning LLMs combine planning and execution into a single API call, simplifying implementation whilst maintaining conceptual separation.
- Chain-of-thought prompting lacks clear separation between planning and action, making it difficult to build iterative loops with environmental feedback.

---

## Summary

This article examines planning as the fundamental distinction between simple tool-calling workflows and genuine AI agents. The author draws from experience building ZTRON, a financial services AI agent, where an initial agentic RAG system failed due to lack of structured planning. Simply running tools in a loop without proper planning mechanisms resulted in the agent reacting to observations without clear strategy or goal decomposition.

The article presents two foundational planning patterns. ReAct (Reason + Act) creates a tight loop of Thought → Action → Observation, allowing agents to dynamically adjust plans based on environmental feedback. Each cycle involves forming a reasoning step, calling a tool, obtaining results, and using that observation to inform the next thought. This pattern offers high interpretability and natural error recovery but can be slower due to its sequential nature. Plan-and-Execute provides a more structured alternative, separating high-level strategic planning from low-level execution. A Planner decomposes goals into multi-step plans, an Evaluator validates logical consistency before execution, and an Executor implements the validated plan with potential for parallel processing.

Modern reasoning LLMs have evolved to integrate planning and execution into single API calls through internal "thinking" features. This optimisation maintains the conceptual separation between planning and action whilst simplifying implementation, making systems faster and more cost-effective. The article emphasises that most production AI agents use derivatives of these foundational patterns, and understanding ReAct and Plan-and-Execute equips developers to build custom solutions or comprehend existing architectures. The key insight is that agents require both tools and planning operating within a loop, with the planning mechanism providing the structure necessary for handling complex scenarios involving multiple tools.

---
**Captured:** 26-Nov-2025

**Link:** https://www.decodingai.com/p/ai-agents-planning

**Key Words:** AI; Agents; Planning; ReAct; Architecture
