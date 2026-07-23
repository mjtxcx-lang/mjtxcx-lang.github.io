# 构建智能Android应用：Gemini Nano端侧推理驱动本地AI体验

> 原文：[Build intelligent Android apps: On-device inference](http://android-developers.googleblog.com/2026/07/android-on-device-inference.html) | 日期：2026-07-24

Google详细介绍了在Android设备上使用Gemini Nano通过ML Kit的Prompt API构建端侧智能功能。端侧推理的优势包括隐私保护、离线可用和低延迟。文章以Jetpacker应用为例展示了三个端侧AI功能：行程摘要生成器（输入行程自动生成准备建议和当地常用短语）、收据费用管理器（拍照提取消费信息，敏感数据全程本地处理）和语音笔记。Gemini Nano 4是最新版本，基于Gemma 4架构，已运行在超过1.4亿台设备上，在电池和性能效率方面做了深度优化。通过ML Kit的Prompt API，开发者可以快速原型化端侧功能。一个关键优化案例：通过AICore应用的提示词迭代，将行程摘要的响应速度从13秒优化到2秒以内。Gemini Nano 4在多模态能力上也有显著提升，特别是OCR和视觉数据提取方面。
