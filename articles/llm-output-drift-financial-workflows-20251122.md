# LLM Output Drift: Cross-Provider Validation & Mitigation for Financial Workflows
**Authors:** Raffi Khatchadourian, Rolando Franco

**Category:** Technical Fundamentals

**Published:** November 2025

---

## Key Points
- Smaller language models (7-8B parameters) achieve 100% output consistency at T=0.0, while larger models (120B) exhibit only 12.5% consistency regardless of configuration.
- Output drift undermines auditability in financial AI systems, creating compliance risks that negate automation benefits through verification overhead.
- Cross-provider validation demonstrates that deterministic behaviour transfers successfully between local (Ollama) and cloud (IBM watsonx.ai) deployments.
- Structured tasks (SQL generation) maintain stability even at T=0.2, while RAG tasks show substantial drift (25-75%), revealing task-dependent sensitivity.
- The research introduces a three-tier model classification system enabling risk-appropriate deployment decisions for regulated financial applications.

---

## Summary
This paper presents the first comprehensive framework for measuring and mitigating Large Language Model (LLM) output drift in financial services deployments. The research reveals a critical inverse relationship between model size and deterministic behaviour: smaller, well-engineered models (Granite-3-8B, Qwen2.5-7B) achieve perfect output consistency essential for regulatory compliance, while larger frontier models (GPT-OSS-120B) fail to meet audit requirements with only 12.5% consistency even at zero temperature.

The authors evaluated five model architectures (7B-120B parameters) across 480 experimental runs covering three regulated financial tasks: SEC 10-K filing analysis (RAG), policy-bounded JSON summarisation, and text-to-SQL generation. Their finance-calibrated deterministic test harness combines greedy decoding, fixed seeds, and SEC structure-aware retrieval ordering with domain-specific validation invariants including ±5% materiality thresholds and citation accuracy requirements.

The framework maps directly to Financial Stability Board (FSB), Bank for International Settlements (BIS), and Commodity Futures Trading Commission (CFTC) requirements, providing practical pathways for compliance-ready AI deployments. The research demonstrates that architectural design and parameter efficiency—not scale alone—determine compliance viability in financial applications, supporting a fit-for-purpose approach where 7-8B parameter models optimise both regulatory compliance and operational efficiency.

---
**Captured:** 2025-11-22

**Link:** https://arxiv.org/abs/2511.07585

**Key Words:** LLM; financial services; regulatory compliance; output drift; model determinism
