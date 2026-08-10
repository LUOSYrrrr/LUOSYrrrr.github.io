---
title: "Audio-L3A - efficient audio class-incremental learning"
excerpt: "<span class='i18n-en'>A frozen-backbone analytic learner reaching 45.16% mAP on five-phase AudioSet-50, 2.65 points above LwF at roughly one-ninth of offline training time.</span><span class='i18n-zh'>冻结 backbone 的解析式持续学习方法：AudioSet-50 五阶段达到 45.16% mAP，领先 LwF 2.65 个百分点，总训练时间约为离线上界的 1/9。</span>"
collection: portfolio
---

_Audio CIL · PyTorch · CNN14 / PANNs · scikit-learn · SLURM · **2026.02 - 2026.05**_

<div class="i18n-en" markdown="1">

An efficient multi-label audio class-incremental learner combining a frozen
backbone, a Ridge closed-form Weighted Analytic Classifier, frequency weighting,
and per-class threshold calibration.

**Results.** &nbsp; Reached **45.16% mAP** on five-phase AudioSet-50, outperforming
the strongest CIL baseline, LwF, by **2.65 points** and finishing only **0.71
points** below the offline joint-training upper bound. After phase 0, the model
requires no backpropagation; total training time is approximately **1/9** of the
offline upper-bound run.

**Calibration.** &nbsp; Diagnosed why raw Ridge scores produced weak F1@0.5.
Per-class Platt scaling raised F1 from 27.51% to 38.93%; sigmoid plus learned
per-class thresholds aligned calibration with the F1 objective and reached
**45.33% F1** across five random seeds.

**Ablations and baselines.** &nbsp; Implemented FT, EWC, SI, LwF, and CIL-ML-KD
across CNN14 and TCResNet-8. Isolated the effects of frequency weighting,
embedding dimension, and threshold calibration; mAP standard deviation across
five class orders was only 0.10.

**HPC engineering.** &nbsp; Reduced a TCResNet-8 baseline from 24 hours to 20
minutes with MFCC feature caching and automated more than 80 experiments across
GPU and CPU SLURM partitions.

_Paper and code are currently private while the thesis is in progress._

</div>

<div class="i18n-zh" markdown="1">

面向多标签音频类增量学习，结合冻结 backbone、Ridge 闭式解加权解析分类器、频率加权和 per-class threshold 校准。

**核心结果。** &nbsp; 在五阶段 AudioSet-50 上达到 **45.16% mAP**，比最强 CIL 基线 LwF 高 **2.65 个百分点**，距离离线联合训练上界仅 **0.71 个百分点**。Phase 0 后无需反向传播，总训练时间约为离线上界的 **1/9**。

**校准。** &nbsp; 定位 Ridge raw score 导致 F1@0.5 偏低的问题。Per-class Platt Scaling 将 F1 从 27.51% 提升至 38.93%；进一步采用 sigmoid + 每类独立学习阈值，使五个随机种子下的 F1 达到 **45.33%**。

**消融与基线。** &nbsp; 在 CNN14 与 TCResNet-8 上实现 FT、EWC、SI、LwF、CIL-ML-KD 五种基线，量化频率加权、embedding 维度和阈值校准的贡献；五种类别顺序下 mAP 标准差仅 0.10。

**HPC 工程。** &nbsp; 使用 MFCC 磁盘缓存将 TCResNet-8 baseline 从 24 小时降到 20 分钟，并通过 SLURM GPU / CPU 多分区自动编排 80 余组实验。

_论文与代码在毕业论文完成前暂不公开。_

</div>
