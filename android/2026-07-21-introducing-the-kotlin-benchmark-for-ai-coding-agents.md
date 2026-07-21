# JetBrains 发布 Kotlin Benchmark：评估 AI 编程 Agent 的官方基准

> 原文：[Introducing the Kotlin Benchmark for AI Coding Agents](https://blog.jetbrains.com/kotlin/2026/07/introducing-the-kotlin-benchmark-evaluate-ai-coding-agents-on-real-world-kotlin-tasks/) | 日期：2026-07-21

JetBrains 正式发布了 Kotlin Benchmark，这是评估 AI 编程 Agent 在 Kotlin 软件工程任务上表现的官方基准。

对于 Kotlin 团队来说，最重要的问题是 AI Agent 能否可靠地完成端到端的 Kotlin 任务——从阅读 issue 到生成通过验证的解决方案。Kotlin Benchmark 旨在填补这一空白。

**基准测试详情：**
- 基于 SWE-bench 方法论，聚焦仓库级别的 Kotlin 软件工程任务
- 数据集包含 105 个工程任务，来自活跃的开源仓库
- 每个任务要求 AI Agent 解读真实 issue 描述、导航项目上下文、生成功能性补丁
- 解决方案在容器化环境中严格验证，只有通过测试才算"已解决"

**与现有基准的区别：**
Kotlin 已有 Kotlin_HumanEval 和 Kotlin_QA 等模型评估资产，用于衡量模型对语言语法和核心概念的理解。Kotlin Benchmark 则着眼于不同层面：AI 编程 Agent 在现有 Kotlin 项目中完成经过验证的软件工程任务的能力。

JetBrains 已在 GitHub 上发布了基准资产，并推出了官方排行榜来追踪评估结果。