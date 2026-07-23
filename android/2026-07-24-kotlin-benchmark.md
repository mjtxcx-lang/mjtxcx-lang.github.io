# JetBrains发布Kotlin AI编程基准测试：Claude Code以85.71%居首

> 原文：[Introducing the Kotlin Benchmark for AI Coding Agents](https://blog.jetbrains.com/kotlin/2026/07/introducing-the-kotlin-benchmark-evaluate-ai-coding-agents-on-real-world-kotlin-tasks/) | 日期：2026-07-24

JetBrains正式发布Kotlin Benchmark，这是首个专门评估AI编程Agent在Kotlin软件工程任务上表现的官方基准测试。该基准基于SWE-bench方法论，包含105个来自活跃开源仓库的真实工程任务，每个任务要求AI Agent解读真实issue描述、理解项目上下文并生成功能性补丁，方案在容器化环境中严格验证后才算通过。首批评估结果：Claude Code搭配Opus 4.7 xhigh以85.71%（90/105任务）的解决率位居榜首，JetBrains Junie搭配Opus 4.7 max（81.9%）和Codex搭配GPT 5.5 xhigh（81.9%）紧随其后。JetBrains强调基准分数是参考信号而非绝对保证，实际表现取决于代码库架构、内部API和编码标准。基准基于开源Multi-SWE-bench基础设施构建，所有数据集和测试工具均已公开，后续将扩展更多Kotlin场景。
