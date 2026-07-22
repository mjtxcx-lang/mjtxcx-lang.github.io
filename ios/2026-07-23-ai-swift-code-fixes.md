# AI 生成的 Swift 代码有哪些坑？资深开发者逐条拆解

> 原文：[What to fix in AI-generated Swift code](https://www.hackingwithswift.com/articles/281/what-to-fix-in-ai-generated-swift-code) | 日期：2026-07-23

Paul Hudson 总结了 AI 工具（Claude、Codex、Gemini 等）在生成 Swift/SwiftUI 代码时最常犯的几类错误，并给出对应的修复方案。由于 Swift 语言和框架迭代迅速、训练语料库相对 Python/JavaScript 较小，以及 Swift 并发本身的高复杂性，AI 生成的代码常出现以下问题：使用已弃用的 API、编写低效代码、过度使用 GeometryReader（常配合不当的固定 frame 尺寸）、以及给出可更简洁表达的冗余写法。Paul 特别指出，LLM 对 GeometryReader 有"近乎偏执的偏爱"，建议开发者优先考虑 `visualEffect()` 和 `containerRelativeFrame()` 等替代方案。此外，AI 还经常"幻觉"出不存在的 API——这一问题目前尚无根本解决方案。文章最后向社区征集了大家在 AI 生成代码中常见的其他问题。