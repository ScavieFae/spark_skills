# Great Book Skills

Books distilled into Claude Code skills. Load a book's wisdom as actionable guidance.

## What This Is

Great Book Skills are [Claude Code skills](https://docs.anthropic.com/en/docs/claude-code/skills) based on influential books. Each skill distills a book's core principles into instructions Claude can apply while working with you.

Think of it as having a writing coach, strategy advisor, or management mentor on call—except instead of asking "what would Grove say?", Claude already knows.

## Available Skills

### Writing
- **[Elements of Style](writing/elements-of-style/)** — Strunk & White's blade for cutting prose
- **[On Writing Well](writing/on-writing-well/)** — Zinsser's warm, exacting eye for nonfiction
- **[Bird by Bird](writing/bird-by-bird/)** — Lamott's survival guide for writers facing the blank page
- **[Hey Whipple, Squeeze This](writing/hey-whipple/)** — Sullivan's irreverent guide to advertising copy

### Strategy
- **[The Lean Startup](strategy/lean-startup/)** — Ries's methodology for building under uncertainty
- **[Good Strategy Bad Strategy](strategy/good-strategy-bad-strategy/)** — Rumelt's bullshit detector for strategy
- **[7 Powers](strategy/7-powers/)** — Helmer's diagnostic for durable competitive advantage

### Leadership
- **[High Output Management](leadership/high-output-management/)** — Grove's operating system for managers who build things
- **[The Manager's Path](leadership/managers-path/)** — Fournier's guide to each level of the engineering ladder
- **[Radical Candor](leadership/radical-candor/)** — Scott's discipline for feedback that's both kind and clear
- **[The First 90 Days](leadership/first-90-days/)** — Watkins' systematic approach to leadership transitions

### Product
- **[Inspired](product/inspired/)** — Cagan's diagnosis of product org dysfunction
- **[The Mom Test](product/mom-test/)** — Fitzpatrick's discipline for customer conversations that reveal truth

### Thinking & Decisions
- **[Thinking, Fast and Slow](thinking/thinking-fast-slow/)** — Kahneman's toolkit for when intuition lies

### Operations
- **[The Goal](operations/the-goal/)** — Goldratt's Theory of Constraints as diagnostic tool

### Communication
- **[Made to Stick](communication/made-to-stick/)** — Heath brothers' craft of ideas that survive

### Design
- **[Don't Make Me Think](design/dont-make-me-think/)** — Krug's commonsense approach to web usability
- **[The Design of Everyday Things](design/design-of-everyday-things/)** — Norman's systematic lens for user-centered design

## Understanding Skills

If you're new to Claude Code skills, here's what you need to know.

**Skills are instructions Claude loads when relevant.** Each skill is a markdown file (`SKILL.md`) that teaches Claude how to approach a specific kind of work. When you're drafting nonfiction and your writing feels stiff, Claude can load *On Writing Well* and apply Zinsser's principles. When you're evaluating a business strategy, it can load *Good Strategy Bad Strategy* and run Rumelt's diagnostic.

**Skills aren't always-on.** Claude reads each skill's description and decides whether to load it based on what you're working on. This means you can have many skills installed without bloating every conversation—only relevant ones activate.

**Skills can also be invoked directly.** Type `/on-writing-well` to explicitly load a skill, regardless of context. Some skills support modes or arguments: `/on-writing-well --revise` or `/mom-test "my interview transcript"`.

**Skills use tokens.** When a skill loads, its contents count against your context window. These skills are kept lean (under 300 lines each), but if you install many skills with overlapping domains (say, all three writing skills), they might all load when you're writing. That's useful if you want multiple perspectives, noisy if you don't.

---

## Installation

### Option 1: Add to your Claude Code settings

Skills are registered by pointing to the folder containing `SKILL.md`.

**For a single project** — add to `.claude/settings.json` in your project:

```json
{
  "skills": [
    "/path/to/great-book-skills/writing/on-writing-well",
    "/path/to/great-book-skills/strategy/good-strategy-bad-strategy"
  ]
}
```

**For all your projects** — add to `~/.claude/settings.json`:

```json
{
  "skills": [
    "/path/to/great-book-skills/writing/on-writing-well"
  ]
}
```

Replace `/path/to/great-book-skills` with wherever you cloned this repo.

### Option 2: Use the CLI

```bash
claude skill add /path/to/great-book-skills/writing/elements-of-style
```

This adds the skill to your user-level settings.

### How many should I install?

Start with one or two that match your current work. If you're doing a lot of writing, install a writing skill. If you're in strategy mode, install a strategy skill.

You *can* install all of them globally, but:
- Skills with overlapping domains may all load at once
- More skills = more potential context usage
- Some skills are better invoked explicitly than auto-loaded

A reasonable approach: install your most-used skills globally, keep specialized ones at the project level, and invoke others directly when needed.

---

## Usage

Once installed, skills activate automatically when the context matches their description. For *Elements of Style*, ask Claude to edit prose, tighten writing, or review for clarity—the skill loads without you asking.

You can also invoke directly:

```
/elements-of-style Review this paragraph for wordiness
```

Some skills have modes. *On Writing Well* supports three:

```
/on-writing-well --draft    # Scaffolding questions before you write
/on-writing-well --revise   # Diagnostic on an existing draft
/on-writing-well --polish   # Final pass, light touch
```

If you don't specify, the skill will determine the mode from context or ask.

## Philosophy

A great book skill isn't a book summary. It's a translation: taking what made the book useful and reformulating it as guidance Claude can execute.

**What makes a good skill:**
- **Actionable** — Not "good writing is clear" but "cut every word that serves no function"
- **Opinionated** — Captures the book's point of view, not generic advice
- **Expert frame** — Written as if by someone who's internalized the book, not summarized it
- **Contextual** — Knows when to apply (and when not to)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the skill template and guidelines.

## License

MIT. The skills are original distillations, not reproductions of copyrighted text.
