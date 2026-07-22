# Android Studio Quail 2 稳定版发布：并发 Agent、内存泄漏检测、AI 崩溃修复

> 原文：[Android Studio Quail 2 is Stable: Multi-task with the Android Studio AI agent](http://android-developers.googleblog.com/2026/06/android-studio-quail-2-stable-features.html) | 日期：2026-07-23

Android Studio Quail 2 正式进入稳定通道，带来三项重大更新：一是全新架构的 Agent Mode，支持同时运行多个 Agent 任务，每个任务可配置不同的 AI 模型，实现并发工作流（如一边重构架构一边修复崩溃）；二是将开源内存泄漏检测工具 LeakCanary 原生集成到 Profiler 中，将堆分析从测试手机转移到开发电脑上执行，泄漏追踪速度提升高达五倍，且不再影响测试应用的流畅度；三是 App Quality Insights（AQI）与 Agent Mode 的深度整合——点击崩溃报告即可获得 AI 生成的根因分析，点击"Fix with AI"按钮后 Agent 将自动分析问题、提出修复方案，经开发者确认后直接修改代码并验证修复效果。此外，该版本还修复了大量 bug 并同步了 IntelliJ 平台的最新稳定性改进。