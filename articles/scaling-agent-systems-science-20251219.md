# Towards a Science of Scaling Agent Systems
**Authors:** Yubin Kim, Ken Gu, Chanwoo Park, Chunjong Park, Samuel Schmidgall, A. Ali Heydari, Yao Yan, Zhihan Zhang, Yuchen Zhuang, Yun Liu, Mark Malhotra, Paul Pu Liang, Hae Won Park, Yuzhe Yang, Xuhai Xu, Yilun Du, Shwetak Patel, Tim Althoff, Daniel McDuff, Xin Liu

**Category:** Architecture & Operations

**Published:** December 2025

---

## Key Points
- Multi-agent systems (MAS) show highly domain-dependent performance ranging from +81% improvement to -70% degradation depending on task structure and coordination architecture
- A predictive scaling model using empirical coordination metrics achieves R²=0.524 and correctly predicts optimal architectures for 87% of held-out task configurations
- Tool-heavy tasks suffer disproportionately from multi-agent coordination overhead, creating a "tool-coordination trade-off"
- Coordination yields diminishing or negative returns once single-agent baselines exceed approximately 45% accuracy (capability saturation)
- Error amplification varies dramatically by architecture: independent agents amplify errors 17.2× while centralised coordination contains this to 4.4×

---

## Summary
This research from Google Research and MIT establishes quantitative scaling principles for agent systems through a comprehensive evaluation spanning 180 controlled configurations across three LLM families (OpenAI, Google, Anthropic) and four agentic benchmarks covering financial reasoning, web navigation, game planning, and workflow execution. The authors systematically evaluate five canonical architectures - Single Agent System (SAS) and four Multi-Agent System variants (Independent, Centralised, Decentralised, Hybrid) - while standardising tools, prompt structures, and token budgets to isolate architectural effects from implementation confounds.

The study reveals that multi-agent system effectiveness is governed by quantifiable trade-offs rather than simple "more agents is better" heuristics. Three dominant patterns emerge: a tool-coordination trade-off where tool-heavy tasks suffer from coordination overhead, capability saturation where coordination yields diminishing returns beyond approximately 45% single-agent performance, and architecture-dependent error amplification ranging from 4.4× (centralised) to 17.2× (independent). Performance varies dramatically by task structure - centralised coordination improves performance by 80.8% on parallelisable financial reasoning tasks, while decentralised coordination excels on dynamic web navigation (+9.2%), yet every multi-agent variant degrades performance by 39-70% on sequential planning tasks.

The researchers derive a predictive scaling model using empirical coordination metrics (efficiency, overhead, error amplification, redundancy) that achieves cross-validated R²=0.524 and correctly predicts optimal coordination strategies for 87% of held-out configurations. Out-of-sample validation on GPT-5.2 (released after the study) confirms that four of five scaling principles generalise to unseen frontier models with MAE=0.071. This provides practitioners with quantitative guidance for architecture selection based on measurable task properties - including task decomposability, tool complexity, and baseline difficulty - rather than relying on heuristics.

---
**Captured:** 19 December 2025

**Link:** https://arxiv.org/html/2512.08296v2

**Key Words:** Multi-Agent Systems; Agent Architectures; Scaling Laws; Coordination; AI Agents
