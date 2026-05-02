---
layout: page
title: Chain-of-Thought Distillation
description: SFT vs. DPO/ORPO for reasoning alignment on Flan-T5-Base.
importance: 3
category: research
giscus_comments: false
---

**Role:** Developer · **Timeline:** Sep 2025 – Dec 2025

A study of **chain-of-thought distillation** for reasoning alignment, systematically comparing **supervised fine-tuning (SFT)** against **preference-based reinforcement learning** (DPO, ORPO) on instruction-tuned LLMs.

### Setup

- **Base model:** Flan-T5-Base (250M parameters)
- **Distillation data:** CoT Collection (1.8M reasoning samples)
- **Benchmarks:** GSM8K (math word problems) and StrategyQA (commonsense reasoning)

### Key result

Under limited compute, **ORPO yielded robust reasoning gains** that SFT and PPO did not match — pushing commonsense accuracy from **14.3% → 40.7%** on StrategyQA while avoiding the cold-start instability that plagues PPO at this model scale.

### Takeaway

Preference-based methods like ORPO are a strong drop-in alternative to PPO for small-model reasoning distillation when full RLHF infrastructure isn't available — the alignment-via-preferences signal is enough to teach the model to reason longer and more accurately.
