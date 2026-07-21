# Nearby Connections API 即将迎来重大变更

> 原文：[Upcoming Changes to the Nearby Connections API](http://android-developers.googleblog.com/2026/07/upcoming-changes-nearby-connections-api.html) | 日期：2026-07-21

发布者：Wei Wang，Android BeTo 工程经理

用户隐私和透明度是 Android 体验的核心。为了更好地遵循这些原则，我们正在更新 Nearby Connections API（就近连接 API）关于设备无线电交互的默认行为。

## 发生了什么变化？

此前，Nearby Connections API 可以在无需用户明确干预的情况下自动开启 Wi-Fi 和蓝牙无线电以建立连接。从现在开始，对于第一方（1P）和第三方（3P）应用，该 API 将不再自动启用这些无线电。

## 这对开发者意味着什么？

如果你的应用依赖 Nearby Connections，你需要更新实现以应对这些变化：

- **手动无线电管理**：你必须确保在启动 Nearby Connections 任务之前，所需的无线电（Wi-Fi 或蓝牙）已经开启。
- **用户通知**：如果所需的无线电处于关闭状态，你的应用现在必须通知用户并要求他们手动启用。API 将不再为你通过程序化方式自动开启。

## 时间安排

这些变更计划于 2026 年底生效。我们建议你现在就审查你的连接工作流程，以确保为用户带来无缝的过渡体验。