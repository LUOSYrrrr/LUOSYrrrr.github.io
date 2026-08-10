---
title: "Whole-Body WAM - Unitree G1 loco-manipulation"
excerpt: "<span class='i18n-en'>Extending FastWAM from tabletop manipulation to 72-D whole-body physical action prediction on Unitree G1 + Wuji hands.</span><span class='i18n-zh'>将 FastWAM 从桌面机械臂任务扩展到 Unitree G1 + Wuji 的 72 维全身物理动作预测。</span>"
collection: portfolio
---

_FastWAM · Wan2.2-TI2V-5B · Video DiT + Action DiT · DeepSpeed · Unitree G1 · Wuji · **2026.05 - 2026.08**_

<div class="i18n-en" markdown="1">

Algorithm internship project extending **FastWAM**, originally evaluated on
tabletop manipulation, to whole-body loco-manipulation on **Unitree G1** with
Wuji dexterous hands.

**Model adaptation.** &nbsp; Worked with a Mixture-of-Transformers design built on
Wan2.2-TI2V-5B: a video expert and action expert share cross-attention while the
action head predicts a continuous **72-D physical action** - 29 body joints,
3 root angular-velocity dimensions, and 20 joints per hand.

**Objective and mixed supervision.** &nbsp; Supported joint video-action flow
matching across full video + body-action data, video-only demonstrations, and
body-only motion trajectories. Dataset-level masks prevent absent modalities
and padded dimensions from becoming false supervision.

**Distributed training and data.** &nbsp; Used Accelerate, DeepSpeed ZeRO-2, NCCL,
and bf16 for multi-node training. Unified human motion, egocentric video, and
heterogeneous robot actions through retargeting, dimension completion, and
valid-dimension masks.

**Teleoperation and quality control.** &nbsp; Built a Pico VR + Trackers + MANUS
collection pipeline and data checks for action discontinuities, state-action
alignment, numeric extremes, and video quality. I also built the public
[WB-WAM Data Reviewer](https://github.com/LUOSYrrrr/WB_WAM_Data_Viewer), a
Kubernetes-hosted remote review workbench with append-only annotations.

</div>

<div class="i18n-zh" markdown="1">

算法实习项目：将原本面向桌面机械臂任务的 **FastWAM** 扩展到 **Unitree G1** + Wuji 灵巧手的全身移动操作。

**模型扩展。** &nbsp; 基于 Wan2.2-TI2V-5B 的 Mixture-of-Transformers 架构，Video Expert 与 Action Expert 共享 cross-attention；动作头直接预测 **72 维连续物理动作**：29 维身体关节、3 维 root 角速度、双手各 20 维关节。

**训练目标与混合监督。** &nbsp; 在完整视频 + 全身动作、纯视频示范、无视频身体运动轨迹之间进行联合 Flow Matching 训练；通过 dataset-level mask 避免把缺失模态和补零维度当作真实监督。

**分布式训练与数据统一。** &nbsp; 使用 Accelerate、DeepSpeed ZeRO-2、NCCL 和 bf16 做多节点训练；通过动作重定向、维度补齐和有效维度掩码，统一人体运动、第一视角视频与不同机器人动作。

**遥操作与数据质检。** &nbsp; 搭建 Pico VR + Trackers + MANUS 采集链路，并实现动作突变、state-action 对齐、数值极值与视频质量检查。另开发公开的 [WB-WAM Data Reviewer](https://github.com/LUOSYrrrr/WB_WAM_Data_Viewer)：部署在 Kubernetes 上的远程审核工作台，审核结果 append-only 保存。

</div>
