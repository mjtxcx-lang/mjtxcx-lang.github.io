# Jetpacker 开源：Google 展示 Android 智能应用完整架构

> 原文：[Build intelligent Android apps: Introduction to Jetpacker](http://android-developers.googleblog.com/2026/07/build-intelligent-android-apps-introduction-jetpack.html) | 日期：2026-07-23

Google 在今年的 I/O 大会上发布了 Jetpacker——一个完全开源的 Android 智能应用技术展示项目，并围绕它推出了系列技术博客。Jetpacker 是一款旅行规划应用，从基础版本出发，逐步融入端侧推理、云端推理、混合推理、系统级智能集成和自主 Agent 等能力，完整呈现了从传统应用到 AI 原生应用的演进路径。具体来说：端侧推理（Gemini Nano 4）用于行程摘要、收据管理和语音笔记；云端推理（Firebase AI Logic）用于博物馆助手等需要大量世界知识的场景；混合推理动态切换本地与云端模型以优化成本；AppFunctions API 将应用核心能力暴露给 Android 操作系统；而基于 A2UI 和 ADK 的云端多 Agent 系统则实现了端到端的预订自动化。项目遵循 Material UI 设计规范和 Android 开发最佳实践，是学习 AI 应用开发的绝佳参考。