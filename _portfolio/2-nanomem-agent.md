---
title: "NanoMemAgent — modular agent framework with layered memory"
excerpt: "<span class='i18n-en'>A modular agent runtime with a ReAct loop, plug-in skills, MCP tool ecosystem, and an L1–L5 memory stack (vector + BM25 + knowledge graph).</span><span class='i18n-zh'>模块化 Agent 执行框架：ReAct 推理循环、插件化 Skill、MCP 工具生态，以及 L1–L5 分层记忆栈（向量 + BM25 + 知识图谱）。</span>"
collection: portfolio
---

_Python · ReAct · Skill / Tool / MCP · ChromaDB · Neo4j · BGE-M3 · BM25 · ThreadPool · **2026.02 – 2026.03**_

<div class="i18n-en" markdown="1">

A modular agent execution framework built from scratch: a ReAct reasoning loop,
dynamic tool calls, MCP integration, a layered memory system (short-term vector
store + long-term knowledge graph), and a plug-in Skill mechanism. Supports
multi-model switching; already wired into Feishu.

**Agent Loop engine.** &nbsp; The core module coordinates message routing →
`ContextBuilder` (system prompt + memory + skills) → LLM inference → tool-call
execution → feedback, with max-iteration guards and chained tool calls.

**Layered memory (L1–L5).** &nbsp; Storage / embedding / retrieval / knowledge /
application. Dual-track storage: **Operational Memory** (dynamic CRUD) + **RAG
Knowledge Base**. Retrieval runs **vector + BM25 + graph** in parallel, fused
with RRF ranking.

**Tool ecosystem.** &nbsp; A standardized **MCP Client** lets filesystem / DB /
search tools plug in with no framework changes. Built-ins: cron scheduling,
background subagents, heartbeat health checks. A single `LLMProvider`
interface swaps OpenAI / Anthropic / local models with zero call-site changes.

</div>

<div class="i18n-zh" markdown="1">

从零实现的模块化 Agent 执行框架。内置 ReAct 推理循环、动态 tool 调用与 MCP 接入、分层记忆系统（短期向量存储 + 长期知识图谱）、插件化 Skill 机制，支持多模型切换，并已接入飞书。

**Agent Loop 核心引擎。** &nbsp; 协调 消息路由 → `ContextBuilder`（系统提示 + 记忆 + 技能）→ LLM 推理 → Tool Calls 执行 → 结果反馈 的完整循环，支持最大迭代次数保护与工具链式调用。

**分层记忆系统（L1–L5）。** &nbsp; 存储 / 嵌入 / 检索 / 知识 / 应用 五层架构；**Operational Memory**（动态 CRUD）与 **RAG Knowledge Base** 双轨存储；**Vector + BM25 + Graph** 三路并行检索 + RRF 融合排序。

**模块化工具生态。** &nbsp; 标准化 **MCP Client** 支持文件系统、数据库、搜索等外部工具动态接入；内置 Cron 定时任务、子代理（Subagent）后台执行、Heartbeat 健康检测；抽象 `LLMProvider` 接口层统一封装 OpenAI、Anthropic、本地模型等，零代码切换。

</div>
