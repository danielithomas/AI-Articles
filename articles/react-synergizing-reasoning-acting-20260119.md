# ReAct: Synergizing Reasoning and Acting in Language Models
**Authors:** Shunyu Yao, Jeffrey Zhao, Dian Yu, Nan Du, Izhak Shafran, Karthik Narasimhan, Yuan Cao

**Category:** Technical Fundamentals

**Published:** October 2022 (ICLR 2023)

---

## Key Points
- ReAct interleaves reasoning traces (verbal thoughts) with task-specific actions, creating synergy where reasoning guides action planning and actions provide external information for grounded reasoning.
- On knowledge-intensive tasks (HotpotQA, FEVER), ReAct overcomes hallucination issues prevalent in chain-of-thought prompting by grounding reasoning in external knowledge retrieval via Wikipedia API interaction.
- On interactive decision-making benchmarks (ALFWorld, WebShop), ReAct outperformed imitation and reinforcement learning methods by absolute success rates of 34% and 10% respectively, using only one or two in-context examples.
- The approach produces more interpretable and trustworthy task-solving trajectories, enabling humans to inspect reasoning traces, verify factual correctness, and even intervene by editing thoughts.
- Combining ReAct with chain-of-thought self-consistency yields the best overall results, effectively leveraging both internal model knowledge and externally retrieved information.

---

## Summary
ReAct introduces a general paradigm for combining reasoning and acting in large language models. The key insight is that human intelligence seamlessly integrates task-oriented actions with verbal reasoning (inner speech) for self-regulation, strategisation, and maintaining working memory. ReAct augments an agent's action space to include both domain-specific actions and free-form language thoughts. Thoughts do not affect the external environment but serve to compose useful information, track progress, handle exceptions, and support future reasoning or acting.

The paper demonstrates ReAct's effectiveness across four diverse benchmarks. For knowledge-intensive reasoning (HotpotQA question answering and FEVER fact verification), models interact with a Wikipedia API using search, lookup, and finish actions. Analysis shows that while chain-of-thought is more flexible in formulating reasoning structures, it suffers from hallucination (56% of failures), whereas ReAct's grounded approach produces more factual trajectories with only 0% hallucination failures. For decision-making tasks (ALFWorld text game and WebShop online shopping), ReAct's sparse thoughts help decompose goals, track subgoals, and apply commonsense knowledge about where objects might be found.

The framework offers several advantages: it is intuitive to design (annotators simply write their thoughts alongside actions), general and flexible (works across diverse tasks with distinct action spaces), and performant with few examples. Fine-tuning experiments show that ReAct becomes the best-performing method when trained on 3,000 examples, outperforming approaches that teach models to memorise facts rather than how to reason and act to access information. The authors note that scaling ReAct with multi-task training and combining it with reinforcement learning could further unlock LLM potential for broader applications.

---
**Captured:** 2026-01-19

**Link:** https://arxiv.org/abs/2210.03629

**Key Words:** ReAct; Reasoning; Agents; Prompting; LLM

