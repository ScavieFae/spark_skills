---
name: the-goal
description: Theory of Constraints as diagnostic tool. Activate when everyone's busy but nothing ships, when queues grow despite heroics, when you hear "we need to go faster" but can't say where. Find the one thing that limits throughput. Everything else is noise.
allowed-tools: Read, Edit, AskUserQuestion
---

# The Goal

You don't have a productivity problem. You have a constraint problem.

Every system has exactly one constraint—the point that limits total throughput. Everything upstream produces faster than the constraint can consume. Everything downstream starves. Until you address that point, improving anything else just builds inventory.

Inventory is money trapped in the system. Work in progress that hasn't become value. Queues.

---

## When to Use This

**Something's stuck and you don't know why:**
- Everyone's busy but output isn't increasing
- You keep adding people but queues grow
- "Waiting on X" is a permanent status
- Work starts fast, finishes slow

**You're about to "improve efficiency":**
- Someone wants to speed up a process
- You're optimizing a team's workflow
- A manager is proud of high utilization
- Leadership wants to "do more with less"

**Heroics aren't working:**
- The team that works hardest is always underwater
- One person leaving would break everything
- Deadlines slip despite overtime

**The question to ask yourself:** Where does work wait? Not where is work hard. Not where are people stressed. Where does it *wait*.

---

## The Principles

These are non-negotiable. Violate them and you'll optimize your way into gridlock.

### Throughput, not utilization

A team at 100% utilization is a team with maximum queues.

Variation exists in every system. When a stage has no slack, variation becomes delay. Delay compounds through dependent stages. Five stages with 10% variation each don't produce 10% output variation—they produce gridlock.

You need slack everywhere except the constraint. Non-constraint resources should be "underutilized." That's the system working.

### Finishing beats starting

Every piece of WIP is inventory. Money in, value not out. The more you start, the slower everything finishes.

Stop starting. Start finishing.

### Local speed creates global delay

An efficient upstream station pushing into a constrained downstream isn't efficient. It's creating blockage.

If someone's proud of 100% utilization upstream of a bottleneck, they're bragging about how efficiently they create waste.

### The constraint moves

Fix one constraint, another emerges. The policies built for the old constraint now strangle flow. When throughput stalls again, question everything—especially the rules that used to work.

---

## When Activated

Determine the mode from context or by asking:

- **Diagnose mode** — "Something's stuck. I need to find the constraint."
- **Exploit mode** — "I know where the bottleneck is. Help me get more from it."
- **Subordinate mode** — "How do I reshape everything else around the constraint?"

---

## Diagnose Mode: Finding the Constraint

You know something's wrong. Work accumulates. Things slow down. But you don't know *where*.

### The Socratic questions

These are Goldratt's questions. Answer them and the constraint reveals itself.

**1. Where does work wait?**

Not where work is hard. Not where people are stressed. Where does it *accumulate*?

In a factory: inventory stacked before a station. In software: PRs aging in review, tickets stuck in a column, deploys waiting for windows, features blocked on one person's approval.

Walk the flow. Look for queues. The constraint is where work piles up.

**2. What's the cycle time by stage?**

If you can't see queues directly, measure. Where does the gap between "started" and "finished" explode?

A ticket takes 2 hours of work and 3 weeks to finish. Where are those 3 weeks hiding?

**3. Who never has an empty queue?**

That's a candidate. The person or team where work is always waiting isn't necessarily slow—they're the constraint.

**4. What happens when that point is unavailable?**

If one person's vacation causes panic, one team's backlog freezes everything, one system's downtime stops all progress—you've found a constraint.

### The diagnostic output

After exploring the flow, summarize:

1. **The flow map**: How does work move from start to value delivered?
2. **Where queues form**: Specific stages where work accumulates
3. **Candidate constraints**: The 1-2 most likely bottlenecks
4. **What to measure**: If still unclear, what data would reveal it?

### Common constraints in software teams

**Code review.** PRs age in queue. Authors context-switch; reviews arrive to forgotten context. *Tells: high PR age, growing PR count, "waiting on review" as permanent status.*

**A single engineer.** One person owns a critical system. Everything routes through them. *Tells: their queue never empties, their vacation causes panic, "we need to ask [name]."*

**Deployment.** Code merges but doesn't ship. Batches grow. *Tells: merge-to-deploy gap grows, release notes become novels.*

**Test infrastructure.** Suite takes hours. Developers avoid tests. Flaky tests get ignored. *Tells: long CI queues, "merge and fix forward," test failures as noise.*

**Decisions.** Features wait for approval. Specs wait for alignment. *Tells: "blocked on decision" status, design docs aging, meetings that don't resolve.*

---

## Exploit Mode: Maximizing the Constraint

You've identified the bottleneck. Before adding resources (elevate), extract everything possible from what you have.

### The Socratic questions

**1. Is the constraint ever idle?**

The constraint should never wait for work. Not for input. Not for decisions. Not in meetings. Every minute of constraint idle time is throughput lost forever.

What makes the constraint wait? Incomplete inputs? Missing context? Rework cycles? Interruptions?

**2. What does the constraint work on?**

Is every task at the constraint genuinely high-value? Or does low-priority work consume constraint time because everything routes there?

If the constraint is a person: what are they doing that someone else could do? If it's a process: what work shouldn't flow through it at all?

**3. What causes rework at the constraint?**

Every time work returns to the constraint, throughput dies. What arrives incomplete? What comes back for revision? What could be done right the first time upstream?

**4. What's the batch size?**

Large batches mean long waits. Can the constraint process smaller pieces, more frequently?

### The exploitation output

For the identified constraint:

1. **Current waste**: Where constraint time is lost (idle, interruptions, rework, low-value work)
2. **Protection measures**: How to ensure the constraint never waits
3. **Quality gates**: What upstream must get right to avoid rework
4. **Batch size**: Whether smaller, more frequent work would increase flow

### Exploitation patterns

**For review bottlenecks:** Reviews arrive complete. Reviewers aren't pulled into meetings. Review has dedicated, protected time. PRs include context (not "see Slack").

**For single-engineer bottlenecks:** Others handle triage. Documentation exists. Decisions get made in their absence for known patterns. They only see the novel problems.

**For deployment bottlenecks:** Deploy criteria are explicit. Rollback is fast. Deploy happens more frequently with smaller batches. The window isn't artificial.

---

## Subordinate Mode: Reshaping the System

Now the hard part. Everything else adjusts to serve the constraint's pace.

### The Socratic questions

**1. What's producing faster than the constraint can consume?**

That's building inventory. That's waste. It feels productive—people are busy!—but it creates queues that slow everything.

What should slow down?

**2. Is downstream ready when the constraint releases work?**

The constraint finishes something. Does it flow immediately, or wait again? Downstream should have slack. Ready the instant work arrives.

**3. What local metrics are you optimizing?**

Story points per sprint. Tickets closed. Lines of code. These local metrics become the enemy when they don't measure throughput through the constraint.

What metrics should die?

**4. What policies exist for the old constraint?**

When the constraint was elsewhere, you built rules. Those rules may now strangle flow. What's still running on autopilot?

### The subordination output

1. **What slows down**: Upstream activities that should produce less
2. **What speeds up**: Downstream activities that should have slack
3. **Metrics to kill**: Local measures that conflict with global throughput
4. **Policies to question**: Rules from when the constraint was elsewhere

### The discomfort

Subordination feels wrong.

People will be idle. Resources will be "underutilized." Managers will ask why the team isn't at capacity.

That's the system working. Slack is not waste. Slack is what allows flow.

When someone protests that their team is sitting idle upstream of the constraint, ask: "What's their utilization creating?" If the answer is inventory, they're efficiently making things worse.

---

## The Five Focusing Steps (Reference)

Always in this order:

**1. Identify.** Find the constraint. Follow the queues.

**2. Exploit.** Get everything possible from the constraint without adding resources.

**3. Subordinate.** Adjust everything else to the constraint's pace. Accept idle time elsewhere.

**4. Elevate.** Now add capacity to the constraint. Only after exploit and subordinate—otherwise new capacity sits idle too.

**5. Don't let inertia become the constraint.** When you elevate, the constraint moves. Something else is now slowest. Go back to step 1.

---

## Signs You're Wrong

**You misidentified the constraint:**
- You exploited and subordinated, but queues didn't shrink
- Throughput stayed flat despite idle time appearing
- A different queue started growing

**You're not subordinating:**
- People upstream are "busy" but the constraint is starving
- Work arrives at the constraint incomplete
- Constraint workers get pulled into non-constraint activities

**You elevated too early:**
- You added capacity but throughput didn't increase
- New capacity sits idle
- The real constraint was hiding behind the apparent one

---

## The Goal Is the Goal

Throughput. Value delivered to customers, converted to money.

Not utilization. Not velocity. Not story points. Not features shipped. Throughput: the rate at which the system generates its goal.

Everything—including this methodology—is means. If a step doesn't increase throughput through the constraint, don't do it.

The question is always: what is the one thing limiting the system's output? Find it. Exploit it. Subordinate to it. Only then add capacity.

Then find the new constraint. The work is never done.
