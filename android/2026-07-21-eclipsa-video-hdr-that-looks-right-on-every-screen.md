# Eclipsa Video：让 HDR 在每一块屏幕上都能正确呈现

> 原文：[Eclipsa Video: HDR That Looks Right on Every Screen](http://android-developers.googleblog.com/2026/06/eclipsa-video-hdr-review.html) | 日期：2026-07-21

发布者：Tibian Elsheikh，Android Core Graphics 产品经理 & Jeffrey Jose，Android Core Graphics 产品经理

我们都经历过这样的场景：你在昏暗的房间里刷着最爱的社交媒体动态，突然弹出一个 HDR（高动态范围）视频。它亮得刺眼，让你不得不眯起眼睛，或者你发现自己不得不调低屏幕亮度才能看清配文。其他时候，一段在手机上看起来鲜艳生动的视频，在客厅电视上观看时却显得平淡、灰暗或褪色。

虽然 HDR 技术旨在让视频看起来更丰富、更逼真，但缺乏统一的行业指南意味着完全相同的视频内容可能因你所使用的显示器不同而呈现出意想不到且令人不适的效果。

为了解决这个问题，我们推出了 Eclipsa Video——一项新标准，旨在让你喜爱的视频在每块屏幕上看起来都一致、平衡且舒适。Eclipsa Video 基于开放的 SMPTE ST 2094-50 规范构建，该规范由 Google 与 Apple 和 NBCUniversal 合作开发。

## 更高的一致性、舒适度和创意控制

Eclipsa Video 超越了单个显示器的猜测。我们的格式不再让设备自行解读视频的亮度，而是携带精确的指导信息，告诉兼容的显示器如何准确地渲染图像。Eclipsa Video 可随硬件扩展，提供三个核心优势：

- **一致的基准线**：Eclipsa Video 为屏幕引入了统一的规则手册。它建立了一个一致的标准亮度基准——称为 HDR 参考白点（HDR Reference White）。这确保了标准文本、应用界面和标准范围色彩保持鲜艳和可读，而不会造成令人不适的屏幕眩光。

- **自适应动态范围余量**：屏幕有不同的物理亮度上限，即"动态范围余量"（Headroom）。Eclipsa Video 指导显示器如何动态处理高光部分。在高端电视上，明亮的细节保持绚丽夺目；而在手机屏幕上，则会智能缩放以防止突然的刺眼过渡。

- **保留创作者意图**：Eclipsa Video 不是对整个视频应用单一的静态设置，而是携带自适应的逐帧指令。可以把它想象成随视频一起传输的创作者数字笔记，确保他们调色的精确色彩、对比度和氛围在你的显示器上得以保留。