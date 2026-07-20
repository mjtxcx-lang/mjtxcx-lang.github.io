# One Swift mistake everyone should stop making today

**来源:** [https://www.hackingwithswift.com/articles/280/one-swift-mistake-everyone-should-stop-making-today](https://www.hackingwithswift.com/articles/280/one-swift-mistake-everyone-should-stop-making-today)

**日期:** 2026-07-21

## 中文概述

每个Swift开发者都应该立即停止犯的一个错误

---

## 原文摘录

Save 50% on my books and bundles!
One Swift mistake everyone should stop making today
TL;DR: You should use replacing(_:with:) rather than replacingOccurrences(of:with:)
There’s a Swift mistake I see time and time again, it can cause serious problems, and it’s trivial to fix. I’ve talked about it before,
other people have talked about it before
, and I even made a long
Hacking with Swift+ video about it
I don’t believe in making folks wait, so here’s the simple answer: if you’re using the
replacingOccurrences(of:with)
you should probably change it to
to avoid causing unintentional and frankly
If you’re not sure why, read on – I’ll start by showing you the problem in a simple way, then show you the solution.
First, think about this code:
let vacation = "🇨🇦🇺🇸"
That’s a trivial string containing two flags. As it’s a string, we can check whether it contains the Canadian flag like this:
print(vacation.contains("🇨🇦"))
And we can check whether the string includes the US flag like this:
print(vacation.contains("🇺🇸"))
Both those will print true, because both those flags are present in the string.
Similarly, we could check whether the string contains the Australian flag like this:
print(vacation.contains("🇦🇺"))
, because clearly the string "🇨🇦🇺🇸" does not contain 🇦🇺.
print(vacation.replacingOccurrences(of: "🇦🇺", with: "🇳🇮"))
That replaces the Australian flag with the Nicaraguan flag, which sounds innocent but is at the core of the problem I’m talking about here.
If you’re reading this and
trying the code, this will hurt your head: that code will print “🇨🇳🇮🇸” – the flags for China and Iceland.
Yes, even though we’re replacing something that doesn’t exist in the string.
What’s happening here?
You know how to code. Now learn how to
My new app focuses on everything around your app that actually determines success, bringing together your App Store listing, competitor research, pricing, reviews, analytics, marketing, and launch workflow so you're never figuring it out alone.
Download Kickstart here
Problem, meet solution
replacingOccurrences(of:with:)
is an Objective-C method rather than Swift, which means it doesn’t have the Unicode safety that has been baked into Swift since day 1.
When we say “🇨🇦🇺🇸”, we’re really writing four characters:
Regional Indicator Symbol Letter C
Regional Indicator Symbol Letter A
Regional Indicator Symbol Letter U
Regional Indicator Symbol Letter S
The first two spell “CA”, which makes the Canadian flag. The latter two spell “US”, which makes the American flag. Each pair of regional indicator symbols makes a flag: GB makes the UK flag, JP makes the Japanese flag, and so on.
But in the middle of “CAUS” lies “AU”, which is the country code for Australia. Technically this ought to be impossible because it would leave “C” at the start by itself and “S” at the end by itself, which isn’t how these characters work – they come in pairs.
However, Objective-C doesn’t treat emoji with the same care that Swift does, so it replaces the regional symbols A and U with the Nicaraguan flag (N and I), making this:
Regional Indicator Symbol Letter C
Regional Indicator Symbol Letter N
Regional Indicator Symbol Letter I
Regional Indicator Symbol Letter S
Now we have “CNIS”, making the country codes for China and Iceland, which explains why we’re getting the strange output earlier.
While the behavior might make sense from a purely technical perspective, it’s clearly completely unwanted – it’s the kind of thing that will cause bizarre string bugs because Objective-C mashed up Unicode characters rather than treating them properly.
Fortunately, there’s a trivial fix: use Swift’s native
print(vacation.replacing("🇦🇺", with: "🇳🇮"))
That will leave the string “🇨🇦🇺🇸” untouched, as it should, because Swift
honors Unicode fully. Plus it’s less code to type, and likely to be faster too – it’s a win all around.
You know how to code. Now learn how to
My new app focuses on everything around your app that actually determines success, bringing together your App Store listing, competitor research, pricing, reviews, analytics, marketing, and launch workflow so you're never figuring it out alone.
Download Kickstart here
Introducing Kickstart: the app that helps indie developers ship
Teach your AI to write Swift the Hacking with Swift way
Agent skills in Xcode: How to install and use them today
SwiftUI Agent Skill - Write better code with Claude, Codex, and other AI tools
What to fix in AI-generated Swift code
Level up your SwiftUI
What's new in SwiftUI for iOS 26
What's new in Swift 6.2?
Was this page useful? Let us know!
Average rating: 4.3/5
Click here to visit the Hacking with Swift store >>
You are not logged in
Log in or create account
Link copied to your pasteboard.
