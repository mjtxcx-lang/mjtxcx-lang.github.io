# SwiftUI Agent技能开源发布：自动修正AI生成代码中的常见错误

> 原文：[SwiftUI Agent Skill - Write better code with Claude, Codex, and other AI tools](https://www.hackingwithswift.com/articles/282/swiftui-agent-skill-claude-codex-ai) | 日期：2026-07-24

Paul Hudson发布了一个开源的SwiftUI Agent技能，专门帮助AI编程工具（如Claude Code、Codex、Gemini）识别和修复生成SwiftUI代码时的常见错误。该技能涵盖了现代API使用、性能优化、无障碍访问等多个方面。由于大语言模型在训练时学习了大量包含不良编程模式的SwiftUI代码，它们经常重复这些反模式——比如按钮对VoiceOver不可见、使用已废弃的API、无意中造成性能问题等。这个Agent技能基于Hudson之前发布的AGENTS.md文件扩展而来，内置了丰富的代码检查和建议，包括并发编程技巧、设计辅助、项目规范建议等。安装只需一条`npx skills add`命令，支持大多数主流AI编程工具。该技能是Swift Agent Skills开源仓库的一部分，此外还有SwiftData、Swift并发和Swift Testing等技能。
