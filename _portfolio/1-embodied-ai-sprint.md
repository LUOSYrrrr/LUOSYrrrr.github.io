---
title: "Embodied AI Sprint"
excerpt: "<span class='i18n-en'>Eight-week self-paced sprint toward a summer-2026 embodied-AI internship. Stack: π₀ (VLA) + Isaac Lab + LeRobot + ROS 2 + SO-101 arm.</span><span class='i18n-zh'>为 2026 年夏天具身智能实习准备的八周冲刺。技术栈：π₀ (VLA) + Isaac Lab + LeRobot + ROS 2 + SO-101 机械臂。</span>"
collection: portfolio
---

<div class="i18n-en" markdown="1">

Self-imposed eight-week sprint toward a summer-2026 research internship in embodied AI.
The stack pairs a **π₀ VLA model** with **Isaac Lab** for sim, **LeRobot** for data and
training, and **ROS 2** on an **SO-101** arm for real-robot work.

**Milestone M0 — environment.** &nbsp; Done. Isaac Sim 4.5.0, Isaac Lab 2.x, PyTorch 2.5.1
on CUDA 12.4, running on a workstation with an RTX 4070 Ti Super (16GB). Apptainer
containers for HPC portability.

**Milestone M1 — Franka Reach RL.** &nbsp; In progress. Baseline PPO / SAC on Isaac Lab's
`Franka-Reach` task as a sanity check before touching manipulation.

**Later milestones.** &nbsp; π₀ fine-tune on LeRobot datasets · sim-to-real on the SO-101 ·
a minimal language-conditioned pick task.

Code and weekly logs at [github.com/LUOSYrrrr/EMBODIED-AI](https://github.com/LUOSYrrrr/EMBODIED-AI).

</div>

<div class="i18n-zh" markdown="1">

为 2026 年夏季具身智能研究实习准备的八周冲刺。技术栈：**π₀ VLA 模型** 做策略，**Isaac Lab** 做仿真，**LeRobot** 做数据和训练，真机用 **ROS 2** 驱动 **SO-101** 机械臂。

**M0 —— 环境。** &nbsp; 已完成。Isaac Sim 4.5.0、Isaac Lab 2.x、PyTorch 2.5.1 + CUDA 12.4，跑在 RTX 4070 Ti Super 16GB 工作站上；用 Apptainer 容器保证能迁到 HPC。

**M1 —— Franka Reach RL。** &nbsp; 进行中。在 Isaac Lab 的 `Franka-Reach` 任务上跑 PPO / SAC 基线，作为接入 manipulation 前的 sanity check。

**后续里程碑。** &nbsp; 在 LeRobot 数据集上 fine-tune π₀ · SO-101 上做 sim-to-real · 一个最小的语言条件抓取任务。

代码和每周进度记录见 [github.com/LUOSYrrrr/EMBODIED-AI](https://github.com/LUOSYrrrr/EMBODIED-AI)。

</div>
