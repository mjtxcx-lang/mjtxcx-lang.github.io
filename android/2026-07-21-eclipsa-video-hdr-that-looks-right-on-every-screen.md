# Eclipsa Video: HDR That Looks Right on Every Screen

**来源:** [http://android-developers.googleblog.com/2026/06/eclipsa-video-hdr-review.html](http://android-developers.googleblog.com/2026/06/eclipsa-video-hdr-review.html)

**日期:** 2026-07-21

## 中文概述

Eclipsa Video：让HDR视频在所有屏幕上都能正确显示的新格式

---

## 原文摘录

Android Developers Blog
The latest Android and Google Play news for app and game
Eclipsa Video: HDR That Looks Right on Every Screen
Link copied to clipboard
Posted by Tibian Elsheikh, Product Manager, Android Core Graphics and Jeffrey Jose, Product Manager, Android Core Graphics
We’ve all been there: You’re scrolling through your favorite social media feed in a dim room, and suddenly an HDR video pops up. It’s so intensely bright that you have to squint, or maybe you find yourself turning down your screen brightness just to read the caption. Other times, a video that looks vibrant on your phone looks flat, dark, or washed out when you watch it on your living room TV.
While High Dynamic Range (HDR) technology was designed to make videos look richer and more lifelike, the lack of unified industry guidelines means that the exact same clip can render in unexpected and jarring ways depending on the display you’re using.
To solve this, we’re introducing Eclipsa Video—a new standard built to make your favorite videos look consistent, balanced, and comfortable on every screen. Eclipsa Video builds on the open
SMPTE ST 2094-50 specification
, which Google developed in collaboration with Apple and NBCUniversal.
Sudden brightness spikes during feed scrolling—fixed with Eclipsa Video.
More consistency, comfort, and creative control
Eclipsa Video moves past individual display guesswork. Instead of leaving it up to your device to interpret a video’s brightness on its own, our format carries precise guidelines that tell compatible displays exactly how to render the image.
Designed to scale with your hardware, Eclipsa Video provides three core benefits:
A consistent baseline:
Eclipsa Video introduces a shared rulebook for screens. It establishes a consistent benchmark for normal brightness—known as the
. This ensures standard text, app interfaces, and standard-range colors remain vibrant and readable without causing uncomfortable screen glare.
Screens have different physical brightness limits, or "headroom." Eclipsa Video guides how displays handle highlights dynamically. Bright details remain brilliant on a premium television, while being scaled intelligently on a mobile screen to prevent sudden blinding transitions.
Preserved creative intent:
Rather than applying a single static setting to an entire video, Eclipsa Video carries adaptive, frame-by-frame instructions. Think of it as a set of digital notes from the creator traveling with the video, ensuring the exact colors, contrast, and mood they graded are preserved on your display.
Eclipsa Video preserves true highlight detail on any screen you watch.
Built natively into Android 17
Starting with Android 17, support for Eclipsa Video is built directly into the platform. This means a more comfortable, true-to-life HDR experience is coming natively to the phones, tablets, and TVs you rely on every day. The video you capture carries its creative intent with it, and the video you watch is shown exactly the way it was meant to be seen.
Guidelines for developers & creators
We’re inviting the developer and creator ecosystem to help build a more reliable HDR environment:
Get started with implementation:
Learn how to configure playback and capture in your apps with our
ExoPlayer & Media3 integration:
Standard playback handling built directly into
allowing ExoPlayer to support Eclipsa Video metadata automatically with no additional player configuration.
Explore open source tools:
metadata and dynamic gain curves in real time using
Eclipsa Video is rolling out now, and you’ll see more apps and devices supporting it over time. Because it’s an open standard, any app developer or hardware manufacturer can integrate it to elevate the viewing experience.
Try out the new tools in Android 17, explore the open-source metadata, and let us know what you think on our developer channels. We can’t wait to see what you create.
1. Device Compatibility:
Eclipsa Video playback and capture are supported natively on devices running Android 17 (API level 37) and above with HDR displays passing Eclipsa Compliance tests.
2. Developer Resources:
SMPTE ST 2094-50 Specification
is openly accessible for technical evaluation.
Google developers blog
Google Developers Blog
