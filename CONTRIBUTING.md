# Contributing a Spark Skill

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

## Licensing

Spark skills are original distillations, not reproductions. Include only:
- Principles restated in your own words
- Common examples (or create your own)
- The book's structure reimagined for action

Do not include:
- Extended quotes
- Proprietary frameworks verbatim
- Content that would substitute for buying the book

The goal is to make the book's wisdom *actionable*, not to replace reading it.
