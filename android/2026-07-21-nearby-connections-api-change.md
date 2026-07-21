# Android Nearby Connections API 将不再自动开启 Wi-Fi 和蓝牙

> 原文：[Upcoming Changes to the Nearby Connections API](http://android-developers.googleblog.com/2026/07/upcoming-changes-nearby-connections-api.html) | 日期：2026-07-22

Google 宣布将于 2026 年底对 Nearby Connections API 进行重要变更，以更好地符合用户隐私和透明度原则。此前该 API 可在未经用户明确干预的情况下自动开启 Wi-Fi 和蓝牙，变更后将不再自动启用这些无线通信模块。依赖此 API 的应用需要更新实现：在尝试建立连接前主动检查并请求用户开启相关无线功能，同时提供清晰的用户界面说明为何需要这些权限。Google 建议开发者尽早检查连接工作流，确保平滑过渡。
