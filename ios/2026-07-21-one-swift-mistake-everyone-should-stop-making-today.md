# 每个 Swift 开发者都应该立即停止犯的一个错误

> 原文：[One Swift mistake everyone should stop making today](https://www.hackingwithswift.com/articles/280/one-swift-mistake-everyone-should-stop-making-today) | 日期：2026-07-21

Paul Hudson 指出一个他反复看到的 Swift 错误，这个错误可能导致严重问题，但修复起来却非常简单。

**核心建议：** 如果你在使用 `String` 的 `replacingOccurrences(of:with:)` 方法，应该改用 `replacing(_:with:)`，以避免产生意想不到的奇怪 bug。

**问题演示：**
```swift
let vacation = "🇨🇦🇺🇸"
print(vacation.replacingOccurrences(of: "🇦🇺", with: "🇳🇮"))
```

这段代码输出的是 `"🇨🇳🇮🇸"`（中国和冰岛的国旗）——即使字符串中根本不存在澳大利亚国旗！

这是因为 `replacingOccurrences(of:with:)` 在 Unicode 层面进行字符替换，而某些国旗 emoji 由多个 Unicode 标量组成。当方法在字符级别搜索时，可能匹配到组成其他国旗的部分 Unicode 序列，导致"替换了不存在的东西"。

**解决方案：** 使用 `replacing(_:with:)` 方法，它在 `String` 的 `Comparable` 层面进行替换，能正确处理 Unicode 组合字符，避免这种诡异的 bug。