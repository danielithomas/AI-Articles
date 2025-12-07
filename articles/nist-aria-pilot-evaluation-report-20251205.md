# NIST ARIA 0.1: Pilot Evaluation Report - Assessing Risks and Impacts of AI
**Authors:** Razvan Amironesei, Afzal Godil, Craig Greenberg, Kristen Greene, Patrick Hall, Theodore Jensen, Jonathan Fiscus, Noah Schulman

**Category:** Strategy & Governance

**Published:** November 2025

---

## Key Points
- ARIA (Assessing Risks and Impacts of AI) is a new NIST program that pairs humans with AI applications to evaluate real-world risks and impacts through scenario-based interactions, performing the Measure function described in the NIST AI Risk Management Framework.
- The pilot evaluation tested seven AI applications across three integrated layers: testing (model testing, red teaming, field testing), assessment (dialogue annotation and post-task questionnaires), and measurement (using the Contextual Robustness Index - CoRIx).
- Three proxy scenarios were designed to represent real-world risks: TV Spoilers (privileged information disclosure), Meal Planner (safety risks regarding dietary restrictions), and Pathfinder (confabulation/factual accuracy in travel information).
- CoRIx measurement trees provide a transparent, multidimensional visualisation of AI system validity risks, enabling stakeholders to trace scores back through testing levels to specific data inputs.
- The pilot demonstrates the feasibility of combining expert annotator judgements with human tester perceptions to characterise AI application behaviour - revealing that these two data sources can yield different insights about the same system.

---

## Summary
This NIST publication documents ARIA 0.1, the pilot evaluation for the Assessing Risks and Impacts of AI program launched in May 2024. ARIA represents a significant methodological advancement in AI evaluation by moving beyond traditional benchmark testing to capture how AI systems behave in realistic human interactions. The framework consists of three interconnected layers: the testing layer (which generates data through model testing with predefined prompts, red teaming for adversarial stress-testing, and field testing for realistic use scenarios), the assessment layer (comprising trained annotator dialogue analysis and post-task questionnaires capturing user perceptions), and the measurement layer (using the novel Contextual Robustness Index to synthesise findings into interpretable metrics).

The pilot involved five organisations submitting seven AI applications, evaluated across three carefully designed scenarios serving as proxies for real-world risks. The TV Spoilers scenario tested applications' ability to shield plot information while remaining helpful - a proxy for privileged information risks. The Meal Planner scenario evaluated adherence to dietary restrictions - a proxy for safety risks. The Pathfinder scenario tested factual accuracy in travel recommendations - a proxy for confabulation risks. Each scenario established specific guardrails defining permitted and prohibited application behaviours. The evaluation produced 508 testing sessions and over 1,500 annotations, with 51 red teamers and 19 field testers participating between December 2024 and January 2025.

The Contextual Robustness Index (CoRIx) measurement trees represent a key methodological contribution. Unlike unidimensional metrics, CoRIx uses tree structures where each level provides increasingly granular information, from high-level validity risk scores down to individual annotator and questionnaire responses. This transparency enables stakeholders to understand precisely which factors contribute to an application's risk profile. Preliminary results showed that well-resourced organisations' applications generally performed better, all applications exhibited some risk related to dialogue naturalness and superfluous information, and notably, expert annotator judgements sometimes diverged from user perceptions - underscoring the value of triangulating multiple data sources. NIST plans to refine the framework through improved documentation, expanded sector-specific scenarios, and enhanced annotation tools for future ARIA evaluations.

---
**Captured:** 5 December 2025

**Link:** https://doi.org/10.6028/NIST.AI.700-2

**Key Words:** AI; Evaluation; Risk Assessment; Sociotechnical; Trustworthiness
