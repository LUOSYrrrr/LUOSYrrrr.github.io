---
title: "PocketLLM — 0.2B LLM trained from scratch, full pipeline"
excerpt: "<span class='i18n-en'>A 0.2B-parameter MoE decoder-only model built end-to-end on a single GPU: pretraining + SFT + DPO / PPO / GRPO alignment. Benchmarked on C-Eval and CMMLU.</span><span class='i18n-zh'>单卡从零训练的 0.2B 参数 MoE Decoder-only 模型：预训练 + SFT + DPO / PPO / GRPO 对齐全链路。在 C-Eval、CMMLU 上评测。</span>"
collection: portfolio
---

_PyTorch · Transformers · MoE · SFT · LoRA · DPO · GRPO · Flash Attention · **2025.09 – 2025.11**_

<div class="i18n-en" markdown="1">

Built a 0.2B-parameter language model end-to-end on a single consumer GPU — a
testbed for everything that happens after "attention is all you need":
pretraining, supervised fine-tuning, and multiple preference-alignment algorithms.

**Full training pipeline.** &nbsp; Decoder-only MoE core at 512 hidden dim.
Pretraining → LoRA-based SFT → preference alignment covering DPO / PPO / GRPO,
all from scratch.

**Data engineering.** &nbsp; Pretraining on cleaned MNBVC corpus. For SFT, built
a short-text (<512 char) instruction dataset from COIG with rule-based noise
removal to improve instruction following.

**Evaluation.** &nbsp; ~25% accuracy on C-Eval and CMMLU — on par with
same-scale baselines under a tight compute budget.

</div>

<div class="i18n-zh" markdown="1">

在单卡算力下，从零训练一个 0.2B 参数规模的极小语言模型——把 "attention is all you need" 之后的所有环节跑一遍：预训练、SFT、以及几种偏好对齐算法。

**全链路训练。** &nbsp; 独立开发结合 MoE 的 Decoder-only 核心架构（512 维度）。完整实现了预训练、基于 LoRA 的高效指令微调（SFT），以及涵盖 DPO / PPO / GRPO 的偏好对齐训练全流程。

**数据工程。** &nbsp; 预训练使用清洗后的 MNBVC 语料；SFT 阶段利用 COIG 构建高质量短文本（<512 字符）数据集，设计规则消除噪声，显著提升指令遵循能力。

**基准评测。** &nbsp; 在 C-Eval、CMMLU 等中文基准测试中，该 0.2B 模型在有限算力下取得了约 25% 的准确率，与同量级基线相当。

</div>
