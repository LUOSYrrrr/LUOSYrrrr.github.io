---
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<!--
  Bilingual home page.
  - Content lives in two parallel blocks: .i18n-en and .i18n-zh.
  - The masthead toggle (top-right) switches which one is visible.
  - CSS/JS for the toggle is inlined in _includes/masthead.html.
  - Each block opens with <div ... markdown="1"> so kramdown still parses Markdown inside.
-->

<div class="i18n-en" markdown="1">

I'm a second-year Master's student at the [University of Melbourne](https://www.unimelb.edu.au), advised by Dr. Ting Dang. My research is on **class-incremental learning for audio** — how a model can absorb new sound classes over time without re-training from scratch or forgetting what it already knew.

I came into machine learning from a cybersecurity background at Sichuan University; that shaped how I think about systems — careful with assumptions, comfortable going low-level. I'm currently pushing toward **embodied AI**, aiming for an algorithm research internship in mid-2026. Along the way I've also shipped production AI / full-stack systems across two internships in Beijing.

## News

* **2026-04** &nbsp; Embodied AI Sprint is running. M0 environment (Isaac Sim 4.5.0, Isaac Lab 2.x, PyTorch 2.5.1 on CUDA 12.4) is up; next milestone is Franka Reach RL.
* **2026-03** &nbsp; Wrapped up AI-application internship at **KNQ Technology** — the table-tennis AI commentary system I built went live end-to-end.
* **2026-02** &nbsp; **NanoMemAgent** released — a modular agent framework with an L1–L5 layered memory stack.
* **2026-Q1** &nbsp; Audio-L3A feature-caching pipeline running on Melbourne's Spartan HPC (SLURM, A100).
* **2025-11** &nbsp; Finished **PocketLLM** — a 0.2B MoE decoder trained from scratch on a single GPU, aligned through SFT + DPO / PPO / GRPO.
* **2025-07** &nbsp; Finished full-stack internship at **SoundAI Technology** — iOS + Java backend for a headset real-time translation product.
* **2024-07** &nbsp; Started M.Sc. Software Engineering at the University of Melbourne.
* **2024-06** &nbsp; Graduated B.Eng. in Cyberspace Security from Sichuan University.

## Current research

**Audio-L3A — analytic class-incremental learning for audio.**
I'm adapting the L3A framework (analytic, RLS-style closed-form learning) from vision to audio CIL. The pipeline uses a frozen CNN14 (PANNs) backbone to cache 2049-dim bias-augmented features; a Weighted Analytic Classifier (WAC) accumulates `A` and `C` matrices and solves classification in closed form — no gradient descent, no rehearsal buffer. Evaluated on AudioSet (50 classes, 30 base + 5 per incremental step). Training runs on Melbourne's Spartan HPC.

_Paper and code — coming soon._

## Experience

**AI Application Engineer, Intern.** &nbsp; [KNQ Technology (麒纪科技), Beijing] &nbsp; _2026.01 – 2026.03_
<br/>
Built an end-to-end AI commentary system for table-tennis matches in Python + FastAPI: **video → OCR → LLM script generation → TTS → merged video**, with RTMP live-stream support. Designed pre-match narrative Agents that fuse player profiles and historical head-to-head data through incremental context injection; wrote a TTS pronunciation-correction module and real-time memory tracking to keep commentary coherent and non-repetitive. Kept an in-match action-recognition Agent interface decoupled from athlete-ID so the live decision loop can plug in later.

**Full-stack Engineer, Intern.** &nbsp; [SoundAI Technology (声智科技), Beijing] &nbsp; _2025.06 – 2025.07_
<br/>
Shipped iOS client + Java backend for a headset-based real-time translation product — closed the loop from **in-ear audio capture → live translation → in-app display**. Designed the membership-tier permission system gating real-time translation, transcription and history. Backend: Spring Boot + MySQL for auth, membership state and API gating; WebSocket for low-latency voice streaming and translation-result return.

## Education

**M.Sc. Software Engineering**, University of Melbourne &nbsp; _2024.07 – present_
<br/>Advisor: Dr. Ting Dang. Research in audio class-incremental learning.

**B.Eng. Cyberspace Security**, Sichuan University &nbsp; _2020.09 – 2024.06_

## Get in touch

Email <luosylois@gmail.com> &nbsp;·&nbsp; GitHub [@LUOSYrrrr](https://github.com/LUOSYrrrr) &nbsp;·&nbsp; [CV (PDF)](/resume.pdf)

</div>

<div class="i18n-zh" markdown="1">

我是[墨尔本大学](https://www.unimelb.edu.au)软件工程硕士二年级学生，导师是 Dr. Ting Dang。研究方向是**音频的类增量学习**——让模型随时间吸收新的声音类别，既不用从头训练、也不遗忘已经学过的旧类。

我本科在四川大学读网络空间安全，这段经历让我习惯**从系统视角看问题**：对假设保持谨慎，愿意往底层钻。目前我正把研究重心推向**具身智能（embodied AI）**，目标是 2026 年中的算法研究实习。研究之外，我也在北京做过两段偏工程的实习——把 AI 能力落地成产品。

## 近况

* **2026-04** &nbsp; 具身智能 Sprint 启动。M0 环境（Isaac Sim 4.5.0、Isaac Lab 2.x、PyTorch 2.5.1 + CUDA 12.4）已跑通，下一里程碑是 Franka Reach RL。
* **2026-03** &nbsp; 在 **麒纪科技** 的 AI 应用开发实习结束——乒乓球赛事 AI 解说系统端到端跑通。
* **2026-02** &nbsp; **NanoMemAgent** 上线——模块化 Agent 执行框架，内置 L1–L5 分层记忆栈。
* **2026-Q1** &nbsp; Audio-L3A 特征缓存流水线在墨大 Spartan HPC（SLURM、A100）上运行。
* **2025-11** &nbsp; 完成 **PocketLLM**——单卡从零训练的 0.2B MoE Decoder 模型，走完 SFT + DPO / PPO / GRPO 全链路。
* **2025-07** &nbsp; **声智科技** 全栈开发实习结束——耳机端实时翻译产品的 iOS 客户端 + Java 后端。
* **2024-07** &nbsp; 入学墨尔本大学软件工程硕士。
* **2024-06** &nbsp; 四川大学网络空间安全学士毕业。

## 正在做的研究

**Audio-L3A —— 音频场景下的解析式类增量学习。**
我在把 L3A 框架（解析式、RLS 闭式解）从视觉迁移到音频 CIL。Pipeline 用 frozen CNN14（PANNs）backbone 缓存 2049 维带偏置增广的特征；加权解析分类器（WAC）累积 `A`、`C` 矩阵做闭式解——不走梯度下降，也不依赖重放缓冲。数据集是 AudioSet（50 类，30 基类 + 每阶段 5 类），训练跑在墨大 Spartan HPC 上。

_论文和代码将陆续公开。_

## 实习经历

**AI 应用开发工程师（实习）。** &nbsp; 北京麒纪科技有限公司 &nbsp; _2026.01 – 2026.03_
<br/>
用 Python + FastAPI 从零搭了一个乒乓球赛事 AI 解说系统，打通 **视频输入 → OCR 识别 → LLM 生成 → TTS 合成 → 视频融合**，支持 RTMP 直播流实时处理。设计了预赛备稿 Agent——融合球员档案、历史交手数据，用增量上下文融合机制把备稿注入解说生成；写了 TTS 读音修正模块和实时记忆追踪，保证解说连贯无重复。还预留了赛中动作识别 Agent 接口，与运动员识别模块解耦，方便后续接入直播实时决策。

**全栈开发工程师（实习）。** &nbsp; 北京声智科技有限公司 &nbsp; _2025.06 – 2025.07_
<br/>
负责 iOS 客户端 + Java 后端的核心功能开发，打通 **耳机语音采集 → 实时翻译 → App 展示** 的完整链路。设计并实现了会员等级与权限体系，控制实时翻译、语音转写、历史记录等能力按会员等级动态开放。后端基于 Spring Boot + MySQL 做用户身份、会员状态与 API 鉴权，支撑高频语音请求；WebSocket 实时语音服务负责语音流的低延迟传输与翻译结果回传。

## 教育背景

**墨尔本大学，软件工程硕士** &nbsp; _2024.07 – 至今_
<br/>导师：Dr. Ting Dang。研究方向：音频类增量学习。

**四川大学，网络空间安全学士** &nbsp; _2020.09 – 2024.06_

## 联系方式

邮箱 <luosylois@gmail.com> &nbsp;·&nbsp; GitHub [@LUOSYrrrr](https://github.com/LUOSYrrrr) &nbsp;·&nbsp; [简历（PDF）](/resume.pdf)

</div>
