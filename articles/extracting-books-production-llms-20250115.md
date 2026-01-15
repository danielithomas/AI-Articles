# Extracting Books from Production Language Models
**Authors:** Ahmed Ahmed, A. Feder Cooper, Sanmi Koyejo, Percy Liang

**Category:** Security & Risk

**Published:** 6 January 2026

---

## Key Points
- Production LLMs (Claude 3.7 Sonnet, GPT-4.1, Gemini 2.5 Pro, Grok 3) can be induced to emit near-verbatim copyrighted text despite safety guardrails.
- A two-phase extraction procedure was used: initial probing with Best-of-N jailbreaking where needed, followed by iterative continuation prompts.
- Some models (Gemini 2.5 Pro, Grok 3) complied directly without jailbreaking; others (Claude 3.7 Sonnet, GPT-4.1) required adversarial techniques.
- Extraction success varied significantly - Claude 3.7 Sonnet achieved 95.8% near-verbatim recall on Harry Potter when jailbroken, while GPT-4.1 achieved only 4.0%.
- Findings have direct relevance to ongoing copyright litigation concerning whether LLM training and output generation constitute copyright infringement.

---

## Summary
This research paper investigates whether copyrighted books memorised during training can be extracted from production (consumer-facing) LLMs that implement safety guardrails. While prior work demonstrated such extraction from open-weight models like Llama 3.1 70B, it remained an open question whether production systems with safety measures would be similarly vulnerable to memorisation attacks.

The researchers tested four production LLMs (Claude 3.7 Sonnet, GPT-4.1, Gemini 2.5 Pro, and Grok 3) using a two-phase approach: first probing extraction feasibility using a seed text prefix (with Best-of-N jailbreaking for models that initially refused), then iteratively prompting the model to continue the text. They measured success using a "near-verbatim recall" metric based on matching text blocks between generated output and the original book.

The results demonstrated that significant extraction was possible from all four models, though success varied considerably. Claude 3.7 Sonnet achieved 95.8% near-verbatim recall on Harry Potter and the Sorcerer's Stone when jailbroken, while Gemini 2.5 Pro and Grok 3 complied directly without jailbreaking, achieving 76.8% and 70.3% respectively. GPT-4.1 showed stronger resistance with only 4.0% recall. These findings are directly relevant to ongoing copyright litigation, as they provide empirical evidence that production LLMs can reproduce substantial portions of copyrighted training material through relatively simple extraction techniques.

---
**Captured:** 15 January 2026

**Link:** https://arxiv.org/abs/2601.02671

**Key Words:** LLM; Copyright; Memorisation; Jailbreaking; Training Data Extraction

