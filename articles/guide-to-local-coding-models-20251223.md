# [Revised] You Don't Need to Spend $100/mo on Claude Code: Your Guide to Local Coding Models
**Authors:** Logan Thorneloe

**Category:** Tooling & Technology

**Published:** 20 December 2025

---

## Key Points
- Local coding models can complete approximately 90% of developer tasks as effectively as frontier cloud-based tools, performing about half a generation behind cloud offerings.
- The author's original hypothesis that local models could replace $100/month subscriptions was ultimately incorrect - the final 10% of performance is critical for professional work.
- Tooling quality varies significantly; common issues include broken tool calling, unclosed thinking traces, and model compatibility problems with coding interfaces.
- Memory management is crucial: model parameters and context window both consume RAM, with quantisation offering trade-offs between memory savings and performance degradation.
- MacBook hardware with unified memory architecture is optimal for local model serving, with MLX offering up to 20% faster token generation than Ollama.

---

## Summary
The article documents an experiment where the author purchased a MacBook Pro with 128GB RAM to test whether running local AI coding models could replace expensive cloud-based subscriptions like Claude Code. The author explored various local model serving tools (MLX and Ollama), coding interfaces (Qwen Code, Aider, OpenCode), and models (Qwen3-Coder, GPT-OSS), documenting the technical considerations around memory management, quantisation, and context window sizing.

After extensive testing, the author revised their initial conclusion. While local models proved capable of handling most coding tasks, the critical 10% of performance - particularly for complex, production-level work - makes paid cloud tools worthwhile for professional developers. The experiment also highlighted that running development tools like Docker alongside local models significantly impacts available RAM and model performance.

The article provides practical guidance for setting up local coding environments, including step-by-step instructions for MLX-based serving and model configuration. The author notes that Google's free-tier offerings (Gemini CLI, Jules) further complicate the cost-benefit analysis, though local models remain valuable for privacy-sensitive applications, offline work, and as supplementary tools to reduce cloud API consumption.

---
**Captured:** 23 December 2025

**Link:** https://www.aiforswes.com/p/you-dont-need-to-spend-100mo-on-claude

**Key Words:** Local LLM; Coding Assistant; Ollama; MLX; Quantisation
