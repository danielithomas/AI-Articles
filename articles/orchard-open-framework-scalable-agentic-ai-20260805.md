# Orchard: An Open Framework for Scalable Agentic AI
**Authors:** Baolin Peng; Wenlin Yao; Qianhui Wu; Hao Cheng; Jianfeng Gao (Microsoft Research)

**Category:** Architecture & Operations

**Published:** 3 August 2026

---

## Key Points
- Orchard is an open-source framework from Microsoft Research covering the full agent lifecycle: environments, training data, reinforcement learning, and evaluation.
- Its core component, Orchard Env, is a lightweight Kubernetes-based service that runs isolated agent environments at scale for data collection, RL, and evaluation.
- Agents are trained inside the real deployment harnesses they will run in (Codex, OpenClaw, ZeroClaw), removing the usual mismatch between training and production behaviour.
- Three reference agents demonstrate the framework: Orchard-SWE (69.7% on SWE-bench Verified, 73% with value-model reranking, at roughly 3B active parameters), Orchard-GUI (68.4% average across three web benchmarks with a 4B vision-language model), and Orchard-Claw (59.6% on Claw-Eval at three attempts).
- The results argue that small open-weight models can rival systems ten times larger when the training methodology and environment infrastructure are right.

---

## Summary
Microsoft Research has released Orchard, an open framework intended to remove a persistent bottleneck in agentic AI research: the strongest agentic systems are built on proprietary infrastructure that the wider community cannot access, reproduce, or extend. Orchard packages the pieces that normally stay behind closed doors, including environment orchestration, training data, training recipes, evaluation methods, and implementation details, and releases them for open use.

The foundation is Orchard Env, a lightweight Kubernetes-based environment service that provisions isolated execution spaces for collecting training data, running reinforcement learning, and performing evaluation. Its notable design decision is that agents are trained directly inside real deployment harnesses such as Codex, OpenClaw, and ZeroClaw rather than in simplified stand-ins, so behaviour learned in training carries over to deployment. On top of this sit several training techniques: credit-assignment supervised fine-tuning, which salvages the productive segments of failed attempts instead of discarding them; Balanced Adaptive Rollout, aimed at extracting signal from sparse rewards; dense reward methods including on-policy distillation from a stronger teacher and a process reward model that scores method rather than outcome; and a compact value model trained on past trajectories to rerank candidate solutions.

Three domain agents show the framework in practice. Orchard-SWE, trained with credit-assignment SFT on 107,000 distilled interactions, reaches 69.7% on SWE-bench Verified and 73% with value-model reranking, using approximately 3 billion active parameters. Orchard-GUI, a 4-billion-parameter vision-language model trained with minimal supervision, averages 68.4% across WebVoyager (74.1%), Online-Mind2Web (67.0%), and DeepShop (64.0%). Orchard-Claw, targeting personal productivity workflows, completes 59.6% of Claw-Eval tasks within three attempts, rising to 73.9% when paired with stronger agent systems. Together they support the paper's central claim: competitive real-world agent performance is achievable with far smaller open-weight models given the right training methodology and infrastructure.

---
**Captured:** 5 August 2026

**Link:** https://www.microsoft.com/en-us/research/blog/orchard-an-open-framework-for-scalable-agentic-ai/

**Key Words:** Agentic AI; Open Source; Reinforcement Learning; Agent Harness; Benchmarks
