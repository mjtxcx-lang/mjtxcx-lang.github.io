# Fable 5 vs. GPT-5.6 Sol on an NP-Hard Problem: Does /goal help?

**来源:** [https://charlesazam.com/blog/fable-5-gpt-5-6-sol-goal/](https://charlesazam.com/blog/fable-5-gpt-5-6-sol-goal/)

**日期:** 2026-07-21

## 中文概述

Fable 5在NP难优化问题上碾压GPT-5.6 Sol，/goal模式并非万能

---

## 原文摘录

I gave Claude Fable 5 and GPT-5.6 Sol the same unpublished NP-hard
optimization problem, with and without their native
mode. Fable 5 is an absolute beast;
is not a game changer.
This is an operations research problem originally submitted to students at a
hackathon. I spent a week years
ago writing C++ to solve it, so I have a useful human baseline.
Fable 5 was an absolute beast on this benchmark. It produced the best solution overall, and its
consistency is unlike anything I have seen from a model on this problem. This is pure raw
intelligence. Incredible.
The other result is that
is not a generic “try harder” switch. It changes the control
loop and the search path. Sometimes that finds a better basin. Sometimes it gives a bad idea
All code, prompts, result tables, exclusions, and trajectory notes are in
. This is a follow-up to my
first article about this benchmark
KIRO is a fiber-network design problem I worked on as an engineering student in 2018. Given
directed distance matrices for Grenoble, Nice, and Paris, the solver has to connect distribution
points and terminals using loops and short chains while respecting several structural
constraints. The objective is total cable length. Lower is better.
A valid network consists of redundant loops rooted at distribution hubs, with short branches
hanging from towers on those loops. Every tower must appear exactly once, and reversing a cable
segment can change its cost.
How large is the search space?
There is no single closed-form count because a solution can use any number of loops, variable
loop sizes, and differently anchored and ordered branches. But Paris alone gives a useful lower
Even if we ignore ordering and branches and only assign each of the 532 terminals to one of
11 distribution hubs, there are
possible assignments.
A stronger lower bound comes from one deliberately restricted family of valid solutions:
exactly 19 loops of 28 terminals each, with no branches. This covers all 532 terminals because
, while staying below the 30-terminal limit for a loop. Order the 532 terminals,
split that ordering into 19 consecutive groups, divide by
because the set of loops is
unordered, and choose one of the 11 hubs for each loop:
(532! / 19!) x 11^19 ~= 10^1223
The primary experiment was intentionally narrow:
Claude Fable 5, Opus 4.8, Sonnet 5; GPT-5.6 Sol, Terra, Luna
Maximum available setting for every model
Harbor 0.1.43, Docker, subscription authentication
Before concentrating repetitions on the flagship pair, I ran one matched 30-minute no-hint
pair for every model in the sweep. For Fable and Sol, the chart uses Pair 1 from the replicated
headline set; the other four models have one pair each.
I then repeated the flagship comparison until I had three matched runs for Fable 5 and three
was better. Goal won four of six trials, so win rate alone makes the
feature look useful. The means tell the other half:
Both models usually got a small benefit and occasionally suffered a large regression. That is
won most runs but made both means worse.
Fable was also clearly stronger. Its plain mean beat Sol’s by 1,875 points, and its goal mean
beat Sol’s by 1,984. More importantly, Fable plain stayed inside a tiny 319-point range while
Sol plain spanned 1,958 points. Fable goal produced the best clean score, 31,934; Fable plain
was the safest configuration.
Deep dive into the goal command
The same command hides two different systems
Claude Code and Codex both expose
, but the implementations are fundamentally different.
Claude Code: a separate evaluator
Claude Code implements
as a session-scoped Stop hook. After each main-model turn, a
small evaluator model, Haiku by default, reads the condition and conversation. It returns yes
or no with a reason. A no starts another turn; a yes clears the goal.
The evaluator cannot use tools or inspect files. It can only judge evidence that appeared in
the transcript. That can catch an early exit, but it cannot know whether another ten million
solver iterations are worthwhile.
Anthropic’s goal documentation
Keep in mind that claude code is not open source, so we rely solely on what Anthropic tells us.
Codex: persisted state and lifecycle tools
I also read the source for the benchmarked release,
. Codex treats a goal as
persisted thread state:
The TUI saves the objective for the active thread, and SQLite stores its status and budget
The working model receives
If the thread becomes idle while the goal is active, Codex injects a continuation turn with
the objective and a completion audit.
Claude delegates completion to another model. Codex lets the working model declare completion,
then resumes it while the persisted goal remains active. Claude’s evaluator is independent but
sees only the transcript; Codex sees the files and tools but effectively grades its own work.
can win most runs and still be a bad default
On a normal coding task, progress is often legible: another turn can fix a test or complete a
migration. Optimization is different. 
