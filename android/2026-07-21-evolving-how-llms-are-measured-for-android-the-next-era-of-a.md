# Evolving how LLMs are measured for Android: the next era of Android Bench

**来源:** [http://android-developers.googleblog.com/2026/07/android-bench-llm-measurement.html](http://android-developers.googleblog.com/2026/07/android-bench-llm-measurement.html)

**日期:** 2026-07-21

## 中文概述

Android Bench基准测试升级：更全面评估LLM在Android开发中的表现

---

## 原文摘录

Android Developers Blog
The latest Android and Google Play news for app and game
Evolving how LLMs are measured for Android: the next era of Android Bench
Link copied to clipboard
Posted by Zoe Lopez-Latorre, Senior Developer Relations Engineer, Android
Back in March, we introduced
—our LLM leaderboard for real-world Android development tasks. Our goal was to provide transparency around model capabilities in Android development and to encourage model improvements, to give you more helpful AI options for your everyday workflow. Since then, we have enhanced the benchmark based on your feedback, including evaluating
and adding cost and efficiency dimensions to the leaderboard.
But AI capabilities are ever-evolving, and measurement needs to follow suit. As part of our July release, we have adopted the
, which includes an updated version of the benchmarking agent used to evaluate models.
Along with this change to our evaluation, in this July release we’re adding 8 new models (
Claude Fable 5, Claude Sonnet 5, Claude Opus 4.8, GLM 5.2, Kimi K2.7 Code, MiniMax M3, Qwen 3.7 Plus and Qwen 3.7 Max
) to the leaderboard. We’re also sharing opportunities for you, the Android developer community, to contribute to the benchmark.
Upgrading our methodology with the Harbor framework
When we designed Android Bench, we anchored our methodology on leading industry standards available at the time. We used mini-swe-agent v1, a general-purpose benchmarking agent, and adapted it to the nuances of Android development to provide a baseline measurement for the capabilities of models for common Android development tasks.
To continue providing you with state-of-the-art evaluations that accurately measure the latest model capabilities on Android development, we are standardizing our benchmark to the
. Harbor defines standards and integrations that make it easy for anyone to run the benchmark, evaluate their preferred set-up, or share results – providing you with additional transparency and visibility.
This upgrade enables us to more rigorously evaluate models and their capabilities, and we re-ran the benchmark on all models to establish an updated baseline. This means there is a minor shift in scoring, but you will still be able to view historical scores within
We want to ensure Android Bench is helpful for you, so we will continuously update it as our evaluations and the industry mature.
Expanding the leaderboard with 8 new models
As part of our commitment to keeping the leaderboard fresh, we have added Claude Fable 5, Claude Sonnet 5, Claude Opus 4.8, GLM 5.2, Kimi K2.7 Code, MiniMax M3, Qwen 3.7 Plus and Qwen 3.7 Max to the Android Bench leaderboard.
is at the top of the leaderboard with a score of 84.5, followed by
in 3rd with a score of 76.2.
When just comparing Open-weight models,
is at the top with 72.2, followed by
with a score of 70.4.
You can check out model performance and efficiency metrics on the updated leaderboard to see how these new and previous models navigate Android-specific challenges like Jetpack Compose migrations, wearable networking, and platform API updates.
Opening Android Bench to community contributions
From the beginning, we’ve valued an open and transparent approach, which is why we made our original methodology and test harness publicly available on GitHub. You’ve asked for a way to provide feedback on our dataset, so now we’re taking collaboration a step further by giving you, the Android developer community, a chance to shape Android Bench.
Starting today, you can contribute to Android Bench in two ways:
submit your own Android development tasks
to evaluate how models handle the scenarios that matter to you.
Run and share benchmark evaluations
firsthand, testing your preferred models against our dataset or your own custom tasks.
We will be reviewing the submitted tasks and will be assessing if they get added to the benchmark. We hope to build a benchmark that truly reflects the diverse, day-to-day realities of the global Android developer community.
With more and more options for agentic development, maintaining a cutting-edge benchmark ensures that the AI assistance you rely on keeps getting smarter, more helpful, and more effective. Head over to our
to check out the tasks. We invite you to submit a task to our team for review, and you can check out
to explore the dataset or submit evaluations.
As always, you can find the
Android Bench, LLM leaderboard, Harbor framework, Android development, Claude Fable 5, GPT 5.5, Claude Sonnet 5, GLM 5.2, Kimi K2.7 Code, MiniMax M3, Qwen 3.7 Plus, Qwen 3.7 Max, AI benchmarking, Jetpack Compose migration, wearable networking, mobile AI agent, Zoe Lopez-Latorre, model evaluation, open-weight models, developer community contributions.
Google developers blog
Google Developers Blog
