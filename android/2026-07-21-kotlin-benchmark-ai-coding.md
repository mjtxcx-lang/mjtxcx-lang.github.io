# JetBrains 发布 Kotlin 基准测试：Claude Code 以 85.71% 解决率领跑

> 原文：[Introducing the Kotlin Benchmark for AI Coding Agents](https://blog.jetbrains.com/kotlin/2026/07/introducing-the-kotlin-benchmark-evaluate-ai-coding-agents-on-real-world-kotlin-tasks/) | 日期：2026-07-22

JetBrains 发布了官方 Kotlin 基准测试（Kotlin Benchmark），用于评估 AI 编码代理在真实 Kotlin 软件工程任务上的表现。该基准测试基于 SWE-bench 方法，包含 105 个来自活跃开源仓库的工程任务，AI 代理需要解读真实 issue、理解项目上下文、生成可用补丁，并在容器化环境中严格验证。首轮评测中，Claude Code（Opus 4.7 xhigh）以 85.71% 的解决率（90/105）排名第一，JetBrains Junie（Opus 4.7 max）和 Codex（GPT 5.5 xhigh）均以 81.9% 紧随其后。JetBrains 计划持续扩展任务覆盖范围，包括 Android、KMP 和 Compose Multiplatform 等领域。
