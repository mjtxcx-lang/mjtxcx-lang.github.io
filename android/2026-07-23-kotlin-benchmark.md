# JetBrains 发布 Kotlin 基准测试：评估 AI 编程 Agent 的真实 Kotlin 能力

> 原文：[Introducing the Kotlin Benchmark for AI Coding Agents](https://blog.jetbrains.com/kotlin/2026/07/introducing-the-kotlin-benchmark-evaluate-ai-coding-agents-on-real-world-kotlin-tasks/) | 日期：2026-07-23

JetBrains 正式发布了 Kotlin Benchmark——首个官方 AI 编程 Agent 的 Kotlin 软件工程基准测试。该基准基于 SWE-bench 方法论，包含 105 个来自活跃开源仓库的真实工程任务，每个任务要求 Agent 解读 issue 描述、理解项目上下文并生成可通过容器化测试验证的功能补丁。首轮评估结果显示：Claude Code（Opus 4.7 xhigh）以 85.71%（90/105）的解决率位居榜首；JetBrains 自家的 Junie（Opus 4.7 max）和 Codex（GPT 5.5 xhigh）均为 81.9% 紧随其后。与侧重语法理解的 Kotlin_HumanEval 等模型基准不同，该基准关注的是端到端软件工程能力。JetBrains 强调分数仅供参考，实际表现取决于项目架构、内部 API 和编码规范等因素。基准数据集和测试框架已在 GitHub 开源，官方排行榜可在 kotlinlang.org/benchmark 查看，后续将持续扩展任务覆盖范围。