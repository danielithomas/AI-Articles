# Security Knowledge Dilution in Large Language Models: How Irrelevant Context Degrades Critical Domain Expertise

**Authors:** Shivani Shukla (University of San Francisco), Himanshu Joshi (Vector Institute for Artificial Intelligence)

**Category:** Security & Risk

**Published:** December 2025

---

## Key Points

- LLMs experience "knowledge dilution" where domain-specific expertise systematically degrades when exposed to large volumes of irrelevant but contextually plausible information.
- Security feature implementation drops by 47% as context dilution increases from 0 to 40,000 tokens, with statistical significance (p < 0.001) across 400 controlled experiments using GPT-4.
- Multi-step security features requiring coordination of multiple constraints show greater vulnerability to dilution (68-73% reduction) compared to fundamental patterns like prepared statements (23% reduction).
- The degradation follows an exponential decay pattern and occurs gradually rather than as a binary failure, making it difficult to detect without systematic evaluation.
- Tasks with higher cognitive complexity demonstrate greater sensitivity to dilution effects, suggesting that complex domain reasoning is more fragile than basic pattern application.

---

## Summary

This NeurIPS 2025 workshop paper introduces and investigates the phenomenon of "knowledge dilution" in large language models, demonstrating how specialised expertise systematically degrades when models are exposed to large volumes of irrelevant but contextually relevant information. Through 400 controlled experiments using GPT-4 across varying levels of context dilution (from 0 to 40,000 tokens), the researchers tested security-focused code generation tasks and measured the implementation of critical security features. The theoretical framework builds on cognitive load theory and attention-based learning models, proposing that dilution emerges from attentional resource competition, semantic interference, and priority recalibration mechanisms.

The study reveals that security feature implementation drops dramatically by 47% as context dilution increases, with the effect following an exponential decay pattern (R² = 0.573). More sophisticated security measures requiring coordination of multiple constraints—such as authorisation controls and secure error handling—showed greater vulnerability to dilution (68-73% reduction) compared to fundamental patterns like prepared statements (23% reduction). Tasks with higher cognitive complexity, such as session management and user search services, demonstrated greater sensitivity to dilution effects than simpler implementations like file upload handlers, suggesting that complex domain reasoning is more fragile than basic pattern application.

These findings have significant implications for AI safety and the deployment of LLMs in critical domains. Unlike adversarial attacks or jailbreaking, knowledge dilution occurs through seemingly benign interactions that gradually shift the model's attention away from domain-specific constraints. The research proposes several mitigation strategies including architectural approaches (separate context windows for domain-specific content, attention preservation mechanisms), and prompting techniques (periodic reinforcement of critical constraints, explicit importance ranking, selective context pruning). The broader implications extend beyond security to any specialised domain requiring sustained attention to domain-specific constraints, representing a fundamental limitation of current transformer architectures.

---

**Captured:** 10 December 2025

**Link:** https://www.techrxiv.org/users/983956/articles/1349576-security-knowledge-dilution-in-large-language-models-how-irrelevant-context-degrades-critical-domain-expertise

**Key Words:** LLM Security; Knowledge Dilution; Context Effects; AI Safety; Code Generation
