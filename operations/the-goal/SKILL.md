---
name: the-goal
description: Theory of Constraints as diagnostic tool. Activate when throughput is stuck—everyone's busy but nothing ships, queues keep growing, deadlines slip despite heroics. Find the bottleneck. Fix it. Everything else is waste.
---

# The Goal

You don't have a productivity problem. You have a constraint problem.

## The only question that matters

Where does work pile up?

That's your constraint. Everything upstream produces faster than the constraint can consume. Everything downstream starves. Until you fix that point, nothing else matters.

Not "where are people struggling." Not "what takes longest." Where does work *wait*.

## How to find it

Walk the flow. Look for queues.

In a factory: inventory stacked before a station. In software: PRs awaiting review, tickets stuck in a column, deploys waiting for a window, features waiting for one person's approval.

The constraint reveals itself in wait time, not work time.

If you can't see queues, track cycle time by stage. Where does the gap between "started" and "finished" explode?

## What not to do

**Don't balance capacity.** Your instinct is to level-load—everyone at 80%, smooth and fair. This destroys throughput.

Variation compounds through dependent stages. Five stages fluctuating 10% each don't produce 10% fluctuation in output. They produce gridlock. Upstream variation dumps into the constraint; downstream starves.

You need *slack* everywhere except the constraint. Non-constraints should have excess capacity. Yes, they'll look "underutilized." That's correct.

**Don't optimize non-constraints.** Making a fast station faster produces nothing but inventory. Inventory is money trapped in the system.

If someone's proud of 100% utilization upstream of a bottleneck, they're bragging about how efficiently they create waste.

## The five moves (always in order)

**1. Identify.** Find the constraint. Follow the queues. Don't guess—find where work waits.

**2. Exploit.** Get everything possible out of the constraint *without spending money*. If code review is the bottleneck: stop pulling reviewers into meetings, ensure reviews arrive complete (no rework cycles), eliminate idle time at the constraint. The constraint should never wait for work.

**3. Subordinate.** Everything else adjusts to serve the constraint's pace.
- Upstream produces only what the constraint can consume. Resources will sit idle. That's correct.
- Downstream stays ready the instant the constraint releases work.
- Everyone's local efficiency becomes irrelevant. Only throughput through the constraint matters.

Subordination feels like waste. It looks like people waiting. That's the system working.

**4. Elevate.** *Now* spend money. Add capacity to the constraint. Only after you've exploited and subordinated—otherwise you're adding capacity that sits idle.

**5. Don't let inertia become the constraint.** When you elevate, the constraint moves. Something else is now slow. Go back to step 1. Policies built for the old constraint will strangle new flow.

## In software teams

Common constraints and their tells:

**Code review.** PRs age in queue. Authors context-switch while waiting; reviews arrive days later to forgotten context. *Tells: high PR age, growing PR count, "waiting on review" as permanent status.*

**A single engineer.** One person owns a critical system. Everything routes through them. *Tells: their queue never empties, their vacation causes panic, "we need to ask [name]" is common.*

**Deployment.** Code merges but doesn't ship. Batches grow waiting for windows. *Tells: gap between merge and deploy grows, release notes become novels, hotfixes take weeks to reach users.*

**Test infrastructure.** Suite takes hours. Developers avoid running tests. Flaky tests get ignored. *Tells: long CI queues, "I'll merge and fix forward," test failures as background noise.*

**Environment access.** Can't spin up a test environment. Work queues for shared staging. *Tells: environment conflicts, "waiting for staging," works-on-my-machine escalations.*

## The uncomfortable truths

**Utilization is not productivity.** A team where everyone is 100% utilized is a team with maximum queues, not maximum throughput. Variation exists; full utilization means gridlock. You want slack.

**Finishing beats starting.** Every piece of WIP is inventory: money in, value not out. More WIP means slower flow. Stop starting. Start finishing.

**Local speed creates global delay.** An efficient upstream station pushing into a constrained downstream isn't efficient. It's creating blockage. Slow the fast parts to match the constraint.

**It moves.** Fix one constraint, another emerges. The policies you built for the old constraint now strangle flow. When throughput stalls again, question everything.

## Signs you're wrong

You misidentified the constraint:
- You exploited and subordinated but queues didn't shrink
- Throughput stayed flat despite idle time appearing
- A different queue started growing

You're not subordinating:
- People upstream are "busy" but the constraint is starving
- Work arrives at the constraint incomplete, needs rework
- Constraint workers get pulled into non-constraint activities

You elevated too early:
- You added capacity but throughput didn't increase
- New capacity sits idle
- The real constraint was hiding behind the apparent one

## The goal is the goal

Throughput. Value delivered to customers, converted to money.

Not utilization. Not velocity. Not "features shipped." Throughput: the rate at which the system generates its goal.

Everything—including this methodology—is means. If a step doesn't increase throughput through the constraint, don't do it.
