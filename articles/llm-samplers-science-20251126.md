# The Underrated Science of LLM Samplers
**Authors:** Shmulik Cohen

**Published:** 25 November 2025

---

## Key Points
- LLM samplers are the algorithms that select which token (word) to generate next from the model's probability distribution, directly controlling the balance between predictable and creative outputs.
- Temperature adjusts the "sharpness" of probability distributions, where low values (e.g. 0.7) make outputs more deterministic whilst high values (e.g. 3.0) increase randomness and creativity.
- Top-P (Nucleus Sampling) adaptively selects the smallest set of tokens whose cumulative probability exceeds a threshold, making it smarter than fixed Top-K sampling.
- Min-P sampling dynamically adjusts the sampling pool based on the most likely token's probability, solving both the "long tail" problem and maintaining high-quality alternatives.
- Combining multiple sampling methods (e.g. Temperature with Top-P or Min-P) provides the most control over LLM output quality and creativity.

---

## Summary

LLM samplers are a critical but underrated component that determines how language models select their next word from probability distributions. When an LLM processes a prompt, it calculates probability scores for every possible token in its vocabulary (often 50,000+ words) using the Softmax function. The sampler then decides which token to actually generate, navigating the crucial trade-off between predictability and chaos.

Different sampling methods offer distinct approaches to this challenge. Greedy sampling always picks the highest probability token, resulting in deterministic but repetitive outputs. Temperature sampling adjusts the sharpness of the probability distribution before selection - lower temperatures make high-probability words more dominant, whilst higher temperatures flatten the distribution for more creative outputs. Top-K sampling considers only the K most probable tokens, but its fixed nature can be inflexible. Top-P (Nucleus Sampling) improves on this by adaptively selecting tokens until their cumulative probability reaches a threshold, making it responsive to the model's confidence level.

Min-P sampling represents a more recent advancement that sets a dynamic minimum probability threshold based on the top token's probability. This method effectively eliminates very low-probability "noise" tokens whilst preserving high-quality alternatives, and works particularly well even at high temperatures. Research shows Min-P outperforms Top-P on both benchmarks and human evaluations. In practice, combining methods - such as using Temperature to shape the distribution followed by Top-P or Min-P to filter options - provides the most nuanced control over LLM outputs, allowing practitioners to dial in the exact balance between coherence and creativity needed for their specific applications.

---
**Captured:** 26-Nov-2025

**Link:** https://www.decodingai.com/p/everything-you-need-to-know-about

**Key Words:** LLM; Sampling; Temperature; Probability; Text Generation
