# Android developer verification: Building a safer ecosystem together

**来源:** [http://android-developers.googleblog.com/2026/06/android-developer-verification.html](http://android-developers.googleblog.com/2026/06/android-developer-verification.html)

**日期:** 2026-07-21

## 中文概述

Android开发者身份验证上线：共同构建更安全的生态系统

---

## 原文摘录

Android Developers Blog
The latest Android and Google Play news for app and game
Android developer verification: Building a safer ecosystem together
Link copied to clipboard
Posted by Matthew Forsythe, Director Product Management, Android App Safety
July 15, 2026: Updated Play Console requirements for Play developers
To meet Android developer verification and
updated Play Console Requirements
, Play developers must
register their Play apps
in Play Console. While 99% of apps on Play have been registered automatically, you should check your
Play Console Home page
to register any remaining apps by September 30, 2026 to avoid global removal from Google Play and ensure a seamless user installation experience.
You can also use Play Console to register apps you distribute outside of Google Play to ensure they can be installed on certified Android devices.
Last year, we introduced
Android developer verification
to strengthen ecosystem security and stop malicious actors from hiding behind anonymity to release harmful apps. Millions of apps have been registered since the verification launched in March, covering nearly all installs on Google Play and a large majority of installs from outside of Google Play. We appreciate the feedback and partnership from industry leaders, developers, and Android communities that helped us design this experience and drive strong adoption.
Initial launch across seven stores and four countries
These new developer verification protections will take effect on September 30, 2026, starting with users in Brazil, Indonesia, Singapore, and Thailand.
industry-wide effort to create a safer ecosystem
. We will begin by verifying app installations from the following stores:
Honor (HONOR App Market)
OPlus (OPPO App Market)
Samsung (Galaxy Store)
Transsion (Palm Store)
Following this initial phase with our partners, we will expand these protections globally for all apps on certified Android devices in 2027.
Automate your workflow with new APIs
To further streamline app registration, we are
launching a suite of developer-requested APIs
to help you register apps in bulk or directly through your continuous integration and deployment (CI/CD) pipelines. The Android Developer ID Status API will let you check if a package name has already been registered, and the Android Developer Console API will let you register and manage package names directly within your development environment. Both APIs also support OAuth delegation, allowing third-party platforms, like Android app stores, to perform these operations natively on your behalf.
We'll launch these APIs over the next few months.
Starting this month, we are rolling out a new
that will be automatically installed on most Android devices. This service will be used later this year to verify developer registration.
We’ll launch the Android Developer ID Status API globally and begin early access for the Android Developer Console API. Early access also starts for
limited distribution accounts
on Android Developer Console. This new type of Android developer account is designed for students, hobbyists, and learners and lets you share your apps to up to 20 devices without a government-issued ID or a fee.
Limited distribution accounts and the new Android Developer Console API will launch globally. We’ll also launch an
for installing apps from unverified developers, which includes security checkpoints to resist coercion scams, while allowing power users to maintain the ability to
from unverified developers.
App registration becomes required for
participating stores in Brazil, Indonesia, Singapore, and Thailand
. Unregistered apps can be sideloaded with Android Debug Bridge (adb) or advanced flow.
After incorporating the feedback from our partners, users, and developer community, we’ll expand the Android verification requirement globally.
Get started with Android developer verification
If you distribute apps in Brazil, Indonesia, Singapore, or Thailand via the stores listed above, please ensure your verification is complete by the September deadline.
Google Play developers:
Most Play developers are already verified, and over 99% of their apps have been registered. Go to your
Play Console Home page
to see your app’s verification status, and
you want to continue distributing that weren't automatically registered.
Developers who distribute only outside of Google Play:
Android Developer Console
today to register your apps.
Students and hobbyists:
for early access to limited distribution accounts to help us refine the feature with your feedback.
Thank you for helping us build a safer Android ecosystem. Stay tuned for more updates as we approach September and the 2027 global rollout.
Google developers blog
Google Developers Blog
