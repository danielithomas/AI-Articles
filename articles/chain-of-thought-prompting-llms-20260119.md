# Chain-of-Thought Prompting Elicits Reasoning in Large Language Models
**Authors:** Jason Wei, Xuezhi Wang, Dale Schuurmans, Maarten Bosma, Brian Ichter, Fei Xia, Ed Chi, Quoc Le, Denny Zhou

**Category:** Technical Fundamentals

**Published:** 28 January 2022 (revised 10 January 2023)

---

## Key Points
- Chain-of-thought prompting significantly improves LLM performance on complex reasoning tasks including arithmetic, commonsense, and symbolic reasoning.
- The technique is an emergent ability that only materialises at sufficient model scale (approximately 100B parameters).
- Using just eight chain-of-thought exemplars with a 540B parameter model achieved state-of-the-art on the GSM8K maths benchmark, surpassing even fine-tuned GPT-3.
- The approach requires no fine-tuning and works through simple few-shot prompting with step-by-step reasoning demonstrations.
- Chain-of-thought combines the strengths of rationale-augmented training with standard few-shot prompting while avoiding the limitations of both approaches.

---

## Summary
This foundational paper from Google Research introduces chain-of-thought prompting, a technique that significantly improves large language models' ability to perform complex reasoning tasks. The core insight is that generating intermediate reasoning steps - a "chain of thought" - enables models to decompose multi-step problems into manageable parts, mimicking how humans solve complex problems.

The researchers demonstrate that reasoning abilities emerge naturally in sufficiently large models when prompted with examples that show step-by-step reasoning. Rather than requiring expensive fine-tuning or new model architectures, the technique works by providing a few demonstrations where the reasoning process is made explicit. This simple approach yields striking improvements: a 540B parameter PaLM model achieved state-of-the-art performance on the challenging GSM8K maths benchmark using only eight exemplars.

Crucially, the paper establishes that chain-of-thought prompting is an emergent property of model scale - the benefits only appear in models of approximately 100 billion parameters or more. Smaller models showed flat or even negative effects from chain-of-thought prompting, suggesting this capability depends on sufficient model capacity. This discovery has had profound influence on both prompting practices and our understanding of how scale affects reasoning capabilities in LLMs.

---
**Captured:** 19 January 2026

**Link:** https://arxiv.org/abs/2201.11903

**Key Words:** Chain-of-Thought; Prompting; Reasoning; LLM; Few-Shot Learning
