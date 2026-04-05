# TurboQuant: Online Vector Quantization with Near-optimal Distortion Rate
**Authors:** Amir Zandieh; Majid Daliri; Majid Hadian; Vahab Mirrokni

**Category:** Technical Fundamentals

**Published:** 28 April 2025

---

## Key Points
- TurboQuant achieves near-optimal distortion rates for both MSE and inner product quantization across all bit-widths and dimensions, differing from theoretical lower bounds by only a constant factor of approximately 2.7x.
- The method is data-oblivious and suitable for online applications, requiring no prior knowledge of the data distribution.
- A two-stage approach combines an MSE quantizer with a 1-bit Quantized Johnson-Lindenstrauss (QJL) transform on the residual to produce unbiased inner product estimates.
- For KV cache quantization in LLMs, TurboQuant achieves quality neutrality at 3.5 bits per channel and only marginal degradation at 2.5 bits per channel.
- In nearest neighbour search tasks, the method outperforms existing product quantization techniques in recall while reducing indexing time to virtually zero.

---

## Summary
TurboQuant addresses the fundamental problem of vector quantization — compressing high-dimensional vectors while preserving their geometric structure — rooted in Shannon's source coding theory. Existing methods fail to achieve optimal distortion rates for both mean-squared error (MSE) and inner product preservation simultaneously. TurboQuant overcomes this by randomly rotating input vectors to induce a concentrated Beta distribution on coordinates, then exploiting the near-independence property of distinct coordinates in high dimensions to apply optimal scalar quantizers per coordinate.

A key insight of the paper is that MSE-optimal quantizers introduce bias in inner product estimation. To address this, the authors propose a two-stage approach: first applying an MSE quantizer, then applying a 1-bit Quantized Johnson-Lindenstrauss (QJL) transform on the residual. This yields an unbiased inner product quantizer. The paper also provides formal information-theoretic lower bounds on the best achievable distortion rate by any vector quantizer, demonstrating that TurboQuant closely approaches these theoretical limits.

Experimental validation confirms the theoretical results across two practical applications. For KV cache quantization in large language models, TurboQuant achieves absolute quality neutrality at 3.5 bits per channel — a significant improvement over prior methods — and only marginal quality degradation at 2.5 bits per channel. For nearest neighbour search, the method surpasses existing product quantization techniques in recall accuracy while effectively eliminating indexing time, making it highly practical for real-time applications.

---
**Captured:** 2026-04-05

**Link:** https://arxiv.org/abs/2504.19874

**Key Words:** Vector Quantization; KV Cache; Distortion Rate; Inner Product Estimation; Nearest Neighbour Search
