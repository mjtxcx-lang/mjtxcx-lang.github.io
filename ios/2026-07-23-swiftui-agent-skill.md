# SwiftUI Agent Skill 开源发布：让 AI 写出更地道的 SwiftUI 代码

> 原文：[SwiftUI Agent Skill - Write better code with Claude, Codex, and other AI tools](https://www.hackingwithswift.com/articles/282/swiftui-agent-skill-claude-codex-ai) | 日期：2026-07-23

Paul Hudson 发布了开源 SwiftUI Agent Skill，旨在帮助 Claude Code、Codex 和 Gemini 等 AI 编程工具识别并修复 SwiftUI 代码中的常见问题。该技能覆盖了现代 API 使用、性能优化、无障碍（Accessibility）支持等多个维度，能够自动检测并建议修复 AI 生成的 SwiftUI 代码中的反模式（anti-patterns）——例如使用已弃用的 API、导致性能问题的代码模式、VoiceOver 不可见的按钮等。技能基于 Paul 此前编写的 AGENTS.md 文件扩展而来，增加了更多检查和最佳实践建议，包括并发编程技巧、设计指导和项目规范等。安装极为简便，只需一行命令：`npx skills add https://github.com/twostraws/swiftui-agent-skill --skill swiftui-pro`。该技能支持多种 Agent 平台，安装后即可在 Claude Code、Codex 等工具中生效。