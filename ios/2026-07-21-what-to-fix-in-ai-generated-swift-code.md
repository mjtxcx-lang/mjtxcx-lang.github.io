# AI 生成的 Swift 代码需要修正的常见问题

> 原文：[What to fix in AI-generated Swift code](https://www.hackingwithswift.com/articles/281/what-to-fix-in-ai-generated-swift-code) | 日期：2026-07-21

随着 AI 辅助编程越来越流行，Paul Hudson 总结了 AI 生成 Swift 代码中最常见的需要修正的问题。

Swift 和 SwiftUI 对 AI 工具来说比其他平台更具挑战性，原因有三：语言和框架演进迅速、Python 和 JavaScript 有更大的代码库可供学习、AI 工具在 Swift 并发方面跟所有人一样挣扎。因此 Claude、Codex 和 Gemini 等工具经常会做出不太理想的选择。

**最需要关注的修正项：**

1. **`foregroundColor()` → `foregroundStyle()`**：字符数相同，但前者已弃用，后者支持渐变等高级功能。

2. **弃用 API 替换**：AI 经常使用已弃用的 API，需要手动替换为现代替代方案。

3. **性能优化**：AI 有时会写出低效的代码模式，特别是在列表和视图更新方面。

4. **Swift 并发**：AI 在 `async/await`、`@MainActor` 和 `Task` 的使用上经常出错。

5. **更简洁的写法**：AI 有时会写出冗长的代码，可以用 Swift 的现代语法简化。

Paul 强调，这篇文章假设目标是 iOS 18 及以上版本，并且这不是一份详尽清单，而是他最常见的检查项。