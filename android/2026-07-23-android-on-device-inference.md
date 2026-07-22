# Android 端侧推理实战：Gemini Nano 4 驱动本地 AI 功能

> 原文：[Build intelligent Android apps: On-device inference](http://android-developers.googleblog.com/2026/07/android-on-device-inference.html) | 日期：2026-07-23

Google 详细介绍了如何利用 Gemini Nano 4 和 ML Kit Prompt API 在 Android 设备上构建端侧 AI 功能。文章以 Jetpacker 应用为例，展示了三个完全离线运行的场景：行程摘要（输入行程计划，生成准备建议和当地常用短语）、收据管理（利用 Gemini Nano 4 增强的多模态能力实现 OCR 和数据提取，敏感信息如信用卡号完全在本地处理）和语音笔记。Gemini Nano 4 基于最新 Gemma 4 架构构建，已在超过 1.4 亿台设备上运行，针对电池和性能效率进行了深度优化。文章特别强调了 prompt 调优的价值——通过 AICore 应用的开发者预览模式反复迭代 prompt，成功将首次响应时间从 13 秒降至 2 秒以内。端侧推理的核心优势在于零云端成本、无需网络连接，以及隐私数据不外传的天然安全性。