---
title: "π₀.₅ on Franka - flexible manipulation"
excerpt: "<span class='i18n-en'>An end-to-end OpenPI adaptation for Franka: DROID-style demonstrations, LeRobot v2 data, 8×A100 full fine-tuning, WebSocket policy serving, and real-robot execution.</span><span class='i18n-zh'>面向 Franka 的 OpenPI 全链路适配：DROID 风格示范、LeRobot v2 数据、8×A100 全量微调、WebSocket 策略服务与真机执行。</span>"
collection: portfolio
redirect_from:
  - /portfolio/1-embodied-ai-sprint/
---

_OpenPI · JAX / PyTorch · Flow Matching · LeRobot · DROID · Franka · **2026.01 - 2026.04**_

<div class="i18n-en" markdown="1">

An end-to-end adaptation of **π₀.₅ (OpenPI)** for flexible factory manipulation,
including part sorting, bin placement, and dynamic grasping under randomized
object poses. The goal was to improve generalization beyond an earlier
Diffusion Policy baseline.

**Training-to-deployment pipeline.** &nbsp; Built the path from raw demonstrations
to execution: trajectory cleaning, forward-kinematics conversion from joint
angles to end-effector Cartesian poses, LeRobot v2 packaging, transform-field
mapping, normalization statistics, dataset and policy adaptation, full
fine-tuning, inference configuration, and evaluation clients.

**Demonstration data.** &nbsp; Configured DROID-style Franka teleoperation,
multi-view cameras, and task management. Collected and quality-checked 100
demonstrations per task for dynamic grasping, part sorting, and feeding tasks.

**Training and serving.** &nbsp; Ran full fine-tuning on **8×A100 GPUs**. Served the
policy over WebSocket and deployed inference on an **RTX 5090 Laptop**
workstation, closing the observation → action chunk → Franka execution loop.

**Regression and model understanding.** &nbsp; Used LIBERO as a regression test for
pipeline changes. Documented the π₀ / π₀.₅ MoT architecture, training forward,
prefill + Euler decoding, block-wise causal masks, state discretization, and
the seven-layer OpenPI data-transform pipeline.

Public technical notes are available in my
[annotated OpenPI fork](https://github.com/LUOSYrrrr/openpi).

</div>

<div class="i18n-zh" markdown="1">

面向工厂柔性分拣场景，将 **π₀.₅（OpenPI）** 适配到 Franka 机械臂，覆盖零件分类入盒、动态抓取与供件等任务，目标是改善原 Diffusion Policy 方案在多品类物体随机位姿下的泛化能力。

**训练到部署全链路。** &nbsp; 打通原始示范清洗、正运动学转换（关节角 → 末端笛卡尔位姿）、LeRobot v2 打包、Transform 字段映射、归一化统计量、Dataset / Policy 适配、全量微调、推理配置和评测客户端。

**示范数据。** &nbsp; 参照 DROID 配置 Franka 遥操作、多视角相机与任务管理流程；围绕动态抓取、零件分类入盒和供件任务，每个任务采集并质检 100 条示范轨迹。

**训练与策略服务。** &nbsp; 在 **8×A100** 上完成全量微调；通过 WebSocket 封装策略服务，在 **RTX 5090 Laptop** 工作站部署推理，闭环完成机器人观测读取、action chunk 推理和 Franka 真机执行。

**回归测试与原理沉淀。** &nbsp; 用 LIBERO 验证代码改动；系统梳理 π₀ / π₀.₅ 的 MoT 架构、训练 forward、prefill + Euler decode、block-wise causal mask、state 离散化，以及 OpenPI 七层数据 transform。

公开技术笔记见我的 [OpenPI 注释分支](https://github.com/LUOSYrrrr/openpi)。

</div>
