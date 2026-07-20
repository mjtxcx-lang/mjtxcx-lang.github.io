# SwiftUI Agent Skill - Write better code with Claude, Codex, and other AI tools

**来源:** [https://www.hackingwithswift.com/articles/282/swiftui-agent-skill-claude-codex-ai](https://www.hackingwithswift.com/articles/282/swiftui-agent-skill-claude-codex-ai)

**日期:** 2026-07-21

## 中文概述

开源SwiftUI Agent Skill发布：自动修复AI生成的SwiftUI常见错误

---

## 原文摘录

Save 50% on my books and bundles!
SwiftUI Agent Skill - Write better code with Claude, Codex, and other AI tools
Improve the AI-written code in all your SwiftUI projects with my free agent skill
If you’re writing SwiftUI with AI coding agents like Claude Code, Codex, or Gemini, I’ve written an open-source
that helps identify and fix common mistakes they make when writing SwiftUI – things like modern API usage, performance, accessibility, and more.
, so it works in a wide variety of agents and will bring immediate benefit to any SwiftUI project.
Even better, most people can install it with just one command:
npx skills add https://github.com/twostraws/swiftui-agent-skill --skill swiftui-pro
For more information about installing and using agent skills in Xcode, check out my YouTube video:
Agent Skills in Xcode - Build better SwiftUI apps with AI agents
I've released several more agent skills, covering SwiftUI, SwiftData, Swift Concurrency, and Swift Testing. You can find them all in a new repository:
You know how to code. Now learn how to
My new app focuses on everything around your app that actually determines success, bringing together your App Store listing, competitor research, pricing, reviews, analytics, marketing, and launch workflow so you're never figuring it out alone.
Download Kickstart here
Why I made this skill
I’ve been working with SwiftUI since June 2019, and as it evolved over time I started to see people adopt some coding patterns that were less than ideal – they sometimes made buttons invisible to VoiceOver, they used deprecated API without realizing, and they would accidentally write code that caused performance problems.
In the past I’ve run workshops helping folks identify this kind of code and get it resolved, culminating in my famous
workshop. But when LLMs started writing SwiftUI code they
adopted many of the same anti-patterns, so I wanted to go a step further.
Recently I wrote an article about
the biggest problems in AI-generated Swift code
, and also converted it to an
that quietly helps make all LLMs smarter while they work.
Sadly, a prominent member of our community decided to plagiarize me, taking huge swathes of my work (often word for word!) and copying it into their own project, then adding their own name at the top as copyright.
You can find out more about that in a video I made about building apps with AI
I don’t have the patience for that kind of behavior, so I built this agent skill to show that we’re better – it’s packed with everything from
my original AGENTS.md file
and a whole lot more.
💫 Fully updated API guidance to help you write the smartest, simplest SwiftUI.
🚀 Actionable, real-world advice based on years of experience.
🙌 The guarantee that checks have not been stolen from other people.
I’ve packed my SwiftUI agent skill with a wide range of checks and advice that will help tools like Claude Code and Codex review your code and suggest lots of helpful improvements, including:
Extensive advice on deprecated API and what to use instead, such as avoiding
, and staying away from
unless it’s strictly required.
Performance tips such as avoiding doing
work in initializers or
properties, breaking up SwiftUI views to make the most of the
macro, and modern formatting APIs.
Accessibility guidance such as ensuring all controls are labeled, touch areas are big enough, and fonts scale correctly.
Useful Swift tips such as
localizedStandardContains()
, and using automatic grammar agreement.
…and that’s just a tiny slice of what’s in there – you’ll also find concurrency tips, design help, project hygiene advice, and more, all of which come together to help ensure the Swift agent of your choosing is as helpful as possible.
I hope the skill is useful to you!
You know how to code. Now learn how to
My new app focuses on everything around your app that actually determines success, bringing together your App Store listing, competitor research, pricing, reviews, analytics, marketing, and launch workflow so you're never figuring it out alone.
Download Kickstart here
Introducing Kickstart: the app that helps indie developers ship
Teach your AI to write Swift the Hacking with Swift way
Agent skills in Xcode: How to install and use them today
What to fix in AI-generated Swift code
One Swift mistake everyone should stop making today
Level up your SwiftUI
What's new in SwiftUI for iOS 26
What's new in Swift 6.2?
Was this page useful? Let us know!
Average rating: 4.9/5
Click here to visit the Hacking with Swift store >>
You are not logged in
Log in or create account
Link copied to your pasteboard.
