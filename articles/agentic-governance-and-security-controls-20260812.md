# Agentic Governance & Security Controls (AGSC)
**Authors:** COHUMAIN Labs & SafeAlign AI

**Category:** Strategy & Governance

**Published:** 2026 (v1.0)

---

## Key Points
- AGSC is an open, vendor-neutral standard of 25 risk-justified controls for autonomous and generative AI systems, organised across four pillars: Safety (5), Alignment (5), Governance (8) and Security (7).
- Its central claim is that for an autonomous agent, governance and security are the same question — the autonomy that creates the governance problem (what may an agent decide?) is the same autonomy that defines the attack surface (what can a compromised agent execute?).
- Three failure-mode observations drive the design: agents invert the safe state by continuing to act wrongly at machine speed rather than stopping, the model itself is an attack surface because prompt injection lives in plain language invisible to code analysis, and orchestration is the primary risk.
- The security controls are grounded in Anthropic's analysis of a year of AI-enabled attacks — 832 actors and 13,873 observations mapped onto MITRE ATT&CK — which found the highest-risk operations were distinguished not by attacker skill but by agents autonomously chaining attack stages.
- Adoption is graduated through three conformance tiers — Foundational (8 controls), Managed (18 cumulative) and Assured (all 25, with continuous verification and third-party attestation for EU AI Act high-risk readiness).

---

## Summary
The Agentic Governance & Security Controls standard, published by COHUMAIN Labs and SafeAlign AI, argues that the conventional separation of governance and security across different teams breaks down for autonomous agents. Traditional IT treats governance as a policy question handled by risk and compliance functions and security as a technical question handled by engineering, but an agent's autonomy makes these the same concern viewed from two directions. The framework consolidates both into a single catalogue of 25 controls spanning Safety (kill-switch mechanisms, content safety, anti-hallucination, output monitoring, oversight procedures), Alignment (autonomy boundaries, human oversight, interpretability, explainability, labelling), Governance (data and model provenance, change management, third-party oversight, training documentation, evaluation, drift detection, end-of-life management, carbon footprint) and Security (multi-agent coordination defence, agent identity, injection defence, observability, threat modelling, security testing, memory protection).

The design rests on three observations about how agentic systems fail differently. First, an inversion of the safe state: conventional systems fail safely by stopping, whereas agents fail by continuing to operate while acting wrongly, and doing so at machine velocity. Second, the model is itself an attack surface, since prompt injection exists as plain-language data rather than executable code and is therefore invisible to conventional static analysis. Third, orchestration rather than individual technique is the primary risk — the standard cites Anthropic's mapping of 832 real-world malicious actors and 13,873 observations onto MITRE ATT&CK, where the highest-risk operations were set apart by agents autonomously chaining attack stages rather than by attacker skill. Prominent observed techniques include T1587 Develop Capabilities (~69%), T1027 Obfuscated Files (~65%), T1005 Data from Local System (~56%) and T1562 Impair Defenses (~55%). The authors flag a deliberate gap: "Agentic Orchestration" has no ATT&CK identifier, despite describing the autonomous, multi-step, tool-connected attack chain unique to agent systems.

To make the catalogue defensible under regulatory scrutiny, every control carries four mappings to external sources: the MIT AI Risk Repository (1,700+ risks across seven domains), MITRE ATLAS, MITRE ATT&CK with the Anthropic Navigator layer, and regulatory standards including the EU AI Act, NIST AI RMF and ISO/IEC 42001. Eight of the controls are described as AI-native, with no traditional IT analogue. Adoption is staged across three conformance tiers — Foundational (8 controls) as a minimum production baseline for the highest-severity and fastest-moving threats, Managed (18 cumulative) for material or customer-facing systems, and Assured (all 25) with continuous compliance verification and third-party attestation aimed at EU AI Act high-risk readiness. The standard is released openly under MIT and CC BY 4.0 licences with a GitHub implementation, a scanner tool for assessing agents, and an EU AI Act crosswalk, and it operationalises peer-reviewed work including ICLR 2026 research on meta-governance of multi-agent systems and IASEAI 2026 work on governance-and-security-by-design.

---
**Captured:** 12 August 2026

**Link:** https://himjoe.github.io/Agentic-governance-and-security-controls-by-COHUMAIN-Labs-and-Safealign-AI/COHUMAIN-AGSC-repo/docs/

**Key Words:** Agentic Governance; Security Controls; AI Standards; EU AI Act; MITRE ATT&CK
