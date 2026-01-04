# Skill Upgrade Playbook

How to take a spark skill from "sensibility injection" to "directed workflow." Developed through upgrading the writing skills and Mom Test.

---

## The Core Distinction

**Sensibility injection:** Principles Claude absorbs and applies diffusely. The skill colors how Claude works, but doesn't direct a specific workflow. Fine for simple editorial skills (Elements of Style).

**Directed workflow:** Active modes, scaffolding questions, diagnostics, output formats. The skill guides a specific process. Better for complex, multi-stage work.

Most books benefit from the directed workflow treatment. The question is: what workflow does this book actually teach?

---

## The Upgrade Process

### 1. Understand the Book's Distinctive Angle

Before touching the skill, answer:

- **What does this book do that others don't?** (Zinsser = warmth + craft for nonfiction. Lamott = finding what's true, not what's polished. Fitzpatrick = pressure-testing conviction about users.)

- **What's the core tension or insight?** Find the thing that makes you uncomfortable. That's usually the real contribution. ("Bad conversations feel good." "Seek to be wrong." "The new paralysis is 'this is fine, why do I hate it?'")

- **Who is the author's voice?** Strunk is terse and imperious. Zinsser is warm but exacting. Lamott is permission-giving. Fitzpatrick is grizzled practitioner. The skill should sound like them.

### 2. Assess the Current Skill

Read it with these questions:

- **Is it sensibility or workflow?** Does it tell Claude how to think, or what to do?

- **Does it have modes?** Different books apply differently at different stages. If the book covers multiple phases of work, the skill needs modes.

- **Are the triggers specific?** "Use for writing" is useless. "Use when prose feels stiff and impersonal" is specific. "Use when you catch yourself saying 'customers want X'" is actionable.

- **Is there a diagnostic?** Can Claude actively analyze work against this book's standards?

- **Is there an output format?** Does Claude know how to present its work when using this skill?

### 3. Find the Modes

Most books have natural modes based on:

**Stages of work:**
- On Writing Well: Draft → Revise → Polish
- Bird by Bird: Stuck → Voice → Excavation
- Mom Test: Build (before) → Check (after)

**Types of input:**
- "I'm starting fresh" vs. "I have a draft"
- "I'm preparing" vs. "I'm debriefing"

**User's current problem:**
- "I don't know what to write" (stuck)
- "This could have been written by anyone" (voice)
- "What's worth keeping?" (excavation)

Name the modes in the user's language, not the book's jargon.

### 4. Design the Scaffolding

For each mode, what questions should be asked before work begins?

**Draft mode scaffolding (On Writing Well):**
1. What's the one thing this piece is about?
2. Who are you to the reader?
3. What surprised you?
4. Where does it end?

**Build mode scaffolding (Mom Test):**
1. What's the riskiest thing you believe?
2. What questions will test it without revealing it?
3. What commitment will you ask for?

Scaffolding questions should:
- Surface what the user knows (or doesn't)
- Create a compass for the work ahead
- Be answerable before the work, not after

### 5. Design the Diagnostics

For modes that analyze existing work, what should Claude look for?

**Structure a diagnostic as:**
1. Categories of issues to scan for (prioritized)
2. What to flag in each category
3. How to present findings (show the passage, name the issue, suggest the fix)

**Example (On Writing Well, Revise Mode):**
1. Where is the writer hiding? (institutional vagueness, hedges)
2. Clutter check (the kill list)
3. Unity check (voice wavering)
4. Lead and ending
5. The human check (does this sound like a person?)

### 6. Specify Output Formats

Tell Claude how to present its work. This makes the skill repeatable.

**Example (Bird by Bird, Voice Mode):**
1. Overall read: Is this draft generic throughout, or alive in places?
2. The generic passages: Quote them, name what's missing
3. The seeds: Anything with heat, specificity, surprise
4. Questions to surface specificity

**Example (Elements of Style):**
"Flag violations in order of impact. Show the original, show the fix, move on. Don't explain what Strunk would say. Just cut."

### 7. Sharpen the Triggers

The description field determines when the skill activates. Be specific.

**Weak:** "Writing advice based on this book"
**Strong:** "Activate when prose feels stiff, impersonal, or hiding behind formality"

**Weak:** "Customer research guidance"
**Strong:** "Activate when building conviction about users, when feedback 'feels positive,' or when you catch yourself saying 'customers want X'"

**Add a "When to Use This" section** for skills with non-obvious triggers. List concrete scenarios:
- "Writing a PRD and realizing you're guessing"
- "You just got off a call that felt really positive"
- "Sales says 'customers keep asking for Y'"

### 8. Update for the Current Moment

Some books need reframing for how work happens now.

**Bird by Bird's reframe:** The old paralysis was the blank page. The new paralysis is AI-generated text that's "fine" but dead. "This is fine. Why do I hate it?"

**The key question:** How does this book's wisdom apply when the first draft is already fluent? When the problem isn't starting, but finding what's true underneath the competent surface?

Not every book needs this treatment. But writing books especially benefit from acknowledging that the drafting problem has changed.

### 9. Find the Collaborative Posture

How do Claude and the user work together in this skill?

**Bird by Bird:** "We're finding this together. I can see patterns. You have the material."

**Mom Test:** "Think of this as the grizzled YC partner you get to pick the brain of."

**Elements of Style:** No collaboration—Strunk is imperious. That's the point.

The posture should match the book's teaching style.

### 10. Add Tool Restrictions

Use `allowed-tools` in frontmatter to focus the skill:

```yaml
allowed-tools: Read, Edit, AskUserQuestion
```

Writing skills shouldn't spawn agents. Editorial skills might only need Read and Edit. Be intentional.

---

## The Hologram Test

A great skill reflects the book's own principles:

- **On Writing Well** should be warm, direct, and clutter-free
- **Elements of Style** should be terse and imperious
- **Bird by Bird** should be permission-giving and truth-seeking
- **Mom Test** should be skeptical and plainspoken

If the skill doesn't feel like the book, something's wrong.

---

## After the First Pass: The Bird by Bird Lens

Structure isn't enough. After modes, scaffolding, and triggers are in place, apply Lamott's lens:

**Check for genericity:**
- What could anyone have written?
- Where are the details plausible but not observed?
- Does this sound like the author—or like a summary of the author?

**Find the heat:**
- Which sentences sting because they're true?
- Where's the surprise, the risk, the specific?
- What would someone who's lived this book recognize?

**Tighten relentlessly:**
- Every pass, tighten. The 3x3 bullet grid becomes three sentences.
- Clever phrases that don't earn their length get cut.
- If modes overlap, consolidate—fuzziness means accidental calls and wasted context.

**Level up LLM-isms:**
- Watch for patterns like "It's not X, it's Y" and similar constructions.
- Don't fear them in first drafts. Revise them into something stronger.
- We improve by revising, not by avoiding.

---

## Checklist for Upgrade

- [ ] Identified the book's distinctive angle
- [ ] Found the uncomfortable insight
- [ ] Defined modes (if applicable)
- [ ] Created scaffolding questions for each mode
- [ ] Designed diagnostics for analysis modes
- [ ] Specified output formats
- [ ] Sharpened the description triggers
- [ ] Added "When to Use This" if triggers aren't obvious
- [ ] Updated for current moment (if relevant)
- [ ] Defined the collaborative posture
- [ ] Added `allowed-tools`
- [ ] Verified the skill sounds like the author
- [ ] Kept it under 300 lines (or used progressive disclosure)
- [ ] Applied Bird by Bird lens for genericity and heat
- [ ] Tightened until nothing's wasted

---

## Skills Upgraded So Far

| Skill | Modes | Key Reframe |
|-------|-------|-------------|
| On Writing Well | Draft / Revise / Polish | Scaffolding questions before drafting |
| Bird by Bird | Stuck / Voice / Excavation | "This is fine. Why do I hate it?" — finding truth in the AI era |
| Elements of Style | None (diffuse blade) | Just cut. Don't explain. |
| Mom Test | Build / Check | "Building conviction without evidence" as the trigger |
| Inspired | Diagnose / Discover / Evaluate | "None of it matters" — the felt experience of the feature factory |

---

## Remaining Skills to Upgrade

- Good Strategy Bad Strategy
- 7 Powers
- High Output Management
- The Manager's Path
- Radical Candor
- Thinking Fast and Slow
- The Goal
- Made to Stick
- Lean Startup

Each needs the same analysis: What's distinctive? What are the modes? What's the current-moment reframe? What's the hologram quality? Then the Bird by Bird lens for genericity and heat.
