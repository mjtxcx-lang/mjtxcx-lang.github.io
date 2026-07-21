# AI 生成的 Swift 代码有哪些坑？五种常见问题及修复方法

> 原文：[What to fix in AI-generated Swift code](https://www.hackingwithswift.com/articles/281/what-to-fix-in-ai-generated-swift-code) | 日期：2026-07-22

Paul Hudson 总结了 AI 工具（Claude、Codex、Gemini 等）在生成 Swift 和 SwiftUI 代码时的常见问题。Swift 语言和框架演进迅速，且相比 Python 和 JavaScript 训练数据较少，导致 AI 工具表现不佳。主要问题包括：使用已弃用的 API、效率低下的代码模式、过度使用 GeometryReader 并搭配不当的固定 frame 尺寸、忽略 Swift 并发特性导致线程安全问题、以及幻觉出不存在的 API。Hudson 建议使用 `visualEffect()` 和 `containerRelativeFrame()` 等现代替代方案，并已将这些问题整理为 AGENTS.md 文件以帮助 LLM 改进。
