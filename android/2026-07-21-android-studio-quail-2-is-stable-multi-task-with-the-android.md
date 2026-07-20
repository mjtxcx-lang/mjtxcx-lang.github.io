# Android Studio Quail 2 is Stable: Multi-task with the Android Studio AI agent

**来源:** [http://android-developers.googleblog.com/2026/06/android-studio-quail-2-stable-features.html](http://android-developers.googleblog.com/2026/06/android-studio-quail-2-stable-features.html)

**日期:** 2026-07-21

## 中文概述

Android Studio Quail 2正式版发布：内置AI编程助手支持多任务并行

---

## 原文摘录

Android Developers Blog
The latest Android and Google Play news for app and game
Android Studio Quail 2 is Stable: Multi-task with the Android Studio AI agent
Link copied to clipboard
Posted by Amman Asfaw, Product Manager, Android Studio
Android Studio Quail 2 is now stable and ready for you to use in production, bringing a shift to your IDE with concurrent agentic workflows, natively integrated memory leak profiling, and context-aware crash remediation. Whether you are performing a sweeping architectural overhaul, tracing a memory leak, or resolving a critical production crash, Android Studio keeps you anchored in your workspace by reducing manual friction.
Here’s a deep dive into what’s new:
Multi-tasking with parallel chats
In Android Studio Quail 2, we've been hard at work redesigning Agent Mode from the ground up. This new architecture provides better performance, offers more flexibility for decomposing complex tasks, and improves the suite of internal tools the agent uses to do its work.
In addition to these behind-the-scenes improvements, these changes also allow you to converse across multiple agent chats simultaneously. Waiting for the Android Studio agent to finish a task before you can ask another question or initiate a separate task in Agent Mode is a bottleneck of the past. You can multi-task seamlessly: kick off a UI refactor in one tab, fix a ProGuard rule in a second, and generate documentation in a third.
You can also change which models the agent uses from chat to chat based on the requests you have. Take a look at
for an analysis of how LLMs perform Android development tasks.
Click the "+" icon to start a new parallel conversation, and use the
icon to navigate between active tasks. Alternatively, select File > New > New Agent Tab to open a conversation in a dedicated tab.
Worktree support is currently unavailable. Exercise caution when running concurrent chats that modify the same project files, which can potentially lead to editor conflicts.
Run multiple agent tasks in parallel with different models of your choice.
Use the History icon to navigate between active tasks.
Memory leak detection with LeakCanary
Memory leaks in Android occur when your code holds onto an object's reference long after its life cycle has ended. This prevents the Garbage Collector from reclaiming that memory, eventually leading to sluggish performance or
Hunting down memory leaks can be a tedious, manual task. Starting with Android Studio Quail 2, the popular open-source leak detector
is natively integrated directly into the Profiler as a dedicated, first-class task.
This integration transforms your debugging performance by lifting and shifting the heap analysis off your resource-constrained testing phone, and onto your powerful development computer. By running the analysis on your computer, leak tracing is up to five times faster and jank-free, leaving your test app running smoothly on the device.
Once a leak is detected during a profiling session:
The Profiler renders an interactive, color-coded leak trace, grouping occurrences and estimating lost memory.
on any leaking object in the trace to instantly jump to that exact line of code in your editor.
to have the Gemini agent ingest the trace, explain the root cause of the retained reference, and write the exact code change (such as unbinding a listener or clearing a static reference) to plug the leak.
Review memory leaks identified via LeakCanary through the Fix with Agent button.
App Quality Insights agent integration
Tracking down the root cause of an app crash can require manually synthesizing stack traces, device data, and source code. However Android Studio’s App Quality Insights (AQI) is now fully integrated with Agent Mode to do the heavy lifting for you.
When you click on a crash in the AQI panel, you immediately get a concise, high-level summary of the issue. If you need to dig deeper, simply click
. This opens a dedicated chat where the agent uses your selected model and pulls in local source code and the full stack trace to deliver a comprehensive explanation of the failure.
With the new agent integration, you move directly from issue identification to resolution. By clicking
, the agent will analyze the issue, propose a step-by-step fix plan, and—upon your approval—apply the necessary code changes directly to your project and verify the resulting fix
button triggering the agent to analyze the issue, then propose the fix
Quality & stability improvements
Beyond new features, we’ve continued our focus on quality by addressing numerous bugs and incorporating the latest stability and performance improvements from the IntelliJ platform, making this a significant enhancement for your daily development.
Ready to dive in and accelerate your development?
Android Studio Quail 2 and start exploring these new features today! As always, your feedback is crucial to us.
, and be part of our vibrant community on
Google developers blog
Google Developers Blog
