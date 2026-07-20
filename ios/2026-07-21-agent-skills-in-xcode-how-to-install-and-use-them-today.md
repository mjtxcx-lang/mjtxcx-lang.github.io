# Agent skills in Xcode: How to install and use them today

**来源:** [https://www.hackingwithswift.com/articles/283/how-to-install-and-use-ai-agent-skills-in-xcode](https://www.hackingwithswift.com/articles/283/how-to-install-and-use-ai-agent-skills-in-xcode)

**日期:** 2026-07-21

## 中文概述

Xcode中安装Agent Skills完整指南：让Claude/Codex写出更好的SwiftUI代码

---

## 原文摘录

Save 50% on my books and bundles!
Agent skills in Xcode: How to install and use them today
Get agent skills for Swift, SwiftUI, Swift Testing, and more
If you’re building apps with agents such as Codex or Claude, this article is for you – I’m going to show you to use agent skills to make them smarter, so they write better code, faster.
We’ll look at how to install and use these agent skills in Xcode, Claude Code, Codex, Gemini, and more. We’ll to look at where to find great agent skills for app development using my new
GitHub repository, and how to evaluate which agents skills will work well. And I’m also going to show you how agent skills are different from AGENTS files, and why you might want both.
The result will be that using AI to write, review, or test code will be so much better, whether you’re using SwiftUI, Swift concurrency, SwiftData, Swift Testing, or something else.
If you missed my previous
video about how to build apps with AI
, I suggest you start there – it walks you through using Xcode, Claude Code, Codex, and more, with lots of tips for getting the most from Xcode, configuring your terminal, getting the most from ChatGPT, and more.
If you’d prefer to watch this as a video, you can find it below. Alternatively, scroll past the video to read the article instead.
Still here? Okay, let’s get into agent skills…
You know how to code. Now learn how to
My new app focuses on everything around your app that actually determines success, bringing together your App Store listing, competitor research, pricing, reviews, analytics, marketing, and launch workflow so you're never figuring it out alone.
Download Kickstart here
Installing agent skills into Xcode
Agent skills are powerful tools designed to solve specific jobs in your code. I’ve written agent skills to improve your SwiftUI code, to make the most of Swift Testing, to optimize your Swift concurrency code, and even to make sure you’re using SwiftData effectively – each skill does one thing, and does it
Before we get into how agent skills work, I want you to see them in action because they are really transformative.
If you’re installing skills from the command line for tools like Claude Code or Codex, it’s easy. But when using Xcode, it might take a few more steps.
First, make sure you have Xcode set up to use agentic coding. Again, I made a
whole video about that previously
, but the short version is to open up Xcode’s Settings, select the Intelligence tab, then configure one or both of the built-in agents, or add your own if you prefer.
That sets up support for Xcode to talk to Claude and Codex directly, which means we can now integrate our skills.
This is where things take two directions depending on your goal, so I’ll show you both, starting with the easiest approach first.
The first step is to find the agent skill you want. For example, you might want to use my
SwiftUI agent skill, which helps write and improve any kind of SwiftUI project
So, you need to open that URL in your browser, and look for the install instructions. It should look like this:
npx skills add https://github.com/twostraws/swiftui-agent-skill --skill swiftui-pro
That’s a terminal command you need to run, so open the Terminal app on your Mac and run it. It will ask:
Which agents you want to install to. You’ll notice the default set includes Codex. If you want to add Claude Code, use the arrow keys to move down and press Space to select it. Hit return to continue.
Whether it should be installed in your current project or globally, so it works everywhere. Both are good options, but you’ll probably find globally more useful.
Whether it should copy the skill individually in lots of places, or use a symlink. The symlink approach means the skill only exists once on your computer, and other places just reference the original copy, so it’s preferred.
Then press return one last time to confirm your settings and install the skill.
That one installation process now means the skill is available in Claude Code, in both the command line app and the desktop app; in Codex, again in both the command line app and the desktop app; but also in Codex for Xcode.
work in Claude for Xcode, so if you’re using Claude there some additional instructions.
But if you’re in one of the other context, you’re all set – all you need to do is restart the app, e.g. quit and relaunch Xcode or Codex, and the skill is available.
Even better, if you want to update your installed skills in the future, you can do it all with one command:
I’ll show you how to use the skill in a minute, but first let’s handle the exception: making the skill work with Claude inside Xcode.
Right now at least, Claude likes to have its own folder for skills, and Apple has a documentation page up about
setting up coding intelligence
where it’s mentioned.
You need to scroll way down the page until you come to a section currently titled “Customize the Codex and Claude Agent environments”, where they tell you how to add skills and other files 
