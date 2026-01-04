# Contributing a Great Book Skill

How to turn a book into a skill.

## The Translation Problem

A book teaches through explanation, examples, and narrative. A skill instructs through directives Claude can execute. The job isn't to summarize—it's to translate.

Ask: **What does someone who's read this book *do* differently?** That's your skill.

## Before You Start

Not every book makes a good skill. Good candidates:

- **Prescriptive over descriptive** — Books that tell you *what to do*, not just *what is*
- **Actionable principles** — Ideas that translate to concrete instructions
- **Distinctive point of view** — Generic advice isn't worth loading

Skip books that are mainly:
- Inspirational/motivational (no actionable content)
- Deeply contextual (require case-by-case judgment the book can't encode)
- Already in Claude's training (common knowledge dressed up)

## Skill Structure

```
category/book-name/
└── SKILL.md
```

### SKILL.md Template

```markdown
---
name: book-name
description: When to activate this skill. Be specific about the task type (editing, planning, reviewing) and context. This is the trigger—if it's vague, the skill won't fire at the right time.
---

# Book Title

One line: what this is and what it's for.

## Core Principle

The book's central insight, stated as an imperative. If the reader remembers nothing else, this.

## [Action Category 1]

Group related principles by what you DO with them. Not "Chapter 3" but "Cutting" or "Structuring Arguments" or "Building Trust."

Instructions in imperative form. "Do X" not "One should do X."

Examples where they clarify. Before → After format works well.

## [Action Category 2]

More principles, more instructions.

## Quick Reference

Optional checklist or test. A way to audit work against the book's standards.
```

### Writing Guidelines

**Imperative form.** "Cut filler words" not "You should cut filler words" or "Filler words should be cut."

**Capture the voice.** Strunk is terse and imperious. Zinsser is warm but direct. Lamott is permission-giving. The skill should feel like the book.

**Concise.** Claude already knows how to write, lead, negotiate. You're adding the book's specific perspective and techniques, not teaching fundamentals.

**Organize by action.** Group principles by what you do with them, not by where they appear in the book.

**Include examples.** Before/after pairs make abstract principles concrete.

## Description Field

The description determines when the skill activates. Be specific:

❌ "Writing advice from this book"
✅ "Apply when editing prose for clarity, cutting wordiness, or when user asks for concise writing"

❌ "Leadership principles"
✅ "Apply when planning difficult conversations, giving feedback, or navigating team conflict"

## Categories

Place skills in the appropriate category folder:

- `writing/` — Prose, editing, style
- `style-guides/` — Chicago, AP, technical writing standards
- `leadership/` — Management, communication, organizational
- `strategy/` — Business, decision-making, planning
- `craft/` — Domain-specific skills (design, engineering practices)

Create new categories as needed.

---

## Advanced Patterns

A basic skill is a *sensibility injection*—principles Claude absorbs and applies diffusely. That's useful, but skills can do more.

### Modes

Some books apply differently depending on where you are in the work. Instead of one-size-fits-all, let the skill branch:

```markdown
## When Activated

Determine the mode from context or by asking:

- **Draft mode** — "I'm starting fresh or still finding what I think"
- **Revise mode** — "I have a draft, help me see what's wrong"
- **Polish mode** — "Final pass, make it sing"
```

Each mode then has its own workflow. Users can also invoke explicitly: `/skill-name --revise`

### Scaffolding

Before the work begins, ask questions that shape it. This is especially powerful for drafting or planning:

```markdown
## Draft Mode: The Scaffolding Questions

Before writing, answer these:

### 1. What's the one thing this piece is about?
Not three things. One. If you can't say it in a sentence, you're not ready.

### 2. Who are you to the reader?
A guide? A friend? An expert reluctantly explaining?

### 3. What surprised you?
The piece lives in your genuine curiosity.
```

These answers become the compass. The skill holds them while the user works.

### Diagnostics

Instead of diffuse application, run an active diagnostic. Read the work and surface specific issues:

```markdown
## Revise Mode: The Diagnostic

Read the draft with [Author]'s eye. Surface specific issues, ranked by impact.

### 1. [Category of problem]

Flag instances of:
- Pattern A
- Pattern B

For each: show the passage, name the issue, suggest the fix.

### 2. [Next category]
...
```

This turns the skill into an active workflow, not just flavor.

### Output Formats

Prescribe how Claude should present its work. This makes the skill repeatable:

```markdown
### Output format for Revise Mode

1. **Overall assessment** (2-3 sentences): What's working, what's the main issue
2. **Ranked issues** (most impactful first): Specific passages with diagnosis
3. **Suggested rewrites**: Show, don't just tell
4. **One question for the writer**: Something to sit with before the next pass
```

### Tool Restrictions

Use `allowed-tools` in the frontmatter to focus Claude on the right capabilities:

```yaml
---
name: on-writing-well
description: Zinsser's warm, exacting eye for nonfiction...
allowed-tools: Read, Edit, AskUserQuestion
---
```

A writing skill probably shouldn't run bash commands or spawn agents. Narrowing tools improves reliability.

### Progressive Disclosure

If a skill needs deep reference material, split it across files:

```
book-name/
├── SKILL.md          # Core workflow, under 300 lines
├── REFERENCE.md      # Detailed patterns, loaded on demand
└── EXAMPLES.md       # Before/after pairs
```

Claude loads `SKILL.md` first. Reference files load only when needed, reducing context cost.

---

## Choosing Your Pattern

| If the book is about... | Consider... |
|-------------------------|-------------|
| A craft with stages (drafting, editing, polishing) | Modes |
| Preparing before action (planning, interviews, negotiations) | Scaffolding |
| Evaluating existing work (code review, strategy audit, feedback) | Diagnostics |
| Dense reference material (style guides, frameworks) | Progressive disclosure |

Many skills combine patterns. *On Writing Well* uses all four: principles first, then modes for draft/revise/polish, scaffolding questions in draft mode, diagnostics in revise mode.

Start simple. Add structure when the skill's use case demands it.

---

## Licensing

Great book skills are original distillations, not reproductions. Include only:
- Principles restated in your own words
- Common examples (or create your own)
- The book's structure reimagined for action

Do not include:
- Extended quotes
- Proprietary frameworks verbatim
- Content that would substitute for buying the book

The goal is to make the book's wisdom *actionable*, not to replace reading it.
