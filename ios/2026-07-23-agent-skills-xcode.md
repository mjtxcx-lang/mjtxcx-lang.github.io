# 在 Xcode 中使用 AI Agent Skills：安装与实战指南

> 原文：[Agent skills in Xcode: How to install and use them today](https://www.hackingwithswift.com/articles/283/how-to-install-and-use-ai-agent-skills-in-xcode) | 日期：2026-07-23

Paul Hudson（Hacking with Swift 创始人）发布了一篇详细的教程，手把手教开发者在 Xcode 中安装和使用 AI Agent Skills。Agent Skills 是专为解决特定编码任务而设计的工具，Paul 已为 SwiftUI、Swift Testing、Swift Concurrency 和 SwiftData 分别编写了对应的技能文件。安装流程因工具而异：对于 Claude Code 和 Codex 的命令行版本，只需运行 `npx skills add` 命令即可一键安装；对于 Xcode（需先在 Settings > Intelligence 中配置内置或自定义 AI agent），Codex 的技能可自动同步，但 Claude for Xcode 需要额外手动配置。Paul 还介绍了他的 Swift Agent Skills GitHub 仓库，以及如何评估哪些技能适合自己的项目。文章同时对比了 Agent Skills 与 AGENTS.md 文件的区别，建议两者配合使用以获得最佳效果。