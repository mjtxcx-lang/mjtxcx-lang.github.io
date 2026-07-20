# Introducing the Kotlin Benchmark for AI Coding Agents

**来源:** [https://blog.jetbrains.com/kotlin/2026/07/introducing-the-kotlin-benchmark-evaluate-ai-coding-agents-on-real-world-kotlin-tasks/](https://blog.jetbrains.com/kotlin/2026/07/introducing-the-kotlin-benchmark-evaluate-ai-coding-agents-on-real-world-kotlin-tasks/)

**日期:** 2026-07-21

## 中文概述

JetBrains发布Kotlin AI编程基准测试，评估AI编码能力

---

## 原文摘录

A concise multiplatform language developed by JetBrains
Visit the Kotlin Site
Introducing the Kotlin Benchmark for AI Coding Agents
Agentic coding benchmarks are getting closer to real-world software development. For Kotlin teams, the most important question is how reliably AI agents can complete end-to-end Kotlin tasks, from reading an issue to producing a solution that passes validation.
We’re taking the first step in addressing that gap by releasing the
, JetBrains’ official benchmark for evaluating AI coding agents on Kotlin software engineering tasks. Our goal is to give developers a credible, public way to assess how different agents perform on Kotlin and compare agent setups using tasks that are closer to day-to-day dev work.
Alongside the benchmark release, we’re publishing the benchmark assets on GitHub and launching the official leaderboard to track the evaluation results.
Explore the benchmark on GitHub
See the first results on the leaderboard
How the Kotlin Benchmark works
The first public iteration of the Kotlin Benchmark is based on the SWE-bench methodology and focuses on repository-level Kotlin software engineering tasks.
Kotlin already has strong model-focused evaluation assets, including
, which help measure a model’s understanding of the language’s syntax and core concepts. The Kotlin Benchmark looks at a different layer: how well an AI coding agent can complete validated software engineering tasks in existing Kotlin projects.
The dataset features 105 engineering tasks sourced from active open-source repositories. Each task requires the AI agent to interpret a real issue description, navigate the project’s context, and generate a functional patch. Solutions are strictly verified in containerized environments, and a task is only marked as resolved when the generated solution passes the required test verification.
You can read more about our environment setup and data collection on the
The first evaluations show that leading coding agents can complete a large share of the current Kotlin Benchmark tasks. These results reflect the first public iteration of the benchmark and do not yet include the most recent model releases. We are already working on the second iteration and will update the leaderboard as newer evaluations are added.
In this run, the top result came from Claude Code with Opus 4.7 xhigh, which resolved 90 of 105 tasks, an 85.71% resolution rate. JetBrains Junie with Opus 4.7 max (81.9%) and Codex with GPT 5.5 xhigh (81.9%) followed closely.
The full leaderboard is available on
kotlinlang.org/benchmark
, where you can compare agents and configurations in detail.
Results shown here reflect the first public iteration of the Kotlin Benchmark. The leaderboard will be updated as newer model evaluations are added.
For teams evaluating coding agents, the benchmark provides a shared frame of reference for comparing setups on Kotlin tasks instead of relying only on vendor claims. The scores are intended as a signal, not a guarantee for every codebase. Real-world results depend on your architecture, internal APIs, coding standards, tooling, and validation process.
We value an open approach, which is why we built this benchmark on the open-source Multi-SWE-bench infrastructure and made all datasets and test harnesses publicly available.
We treat benchmarks as a continuous quality measurement pipeline. Moving forward, we plan to expand the framework in these areas:
Broader Kotlin ecosystem coverage:
We want the task mix to better reflect how Kotlin is used in practice, including areas such as Android and Kotlin Multiplatform, and cover a wider range of task difficulty levels.
More evaluation metrics:
Passing tests is a useful correctness signal, but it is only one part of agent evaluation. Future iterations will look at  cost, performance, maintainability, and code quality.
More agents and model setups:
We plan to evaluate more commercial agents, agent-model configurations, and open-weight models, so teams can compare a wider range of setups.
The benchmark is open, so you can inspect the tasks, compare results, and tell us which Kotlin scenarios we should cover next.
Does Speaking to Agents Like Cavemen Really Save 65% of Tokens? We Test
Does “rtk” skill really cut agent tokens by 60–90%? We tested it
Subscribe to Kotlin Blog updates
By submitting this form, I agree to the JetBrains
By submitting this form, I agree that JetBrains s.r.o. ("JetBrains") may use my name, email address, and location data to send me newsletters, including commercial communications, and to process my personal data for this purpose. I agree that JetBrains may process said data using
services for this purpose in accordance with the
JetBrains Privacy Policy
. I understand that I can revoke this consent at any time in
. In addition, an unsubscribe link is included in each email.
Thanks, we've got you!
Introducing Tracy: The AI Observability Library for Kotlin
Easily track LLM usage, tool calls, and application flow in
