# Measuring AI Agent Autonomy in Practice
**Authors:** Miles McCain, Thomas Millar, Saffron Huang, Jake Eaton, Kunal Handa, Michael Stern, Alex Tamkin, Matt Kearney, Esin Durmus, Judy Shen, Jerry Hong, Brian Calvert, Jun Shern Chan, Francesco Mosconi, David Saunders, Tyler Neylon, Gabriel Nicholas, Sarah Pollack, Jack Clark, Deep Ganguli

**Category:** Architecture & Operations

**Published:** 18 February 2026

---

## Key Points
- Among the longest-running Claude Code sessions, autonomous turn duration nearly doubled over three months (from under 25 minutes to over 45 minutes), with growth smooth across model releases - suggesting a deployment overhang where models are capable of more autonomy than they exercise in practice.
- Experienced Claude Code users shift from approving individual actions to a monitoring-and-intervening oversight style, with auto-approve usage rising from roughly 20% to over 40% while interrupt rates also increase with experience.
- Agent-initiated stops (Claude pausing to ask for clarification) occur more frequently than human-initiated interruptions, particularly on complex tasks - demonstrating that training models to recognise their own uncertainty is a valuable safety property.
- Analysis of nearly one million API tool calls shows 80% have some form of safeguard, 73% appear to have a human in the loop, and only 0.8% of actions are irreversible - though high-risk deployments in healthcare, finance, and cybersecurity are emerging.
- Software engineering accounts for nearly 50% of all agentic API activity, but the frontier of risk and autonomy is expected to expand as agents move into higher-stakes domains where output verification is more difficult.

---

## Summary
Anthropic analysed millions of human-agent interactions across Claude Code and their public API using their privacy-preserving Clio tool to empirically study how much autonomy people grant AI agents in real-world deployments. The study adopted a practical definition of agents as AI systems equipped with tools that allow them to take actions, and developed complementary metrics from two data sources: the public API (broad visibility across thousands of customers at the individual tool-call level) and Claude Code (deep session-level insight into a single product).

The findings reveal that agent autonomy is co-constructed by the model, the user, and the product rather than being a fixed property. In Claude Code, the longest autonomous sessions nearly doubled in duration over three months, while experienced users shifted from step-by-step approval to a supervisory oversight style - granting more autonomy but also interrupting more often when needed. Notably, Claude itself limits its own autonomy by pausing for clarification more frequently than humans interrupt it, particularly on complex tasks. On the public API, most agent actions remain low-risk and concentrated in software engineering, though emerging usage in healthcare, finance, and cybersecurity signals expansion into higher-stakes domains.

The researchers conclude that effective oversight requires new post-deployment monitoring infrastructure and new human-AI interaction paradigms, rather than mandating specific interaction patterns like requiring approval for every action. They recommend that model developers train models to recognise their own uncertainty, product developers invest in tools that give users trustworthy visibility into agent behaviour, and policymakers avoid prescribing rigid oversight requirements that may not match how experienced users actually supervise agents.

---
**Captured:** 23 February 2026

**Link:** https://www.anthropic.com/research/measuring-agent-autonomy

**Key Words:** AI Agents; Autonomy; Human Oversight; Post-deployment Monitoring; Agent Safety
