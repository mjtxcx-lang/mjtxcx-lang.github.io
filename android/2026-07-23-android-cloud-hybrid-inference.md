# Android 智能应用开发：云端与混合推理实践指南

> 原文：[Build intelligent Android apps: Cloud and hybrid inference](http://android-developers.googleblog.com/2026/07/build-intelligent-android-apps-cloud-hybrid-inference.html) | 日期：2026-07-23

Google Android 开发者博客发布了"构建智能 Android 应用"系列的第二篇技术文章，深入讲解如何使用 Firebase AI Logic 实现云端和混合 AI 推理。文章以开源示例应用 Jetpacker 为案例，展示了三个实战场景：博物馆助手（聊天机器人）利用 Firebase AI Logic SDK 的三种 grounding 技术——Google Search 搜索增强、URL 上下文注入和自定义工具调用——来提供实时、准确的展馆信息；餐厅评论生成功能则使用 Firebase 混合推理（Hybrid Inference）API，优先在支持 Gemini Nano 的设备上本地执行，不支持时自动回退到云端模型，兼顾成本、延迟和离线可用性。混合推理 API 支持四种路由模式：优先本地（PREFER_ON_DEVICE）、仅本地、仅云端和自动选择。代码示例展示了如何通过 `Firebase.ai.generativeModel()` 配置模型并动态构建工具列表。