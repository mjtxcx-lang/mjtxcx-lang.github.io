# Android Studio Quail 2稳定版发布：多任务AI Agent、原生LeakCanary集成

> 原文：[Android Studio Quail 2 is Stable: Multi-task with the Android Studio AI agent](http://android-developers.googleblog.com/2026/06/android-studio-quail-2-stable-features.html) | 日期：2026-07-24

Android Studio Quail 2正式发布稳定版，带来三大核心升级。首先是Agent Mode的全面重构：新架构支持并行运行多个Agent任务，且可为不同任务选择不同模型，实现真正的并发Agent工作流。其次，广受欢迎的开源内存泄漏检测工具LeakCanary被原生集成到Profiler中，作为一等公民任务直接内置于IDE——堆分析从资源受限的测试手机转移到开发电脑上执行，泄漏追踪速度提升高达5倍且不会造成应用卡顿。第三，App Quality Insights（AQI）与Agent Mode深度集成：点击崩溃报告即可获得AI生成的简明摘要，进一步点击即可在专用聊天中获取包含源码和完整堆栈跟踪的全面分析，AI还能提出修复方案并直接应用代码变更。此外，Quail 2还整合了IntelliJ平台的最新稳定性和性能改进。
