# ASI-Evolve: AI Accelerates AI
**Authors:** Weixian Xu, Tiantian Mi, Yixiu Liu, Yang Nan, Zhimeng Zhou, Lyumanshan Ye, Lin Zhang, Yu Qiao, Pengfei Liu

**Category:** Technical Fundamentals

**Published:** 31 March 2026

---

## Key Points
- ASI-Evolve is the first unified agentic framework to demonstrate AI-driven discovery across all three central pillars of AI development: data curation, neural architectures, and learning algorithms.
- In neural architecture design, the system discovered 105 state-of-the-art linear attention architectures, with the best surpassing DeltaNet by +0.97 points — nearly three times the gain of recent human-designed improvements.
- The framework augments evolutionary search with a cognition base that injects accumulated human priors and a dedicated analyzer that distills complex experimental outcomes into reusable insights.
- Discovered RL algorithms outperformed the GRPO baseline by up to +12.5 points on AMC32, while evolved data curation pipelines improved average benchmark performance by +3.96 points with MMLU gains exceeding 18 points.
- Initial evidence shows the AI-for-AI paradigm transfers beyond the AI stack, with positive results in mathematics and biomedicine including a +6.94 AUROC improvement in drug-target interaction prediction.

---

## Summary
ASI-Evolve addresses a fundamental question: can AI autonomously accelerate the development of AI itself? While recent agentic systems have demonstrated strong performance on well-scoped tasks with rapid feedback, it has remained unclear whether they can handle the costly, long-horizon, and weakly supervised research loops that drive real AI progress. The paper presents an agentic framework that closes this loop through a learn-design-experiment-analyze cycle, augmenting standard evolutionary approaches with two key components: a cognition base containing 150 domain literature entries that inject human priors to reduce the exploration space, and a dedicated analyzer that converts multi-dimensional experimental signals into structured, decision-oriented reports for future iterations.

The framework is evaluated across three foundational components of AI development. In neural architecture design, 1,773 exploration rounds produced 1,350 candidate architectures, yielding 105 that surpassed the state of the art for linear attention. In pretraining data curation, evolved strategies identified and eliminated quality issues across 672 billion tokens of academic content, producing substantial benchmark improvements. In reinforcement learning algorithm design, 300 rounds generated 10 algorithm variants outperforming the GRPO baseline, introducing innovations such as pairwise asymmetric optimization and budget-constrained dynamic radius mechanisms. The system also achieved competitive results on the circle packing benchmark, reaching state-of-the-art performance in just 17 rounds compared to over 460 for competing approaches.

Ablation studies confirm that both the cognition base and analyzer independently contribute value — the cognition base accelerates cold-start exploration while the analyzer sustains improvement over longer horizons. Importantly, the framework demonstrates transferability beyond the AI stack, with drug-target interaction experiments in biomedicine showing meaningful gains in cold-start and out-of-distribution scenarios. Together, these results suggest that closed-loop AI-driven research across data, architectures, and algorithms is becoming feasible, representing a promising step toward AI systems that can meaningfully accelerate their own foundational development.

---
**Captured:** 2026-04-14

**Link:** https://arxiv.org/abs/2603.29640

**Key Words:** Neural Architecture Search; AI-for-AI; Evolutionary Algorithms; Reinforcement Learning; Data Curation
