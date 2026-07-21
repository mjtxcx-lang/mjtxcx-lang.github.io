# SwiftUI Agent Skill：让 AI 写出更好的 SwiftUI 代码

> 原文：[SwiftUI Agent Skill - Write better code with Claude, Codex, and other AI tools](https://www.hackingwithswift.com/articles/282/swiftui-agent-skill-claude-codex-ai) | 日期：2026-07-21

Paul Hudson 发布了一个开源 SwiftUI Agent Skill，帮助识别和修复 Claude Code、Codex、Gemini 等 AI 编程 agent 在编写 SwiftUI 时的常见错误。

这个 Agent Skill 覆盖了现代 API 使用、性能优化、无障碍访问（Accessibility）等多个方面。它基于 Agent Skills 格式构建，兼容多种 AI agent，可以为任何 SwiftUI 项目带来立竿见影的改进。

**一键安装：**
```bash
npx skills add https://github.com/twostraws/swiftui-agent-skill --skill swiftui-pro
```

**为什么需要这个 Skill？**
Paul 自 2019 年 6 月起就在使用 SwiftUI，随着框架的演进，他注意到许多开发者采用了一些不太理想的编码模式——比如让按钮对 VoiceOver 不可见、使用已弃用的 API 而不自知、意外写出导致性能问题的代码。当 LLM 开始编写 SwiftUI 代码时，这些问题变得更加普遍。

Paul 还发布了更多 Agent Skills，覆盖 SwiftUI、SwiftData、Swift Concurrency 和 Swift Testing，全部可以在 Swift Agent Skills 仓库中找到。