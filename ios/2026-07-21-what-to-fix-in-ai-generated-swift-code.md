# What to fix in AI-generated Swift code

**来源:** [https://www.hackingwithswift.com/articles/281/what-to-fix-in-ai-generated-swift-code](https://www.hackingwithswift.com/articles/281/what-to-fix-in-ai-generated-swift-code)

**日期:** 2026-07-21

## 中文概述

AI生成Swift代码的常见问题清单：性能、可访问性、现代API使用

---

## 原文摘录

Save 50% on my books and bundles!
What to fix in AI-generated Swift code
As AI-assisted coding increases in popularity, here are a handful of things I would suggest you look out for – and what to replace them with instead.
Building apps in Swift and SwiftUI isn’t quite as easy for AI tools as other platforms, partly because our language and frameworks evolve rapidly, partly because languages such as Python and JavaScript have a larger codebase to learn from, and partly also because AI tools struggle with Swift concurrency as much as everyone else.
As a result, tools like Claude, Codex, and Gemini often make unhelpful choices you should watch out for. Sometimes you’ll come across deprecated API, sometimes it’s inefficient code, and sometimes it’s just something we can write more concisely, but they are all easy enough to fix so the key is just to know what to expect!
Before I start, I want to mention three things up front:
This advice assumes you’re able to target modern versions of iOS, i.e. iOS 18 or later. If you need to support older versions, your AI of choice will have a better chance of getting it correct.
This is not designed to be an exhaustive list; it’s just the most common things I look out for.
I’m not interested in arguing about whether LLMs are good or not; I accept they exist, and that many people want to use them, so I might as well help folks use them better.
You know how to code. Now learn how to
My new app focuses on everything around your app that actually determines success, bringing together your App Store listing, competitor research, pricing, reviews, analytics, marketing, and launch workflow so you're never figuring it out alone.
Download Kickstart here
. It’s the same number of characters to type, but the former is deprecated, whereas the latter supports more advanced features like gradients.
clipShape(.rect(cornerRadius:))
. Again, the former is deprecated, whereas the latter offers more advanced features such as uneven rounded rectangles.
modifier should not be used in its 1-parameter variant. Either accept two parameters or none, but the old variant is unsafe and deprecated.
modifier, replace it with the new
API instead. This lets you benefit from the new type-safe tab selection, and also adopt things like the iOS 26 search tab design.
Replace almost all use of
with an actual button – the only exceptions are where you need to know a tap’s location or the number of taps. This is significantly better for VoiceOver, but also means things like eye tracking on visionOS works better.
macro, unless you specifically rely on the Combine publisher for some reason. This lets your code be simpler and faster too.
Be careful if you see
in SwiftData model definitions – this does
If it break ups views by placing things into computed properties, tell it to split them out into separate SwiftUI views instead. This is important for performance when using
– computed properties do
benefit from the intelligent view invalidation of
Some LLMs (particularly Claude) love to force specific font sizes – search for
and replace as many of them as you can using Dynamic Type fonts. (If you can support iOS 26 or later, you can also use
.font(.body.scaled(by: 1.5))
Watch out for using the old, inline destination
API in lists, and replace it with
navigationDestination(for:)
Expect to see button labels being made with
rather than the newer, inline API (
Button("Tap me", systemImage: "plus", action: whatever)
), or, worse, with just an image – it’s a real problem for VoiceOver users.
ForEach(Array(x.enumerated()), id: \.element.id)
ForEach(x.enumerated(), id: \.element.id)
You can safely replace the longer code to find the documents directory with just
URL.documentsDirectory
. The only reason to stay with the former is if you still need to support iOS 15.
Task.sleep(nanoseconds:)
back from the dead. You’re looking for
I know the resulting code is longer, but try to replace C-style number formatting with the safer versions. For example,
Text(String(format: "%.2f", abs(myNumber)))
Text(abs(change), format: .number.precision(.fractionLength(2)))
Watch out for it placing lots of types in a single file – it’s a fantastic way to guarantee longer build times.
If you’re rendering SwiftUI views, you should replace
UIGraphicsImageRenderer
All three popular LLMs seem to enjoy over-using the
modifier. See above about Dynamic Type, but also remember that
do not always produce the same result.
If the LLM hits a concurrency problem, you can expect to see
DispatchQueue.main.async
used an unreasonable number of times. (We only have ourselves to blame for this, but still – ditch it!)
If you’re working with a new app project, main actor isolation is on by default so you don’t need to mark things with
– boy oh boy do LLMs love
, often combined with the other cardinal sin of adding fixed frame sizes where they don’t belong. Please consider some of the alternatives instead, including
containerRelativeFrame()
Finally, no article on this c
