# Adversarial Poetry as a Universal Single-Turn Jailbreak Mechanism in Large Language Models
**Authors:** P. Bisconti, M. Prandi, F. Pierucci, F. Giarrusso, M. Bracale, M. Galisai, V. Suriani, O. Sorokoletova, F. Sartore, D. Nardi

**Category:** Security & Risk

**Published:** 20 November 2025

---

## Key Points
- Adversarial poetry achieves 62% average attack success rate across 25 frontier LLMs, with some providers exceeding 90%, demonstrating that poetic reformulation functions as a universal single-turn jailbreak technique.
- The vulnerability spans all major risk domains including CBRN hazards, cyber-offence, manipulation, and loss-of-control scenarios, indicating the attack exploits general safety mechanisms rather than domain-specific filters.
- Converting 1,200 MLCommons harmful prompts into verse produced attack success rates up to 18 times higher than prose baselines, with effectiveness comparable to or exceeding specialised jailbreak techniques.
- Smaller models demonstrated greater resilience than larger counterparts within the same families, suggesting an inverse relationship between capability and robustness under stylistic perturbation.
- The vulnerability persists across all alignment approaches tested (RLHF, Constitutional AI, mixture-of-experts), revealing fundamental limitations in current safety training methods that fail to generalise across stylistic variations.

---

## Summary
Researchers from DEXAI-Icaro Lab and Sapienza University of Rome have demonstrated that reformulating harmful requests as poetry systematically bypasses safety mechanisms in large language models. Testing 25 frontier models from nine providers (Google, OpenAI, Anthropic, Deepseek, Qwen, Mistral AI, Meta, xAI, and Moonshot AI), the study found that poetic prompts achieved an overall attack success rate of 62%, with individual providers showing rates as high as 90-100%. The attacks required no iterative refinement or multi-turn interaction, functioning purely through single-turn stylistic transformation whilst maintaining semantic intent.

The research employed two complementary datasets: 20 hand-crafted adversarial poems and 1,200 systematically transformed MLCommons harmful prompts. Using an ensemble of three open-weight judge models validated against human annotations, the team evaluated outputs across CBRN hazards, cyber-offence capabilities, harmful manipulation, and loss-of-control scenarios. The poetic transformations produced attack success rates up to three times higher than prose equivalents, with privacy-related prompts showing the most extreme vulnerability (increasing from 8.07% to 52.78%). Notably, the effect proved independent of model architecture, with both proprietary and open-weight systems displaying comparable susceptibility.

The findings reveal a systematic vulnerability stemming from how current alignment methods handle stylistic variation. Smaller models exhibited greater refusal stability than larger counterparts within the same families, suggesting capability gains do not automatically translate to robustness. The cross-provider consistency (ranging from 3.12% to 62.15% increase in attack success rates) indicates the vulnerability emerges from fundamental limitations in contemporary safety training approaches rather than implementation-specific weaknesses. The research highlights critical gaps in current evaluation protocols and regulatory frameworks, demonstrating that benchmark-based compliance assessments may systematically overstate real-world robustness when models encounter inputs outside their prosaic training distribution.

---
**Captured:** 05 January 2026

**Link:** https://arxiv.org/html/2511.15304v2

**Key Words:** LLM Security; Jailbreak; Adversarial Attacks; AI Safety; Alignment
