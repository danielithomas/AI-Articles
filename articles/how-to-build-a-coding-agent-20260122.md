# how to build a coding agent: free workshop
**Authors:** Geoffrey Huntley

**Category:** Tooling & Technology

**Published:** 24 August 2025

---

## Key Points
- Building a coding agent requires only approximately 300 lines of code running in a loop with LLM tokens, demystifying the perceived complexity of these tools.
- The five core primitives of any coding agent are: read_file (reading file contents), list_files (directory listing), bash (command execution), edit_file (applying code edits), and code_search (pattern matching with ripgrep).
- Agentic models like Claude Sonnet are trained to bias toward action and tool-calling rather than extended reasoning, making them ideal for iterative agent workflows.
- Context window management is critical for agent performance - excessive allocation degrades outcomes, so the context window should be treated like limited computer memory.
- Understanding how to build agents is now fundamental professional knowledge that transforms developers from passive AI consumers into active producers who can automate workflows.

---

## Summary
This article presents a practical workshop on building coding agents from first principles. Geoffrey Huntley, an engineer at Sourcegraph, demystifies coding agents by explaining they are simply approximately 300 lines of code running in a loop with LLM tokens. The article walks through building a basic agent by implementing five core primitives: read_file (reading file contents), list_files (directory listing), bash (command execution), edit_file (applying code edits), and code_search (using ripgrep for pattern matching).

The tutorial emphasises that models like Claude Sonnet are "agentic" because they're trained to bias toward tool-calling actions rather than extended reasoning, functioning like a "digital squirrel" chasing tool calls. A critical concept introduced is context window management - treating it like limited computer memory where excessive allocation degrades performance. The article argues that understanding agent fundamentals is now essential professional knowledge for 2025, transforming developers from passive AI consumers into active producers who can automate workflows.

Using Go code examples, the workshop demonstrates how Model Context Protocols (MCPs) are simply function registrations with descriptions that guide the LLM to invoke tools, and how the inferencing loop processes user input and tool results iteratively. The article also discusses LLM specialisations, categorising models as either high safety, low safety, oracle (for reasoning), or agentic (for tool-calling), emphasising that different models serve different purposes and shouldn't be compared solely on context window size and cost.

---
**Captured:** 22 January 2026

**Link:** https://ghuntley.com/agent/

**Key Words:** AI Agents; Coding Assistants; LLM; Tool Calling; Developer Productivity
