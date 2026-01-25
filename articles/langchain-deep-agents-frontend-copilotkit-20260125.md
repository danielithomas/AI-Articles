# How to build a Frontend for LangChain Deep Agents with CopilotKit!
**Authors:** Anmol Baranwal and Nathan Tarbert

**Category:** Tooling & Technology

**Published:** 20 January 2026

---

## Key Points
- LangChain's Deep Agents provide a structured framework for building multi-agent systems with built-in planning, filesystem context, and subagent spawning capabilities.
- CopilotKit acts as a frontend runtime that keeps UI state synchronised with agent execution by streaming agent events and state updates in real-time using the AG-UI protocol.
- The architecture separates concerns by using a Next.js frontend for UI, a FastAPI backend for the Deep Agents service, and CopilotKit as the middleware layer connecting them.
- Deep Agents use three key middleware components: to-do list middleware for planning, filesystem middleware for context management, and subagent middleware for task delegation.
- The implementation demonstrates building a job search assistant that parses resumes, orchestrates web searches through subagents, and streams structured results back to the UI without polluting the chat interface.

---

## Summary
The article introduces how to build production-ready frontends for LangChain's Deep Agents using CopilotKit, addressing a common challenge in agentic systems where powerful backend agents lack proper UI integration. Deep Agents represent an evolution beyond simple "LLM in a loop" architectures by providing structured multi-agent systems with explicit planning, persistent filesystem context, and hierarchical task delegation through subagents. The framework packages these capabilities as middleware components that inject planning tools, file operations, and subagent spawning into standard LangGraph graphs.

The tutorial demonstrates this integration through a practical job search assistant that accepts resume uploads, extracts skills, and searches for relevant positions. The architecture uses a Next.js frontend with CopilotKit's React components, a FastAPI backend hosting the Deep Agents service, and the AG-UI protocol as the communication layer. CopilotKit's middleware enables real-time synchronisation between the UI and agent state, allowing structured tool outputs (like job listings) to render in dedicated UI components rather than cluttering the chat interface.

The implementation showcases key patterns including resume parsing with PDF extraction, skill detection, web search integration via Tavily, and controlled tool execution through strict system prompts. The Deep Agents graph orchestrates the workflow by planning search steps, delegating to specialised subagents for job discovery, and returning structured JSON results through explicit tool calls. This separation of concerns enables developers to build sophisticated agent applications with professional UIs whilst maintaining clean code organisation and real-time state management.

---
**Captured:** 25 January 2026

**Link:** https://www.copilotkit.ai/blog/how-to-build-a-frontend-for-langchain-deep-agents-with-copilotkit

**Key Words:** Deep Agents; CopilotKit; LangGraph; AG-UI; Multi-agent Systems
