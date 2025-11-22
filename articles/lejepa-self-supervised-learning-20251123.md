# LeJEPA: Provable and Scalable Self-Supervised Learning Without the Heuristics
**Authors:** Randall Balestriero, Yann LeCun

**Published:** 11 November 2025

---

## Key Points
- Introduces LeJEPA, a theoretically grounded training objective for Joint-Embedding Predictive Architectures (JEPAs) that eliminates ad-hoc heuristics.
- Identifies isotropic Gaussian as the optimal distribution for JEPA embeddings to minimise downstream prediction risk.
- Presents Sketched Isotropic Gaussian Regularisation (SIGReg), a novel objective that constrains embeddings to the ideal distribution.
- Demonstrates stability across hyperparameters, architectures (ResNets, ViTs, ConvNets), and domains with only a single trade-off hyperparameter.
- Achieves 79% accuracy on ImageNet-1k linear evaluation with ViT-H/14, using only approximately 50 lines of code for implementation.

---

## Summary
This paper presents LeJEPA, a theoretically grounded approach to Joint-Embedding Predictive Architectures (JEPAs) for self-supervised learning. The authors address the lack of practical guidance and theoretical foundation in existing JEPA implementations, which has led to ad-hoc research and development. They identify that JEPA embeddings should follow an isotropic Gaussian distribution to minimise downstream prediction risk, and introduce Sketched Isotropic Gaussian Regularisation (SIGReg) as a novel objective to achieve this distribution.

LeJEPA combines the traditional JEPA predictive loss with SIGReg, resulting in a method with significant practical advantages: it requires only a single trade-off hyperparameter, has linear time and memory complexity, and demonstrates stability across various hyperparameters, architectures (including ResNets, ViTs, and ConvNets), and domains. Importantly, LeJEPA eliminates common heuristics such as stop-gradient, teacher-student frameworks, and hyperparameter schedulers, while being friendly to distributed training with only approximately 50 lines of code required.

The empirical validation is extensive, covering over 10 datasets and 60+ architectures across varying scales and domains. When pretrained on ImageNet-1k and evaluated with linear probing using a frozen backbone, LeJEPA achieves 79% accuracy with a ViT-H/14 architecture. The authors aim to re-establish self-supervised pretraining as a fundamental pillar of AI research through this simplified and theory-friendly approach.

---
**Captured:** 23 November 2025

**Link:** https://arxiv.org/abs/2511.08544

**Key Words:** Self-supervised Learning; JEPA; Representation Learning; Deep Learning; Computer Vision
