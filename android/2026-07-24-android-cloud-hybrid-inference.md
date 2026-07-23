# 构建智能Android应用：Firebase AI Logic实现云端与混合推理

> 原文：[Build intelligent Android apps: Cloud and hybrid inference](http://android-developers.googleblog.com/2026/07/build-intelligent-android-apps-cloud-hybrid-inference.html) | 日期：2026-07-24

Google发布"构建智能Android应用"系列博文的最新篇章，聚焦Firebase AI Logic实现云端和混合AI推理。文章以Jetpacker示例应用中的博物馆助手功能为例，展示了如何利用云端模型处理需要更丰富世界知识、更大上下文窗口或复杂查询的场景。核心创新在于Firebase AI Logic SDK支持的三种"接地"（Grounding）技术：Google搜索接地、URL上下文接地，以及混合推理。混合推理是最大亮点——Firebase API支持四种路由模式，优先使用端侧Gemini Nano执行任务以降低延迟和成本，在设备不支持时自动回退到云端模型，确保所有设备兼容。文章还展示了餐厅评论功能的实现：AI生成评论草稿后自动复制到剪贴板，并通过Intent直接打开Google Maps对应餐厅的评论页面，实现无缝用户体验。
