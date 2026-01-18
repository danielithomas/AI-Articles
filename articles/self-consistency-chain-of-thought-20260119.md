# Self-Consistency Improves Chain of Thought Reasoning in Language Models
**Authors:** Xuezhi Wang, Jason Wei, Dale Schuurmans, Quoc Le, Ed H. Chi, Denny Zhou

**Category:** Technical Fundamentals

**Published:** 21 March 2022 (ICLR 2023)

---

## Key Points
- Self-consistency is a decoding strategy that samples diverse reasoning paths and selects the most consistent answer through majority voting, replacing naive greedy decoding in chain-of-thought prompting
- Achieves substantial improvements on reasoning benchmarks: GSM8K (+17.9%), SVAMP (+11.0%), AQuA (+12.2%), StrategyQA (+6.4%), and ARC-challenge (+3.9%)
- Leverages the insight that complex reasoning problems typically admit multiple valid reasoning paths leading to the same correct answer
- Functions as a drop-in replacement for greedy decoding without requiring additional training, fine-tuning, or architectural changes
- Performance scales with the number of sampled reasoning paths, with gains continuing as sample count increases

---

## Summary
This paper introduces self-consistency, a decoding strategy designed to improve chain-of-thought prompting in large language models. The core insight is that complex reasoning tasks typically admit multiple different reasoning paths that converge on the same correct answer. Rather than relying on greedy decoding (which selects only the single most likely reasoning path), self-consistency samples a diverse set of reasoning paths from the model's decoder and determines the final answer through majority voting.

The method operates in three stages: first, the language model is prompted with chain-of-thought exemplars demonstrating step-by-step reasoning; second, multiple reasoning paths are sampled from the model using temperature-based sampling; third, the most commonly occurring final answer across all sampled paths is selected as the output. This approach is analogous to human intuition that if multiple independent reasoning approaches lead to the same conclusion, confidence in that answer increases.

Empirical evaluation across four large language models demonstrates that self-consistency significantly boosts chain-of-thought performance on arithmetic and commonsense reasoning benchmarks. The technique is particularly effective because it requires no additional training, fine-tuning, or changes to the underlying model - it operates purely at inference time by leveraging the model's existing capabilities more effectively through diverse sampling and aggregation.

---
**Captured:** 19 January 2026

**Link:** https://arxiv.org/pdf/2203.11171

**Key Words:** Chain of Thought; Self-Consistency; Reasoning; Decoding; Prompting
